# RFC: Graph Roles in Apollo Studio

> This is an Enterprise feature.

We recently [introduced user roles to Studio](https://www.apollographql.com/docs/studio/org/members/#member-roles) and are now tackling Phase 2 of the [roles and permissions plan](https://github.com/apollographql/apollo-studio-community/blob/main/preview-docs/UserRoles.md), which involves introducing access control to graphs.

We've identified new requirements for access control at the graph level since the first doc was written, including needs to control permissions with variant granularity.

1. Introduce a **Graph Admin** role that can operate with all permissions of the **Contributor** role, but can also manage user access to the graph and delete the graph. (Our current **Admin** role will be renamed to **Org Admin**. **Graph Admin**s and **Org Admin**s will have identical permissions to act on graphs, but org admins will also be able to manage org membership, billing, etc.)  The **Contributor** role will be made less powerful. It will not be able to perform management tasks on the graph like updating integrations and settings; it will have all the permissions of **Observer** plus the ability to push new versions of the graph's schema.
2. Introduce a way to override any role a user might have in the org with a higher role for a specific graph. A user might be an **Observer** in the org, but can be promoted to a **Contributor** on a specific graph. When users create a graph, they are automatically made **Graph Admin** on that graph. **Graph Admin**s and **Org Admin**s can update these graph-specific permissions.
3. Introduce a way to mark variants as **protected**. On a protected variant, you need to be a **Graph Admin** rather than a **Contributor** to push new versions of the graph's schema to that variant. **Graph Admin**s and **Org Admin**s can control whether variants are protected.
4. Introduce a way to assign roles to graph API keys. We would make the **Consumer**, **Observer**, **Contributor**, and **Graph Admin** roles available for assignment on API key creation. (Existing graph API keys continue to support the same operations they currently support.) **Graph Admins** can create and view graph keys with any role.
5. Introduce a setting on graphs that flags them as "visible" or "hidden" to the members of that graph's org by default. Right now, all graphs in the org are visible to all members of the org. If you mark a graph as "hidden" to your org, only users with explicit overridden roles on the graph (as described in "2") or who are **Org Admin**s can see it. **Graph Admin**s and **Org Admin**s can control whether graphs are hidden.


**We intend to release these new features on Tuesday, January 19th.** For full details on precisely what each role will be able to do after this feature is release, you can view a [preview of the docs](https://deploy-preview-1080--studio-docs.netlify.app/bdocs/studio/org/members/).

The following visible changes will occur when the features are released:

- All **Admin**s will now be called **Org Admin**s.
- All **Contributor**s will be changed to **Graph Admin**s. In addition to what they could do before, these users can now delete graphs and manage graph-specific permissions. If this is more than these users should be able to do, you may want to change them to being **Contributor**s instead.
- A new **Contributor** role will be created. This new **Contributor** is nearly identical to **Observer**, except that it can also perform a small set of write operations on non-protected variants.
- **Observer**s will no longer be able to view integration settings, as some of these settings contain sensitive information.
- Newly created graph API keys will have a role associated with them (**Graph Admin** by default). Existing graph keys will be identified as "Legacy Admin"; they continue to have the same permissions as before (as described in the [docs preview](https://deploy-preview-1080--studio-docs.netlify.app/bdocs/studio/org/members/#graph-key-roles).
