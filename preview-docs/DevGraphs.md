# Preview: Graphs for Local Development

For a long time, we have wanted to make Studio's tools for writing queries and iterating on schema change accessible to folks during local development. Up until now, Studio's tools have mostly been designed to connect to graphs that are deployed and have lacked the responsivity to schema changes that's necessary for a nice local development experience.

We have recently added a new type of graph to Studio called a "Development Graph" with special properties:

- Dev graphs give you full access to Studio's Explorer and Schema tools for free, unlimited use.
- Dev graphs will poll your localhost and pick up changes to your schema as soon as you make them. Dev graphs will reload themselves automatically, so you can start querying those schema changes with no effort on your end.
- Dev graphs don't require any set up in your code. They provide tools entirely based on introspection and will work with every spec-compliant GraphQL server.
- Dev graphs are private to you. If your team already has some shared graphs in Studio, your teammates will not see your dev graphs in their list.

### Intended Use

We intend for folks to use dev graphs when running their servers locally to spike out changes to their schema and test their endpoints.

We have seen people use dev graphs in a variety of ways, from creating one per project to creating one per branch. Each dev graph is its own sandbox and isolated workspace, so you can have context in multiple workspaces at once even if you're switching branches locally or running different graphs on the same port.

#### Development Graph Workflow

Imagine your server printing on startup:

```
🚀  Server is running!
🔉  Listening on port 4000
📭  Query at https://studio.apollographql.com/dev
```

You follow the link to https://studio.apollographql.com/dev to query your localhost with Studio's [Explorer](https://www.apollographql.com/blog/introducing-the-apollo-explorer/):

![image](https://user-images.githubusercontent.com/5922187/94214674-0243d600-fe8f-11ea-9e3b-b08fe7facc90.png)

### On Our Minds

We aim to make dev graphs especially easy to use with Apollo Server, and will probably be considering a closer integration with Apollo Server over time.

We also aim to make more of the production tools in Apollo Studio available for dev graphs as we figure out in the future and invite feedback on how you'd want to use them in your development flow.

### We want to hear from you! Share your thoughts

Want to give the experience a try? Visit https://studio.apollographql.com/dev yourself to try things out. You can also clone https://github.com/daniman/graphql-server for a quick server starter if you don't have one handy.
