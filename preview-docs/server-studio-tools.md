# The future of Apollo Server developer tooling

This document outlines details on some coming changes to Apollo Server related to the embedded GraphQL Playground.

## tldr: the short version
In a coming version of Apollo Server we will change the default behavior of Apollo Server in non-production mode
to stop serving the embedded version of GraphQL Playground by default and provide easier ways to connect your
server to the free developer tooling in Apollo Studio.

## A brief history of tooling in Apollo Server
One of the great things about GraphQL is that exploring and querying any GraphQL server can be done from the schema alone. Apollo Server has come "out of the box" with GraphQL Playground to make it simple to query your server easily. Over the years we've found GraphQL Playground to be useful, but limiting. In addition, one of our goals for the upcoming releases of Apollo Server is to decouple our dependencies on outside libraries. The version of Playground we are using is outdated, so we started evaluating what changes we could make in the future to keep the tooling that ships free with Apollo Server as good as we could make it.

## Apollo Studio developer tools
In 2020 Apollo set out to build the next generation of developer tooling for GraphQL and built the Explorer and schema documentation into Apollo Studio. Apollo also [announced last December](https://www.apollographql.com/blog/apollo-studio-a-graphql-ide-for-every-environment/)the introduction of (dev graphs)[https://www.apollographql.com/docs/studio/dev-graphs/], which made it practical to hook your local server up to the Explorer and other developer tools in Apollo Studio.

We've now had a few months to see how Apollo Explorer and dev graphs work, and we've talked to many teams about how their developers want to work. We've seen a tremendous response from our community, so we are ready to start using our free hosted tools as the default experience in your local Apollo Server. We also want to make it simple to configure your production servers to connect your users directly to the tools in Apollo Studio if you choose to do so.

## What will be changing?
When setting up a vanilla Apollo Server install today you get a running GraphQL Playground automatically. Instead, you will get a landing page that provides links to tooling options in Apollo Studio as well as links to documentation on how to configure your Apollo Server.

For a production server you will also be able to configure a plugin to always redirect to a graph page in Apollo Studio or to use GraphiQL.

## Feedback and questions
Please leave your feedback and questions on this issue: https://github.com/apollographql/apollo-studio-community/issues/79
