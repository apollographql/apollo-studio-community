# RFC: Graph Roles in Apollo Studio

> This is an Enterprise feature.

We recently [introduced user roles to Studio](https://www.apollographql.com/docs/studio/org/members/#member-roles) and are getting ready to tackle Phase 2 of the [roles and permissions plan](https://github.com/apollographql/apollo-studio-community/blob/main/preview-docs/UserRoles.md), which involves introducing access control to graphs.

We've identified new requirements for access control at the graph level since the first doc was written, including needs to control permissions with variant granularity.

Here's what we plan to do for the next phase of work in Studio on access control, which we hope will cover your needs for graph and variant permissions. If this plan does not address your needs, please let us know so we can understand what the gaps are.

1. Introduce a **Graph Admin** role that can operate with all permissions of the **Contributor** role, but can also manage user access to the graph (our current **Admin** role becomes **Org Admin**). When users create a graph, they are automatically the graph admin, and they can delegate that permission to other users by granting the graph admin role to other users on that graph.
2. Introduce a way to mark variants as **protected**. A protected variant is effectively _read-only_ to everyone who can see the graph except the graph admins and org admins, who have permission to push schemas, see keys, change configuration, etc.
3. Introduce a way to assign roles to graph API keys. We would make the **Consumer**, **Observer**, **Contributor**, and **Graph Admin** roles available for assignment on API key creation.
4. Introduce a setting on graphs that flags them as "visible" or "hidden" to the members of that graph's org by default. Right now, all graphs in the org are visible to all members of the org. If you mark a graph as "hidden" to your org, only you will see it. You can grant permission for other users in your org to see your graph as well.
