# RFC: User Roles in Orgs and on Graphs

At the request of many, we are doing some work to make user roles configurable at the organization and graph level in [Apollo Studio](https://studio.apollographql.com).

We are looking for feedback from you on if these roles make sense, if you have a need that is not encapsulated in the proposal, if you see things we might be missing, etc. Please engage with us and ask questions through issues on this repository.

### Proposed Roles

We anticipate exposing 4 primary roles ot start. Unless you're on our private roles beta (you would know), everyone in your organization right now is an **Admin**.

- **Billing Manager** — full admin access to configuration on your organization, its billing, and its members, but no access to graphs.
- **Consumer** — full access to the Documentation and Explorer pages in Studio, but limited access to everything else. This role can be considered "read-only".
- **Contributor** — basically everything an admin can do, minus a few very destructive acts like deleting graphs and adding other admins. You can make API keys, you can set up integrations, etc.
- **Admin** — full permission to change everything about the org and the graphs within it, incl. promoting other admins, inviting other users, transferring graphs, deleting graphs, etc.

New members can be invited as a Billing Manager, Consumer, Contributor, or Admin.

### Roles on Graphs

We will start by building out user roles at the org level, but plan to follow that on with providing a configuration at the graph level soon after.

For any graph, you can set a specific role for a user to be higher than their default role, which would be their role in the org. When that user tries to access the graph, their permisisons on the graph will be the maximum of their permissions in that specific graph and in the org.
