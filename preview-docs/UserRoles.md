# RFC: User Roles in Apollo Studio

At the request of many, we are doing some work to make user roles configurable at the organization and graph level in [Apollo Studio](https://studio.apollographql.com).

We are looking for feedback on whether our plans will fit the needs of your organization .

If you have a need that is not encapsulated below, or if you see things we might be missing, please engage with us and ask questions through issues on this repository.

### Proposed Phases

**Phase 1: Organization-wide, pre-defined user roles**
Users can be designated as one of 4 distinct user roles, pre-defined within Apollo Studio. Those roles will control permissions a given user has for **all** graphs within your organization. We are starting with this because it's useful in many cases and can be launched sooner and independently from subsequent phases. This is likely to be a feature only available to paid accounts.

**Phase 2: Per-graph, pre-defined user roles**
Using the same roles as phase 1, apply them on a per-graph basis to specific users. This will allow someone to admin one graph but have read-only access to another, for instance. For any graph, you can set a specific role for a user to be higher than their default role, which would be their role in the org. When that user tries to access the graph, their permisisons on the graph will be the maximum of their permissions in that specific graph and in the org. This is likely to be a feature only available to "enterprise" plans.

**Phase 3: Private graphs + Custom roles + team management**
More flexible permisions, with some amount of customization and/or custom roles. This phase will also likely allow hiding graphs entirely from some people.

**Phase 4: SAML attribute automation**
Automated permissions based on mapping SAML attributes and/or other mechanisms to more tightly integrate existing SSO systems with specific permissions and/or roles.

### Proposed Roles

We anticipate exposing 4 primary roles ot start. Unless you're on our private roles beta (you would know), everyone in your organization right now is an **Admin**.

- **Billing Manager** — full admin access to configuration on your organization, its billing, and its members, but no access to graphs.
- **Consumer** — full access to the Documentation and Explorer pages in Studio, but limited access to everything else. This role can be considered "read-only".
- **Contributor** — basically everything an admin can do, minus a few very destructive acts like deleting graphs and adding other admins. You can make API keys, you can set up integrations, etc.
- **Admin** — full permission to change everything about the org and the graphs within it, incl. promoting other admins, inviting other users, transferring graphs, deleting graphs, etc.

New members can be invited as a Billing Manager, Consumer, Contributor, or Admin.
