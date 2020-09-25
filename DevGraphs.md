# Preview: Dev Graphs

We have wanted to make Apollo Studio helpful to folks during local development for a long time. Up until now, Apollo Studio has largely been tailored to work with graphs already running in production.

Dev Graphs are **a new type of graph** that users can create in Studio. They have special properties that have been optimized for development-time concerns.

### Dev Graph Properties

- Dev graphs are set up and kept up-to-date with schema introspection.
- Dev graphs are unique to you –– only you can see and use the dev graphs you create.
- Dev graphs watch for changes to your server so they can update themselves near-instantaneously when your schema changes.
- Dev graphs are transient and can be considered "disposable" in your workflow (e.g. you could make a dev graph per branch).
- Dev graphs are sandboxes that are safe to experiment with, and completely separate from your other graphs in Studio.
- Every tool in dev graphs is completely free to use, and always will be.

Dev graphs contain a subset of Studio's full feature set right now:

- Explorer
- Schema Reference
- Schema Changelog

We will be introducing more of Studio's tools for regular graphs to dev graphs over time as we add support for local development to those features.

### Intended Use

We intend for folks to use dev graphs when running their servers locally to spike out changes to their schema and test their endpoints.

Imagine your server printing on startup:

```
🚀  Server is running!
📭  Query at https://studio.apollographql.com/dev
🔉  Listening at http://localhost:4000/
```

You follow the link to https://studio.apollographql.com/dev to query your localhost with [Apollo's Explorer](https://www.apollographql.com/blog/introducing-the-apollo-explorer/):

![image](https://user-images.githubusercontent.com/5922187/94214674-0243d600-fe8f-11ea-9e3b-b08fe7facc90.png)

### On Our Minds

We aim to make dev graphs especially easy to use with Apollo Server, and will probably be considering a closer integration with Apollo Server over time.

We also aim to make more of Studio's tools for regular graphs available in dev graphs as we figure out how those tools should work in a local development workflow.

### Share Your Thoughs Please Please Please

Want to give the experience a try? Visit https://studio.apollographql.com/dev yourself to try things out. You can also clone https://github.com/daniman/graphql-server for a quick server starter if you don't have one handy.
