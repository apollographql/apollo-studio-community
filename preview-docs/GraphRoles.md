# RFC: Graph Roles in Apollo Studio

> This is an Enterprise feature.

We recently [introduced user roles to Studio](https://www.apollographql.com/docs/studio/org/members/#member-roles) and are getting ready to tackle Phase 2 of the [roles and permissions plan](https://github.com/apollographql/apollo-studio-community/blob/main/preview-docs/UserRoles.md), which involves introducing access control to graphs.

We've identified new requirements for access control at the graph level since the first doc was written, including needs to control permissions with variant granularity.

Here's what we plan to do for the next phase of work in Studio on access control, which we hope will cover your needs for graph and variant permissions. If this plan does not address your needs, please let us know so we can understand what the gaps are.

1. Introduce a **Graph Admin** role that can operate with all permissions of the **Contributor** role, but can also manage user access to the graph and delete the graph. (Our current **Admin** role will be renamed to **Org Admin**. **Graph Admin**s and **Org Admin**s will have identical permissions to act on graphs, but org admins will also be able to manage org membership, billing, etc.)  The **Contributor** role will be made less powerful. It will not be able to perform management tasks on the graph like updating integrations and settings; it will have all the permissions of **Observer** plus the ability to push new versions of the graph's schema.
2. Introduce a way to override any role a user might have in the org with a higher role for a specific graph. A user might be an **Observer** in the org, but can be promoted to a **Contributor** on a specific graph. When users create a graph, they are automatically made **Graph Admin** on that graph.
3. Introduce a way to mark variants as **protected**. On a protected variant, you need to be a **Graph Admin** rather than a **Contributor** to push new versions of the graph's schema.
4. Introduce a way to assign roles to graph API keys. We would make the **Consumer**, **Observer**, **Contributor**, and **Graph Admin** roles available for assignment on API key creation. (Existing graph API keys would act as **Contributor**s.)
5. Introduce a setting on graphs that flags them as "visible" or "hidden" to the members of that graph's org by default. Right now, all graphs in the org are visible to all members of the org. If you mark a graph as "hidden" to your org, only users with explicit overridden roles on the graph (as described in "2") or who are **Org Admin**s can see it. (While **Org Admin**s will have full read and write access to hidden graphs, hidden graphs that they do not have explicit overridden roles on may still be hidden by default from graph lists in the UI unless explicitly requested.)

### Other considerations

This plan does not yet tackle variant-specific tokens, but we think there's value to that and will likely end up adding that as well sooner rather than later.

Having variant-specific tokens will allow us to create contributor tokens for protected variants, which would save us from needing an added Deployer role in between Contributor and Graph Admin at some point.
