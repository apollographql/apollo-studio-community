# Apollo Studio

Welcome to the community feedback repo for [Apollo Studio](http://studio.apollographql.com/), a web-based suite of tools that help you build and evolve your GraphQL API.

We use this repository to engage with our Studio users and **track bugs**, **feature requests**, **ideas**, etc. We read _everything_ that comes in here and are grateful to you for any time you spend sharing your thoughts with us. We also like to share early documentation here for things we're working on.

If you ever need urgent, SLA-backed support for Studio, please reach out to us through support@apollographql.com. We can't make any guarantees about the speed of our responses on this repository specifically.

## What is Studio

Studio has tools for several types of people in your organization, including administrators to your graph, contributors to your graph, and consumers of your graph.

### Developer Portal

By synchronizing your schema with Studio, you can create a developer portal for your team to access your graph that includes:

- Auto-documentation for your schema across all your environments
- Auto-generated schema changelog across all your environments
- Schema change notifications
- An IDE for querying your graph with significantly more usability features than other query IDEs in the ecosystem ([Explorer](https://www.apollographql.com/docs/studio/explorer))
- A mode to use the Explorer during local development and have it poll to keep itself up-to-date

### Usage Insights

Studio can also give you deep insights about your graph's usage if you synchronize usage data to it:

- High-level usage metrics analytics
- Schema change validation (using live usage data) for your CI checks
- Usage tracking on a per-client basis
- Operation tracing and error reporting

### Federation

If you're building a federated graph, Studio offers **Managed Federation** (a mode you can run your federation gateway in) that provides:

- Managed deploys for federated services (publish changes to implementing services without having to restart your gateway)
- An iterface to see the state of your partial schemas and their composition
- A composed schema view, with annotations to show the source of each part of your schema
- An added step of schema change validation that checks for a valid composition of your federated services
- Live query plans in the Explorer as you build operations

### Access Control

For teams that need fine-grained access control to Studio, you can contact our Sales team to get access to:
- User roles that can be applied to your organization or to specific graphs
- Extra visbility properties on graphs (e.g. hide graph for most people in org, invite just a few to collaborate with you)
- Protected variants
- SSO login integrations

For more info on Studio features and specifics, you can also [visit our docs](https://www.apollographql.com/docs/studio/).
