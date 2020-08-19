> **👋 Update:** The Explorer is now available for unlimited, free use in [Apollo Studio](https://studio.apollographql.com). Take a look at our [announcement post](https://www.apollographql.com/blog/introducing-the-apollo-explorer/) for more details on the specifics.

# Preview: Explorer

Welcome to the pre-release docs for the Explorer, a browser-based tool for exploring GraphQL schemas, composing queries, and testing responses.

## We'd love to hear your feedback

Before you start, please keep in mind that **we are very eager to hear your feedback**. We are very interested in seeing if the current experience is useful by itself and/or what other problems you want your graph exploring tools to provide.

1. Please [fill out our structured form](https://forms.gle/hhfA72JPC3fw43Wx5) after you have had a chance to use the Explorer for a few tasks if you are interested in sharing structured feedback.
2. For open-ended suggestions or bug reports, please submit an Issue in this repository.

## Getting Started

If you are reading this, you are someone we are showing this to "too early" with the explicit purpose of working with you to solve the problems that graph developers face.

To try the Explorer, visit <https://studio.apollographql.com/explorer>. You will need to login with your Apollo user account, create a graph, and publish your schema if you haven't done that before.

### Set up your graph

The Explorer is a client for querying your graph, much like GraphiQL and GraphQL Playground, but built by Apollo and hosted in the cloud.

#### Motivations for building a hosted GraphQL client

We seek to solve a set of problems that we've heard from graph administrators:

1. A simple way to provision access to a query design tool to consumers of my graph without needing to run additional software on my production systems.
2. An expressive and pleasant tool that incorporates reference documentation with an operation authoring experience, so consumers of the graph can quickly formulate the right query for their problem.
3. Provide tooling that can accommodate very large graphs, including nice ways to let certain consumers reason about subsets of the total graph while formulating their operations.
4. Provide stateful features like saved operations, collaboration, and incorporation of performance data and graph metadata into the experience.

#### Authentication

The Explorer does not explicity support any forms of authentication with endpoints. If you need to authenticate with your graph, you can do that by setting headers on your requests. The headers you set will be saved in your browser's local storage, one object entry per graph/variant pair.

We are extremely interested in hearing how you authenticate with your graph and what type of auth experience you would find ideal for a tool like Studio, so [please don't hold back from sharing them with us](https://forms.gle/hhfA72JPC3fw43Wx5).

#### CORS considerations

The queries you construct will be sent directly from the web app in your browser at https://engine.apollographql.com to your server. Many servers have [CORS protections enabled](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) that prevent requests from unknown URLs from being responded to. If your server has these protections enabled, you will likely need to safe-list (whitelist) https://engine.apollographql.com in your CORS policy so that your requests from Studio are not rejected.

We are extremely interested in hearing your thoughts on CORS, so [please don't hold back from sharing if you have them](https://forms.gle/hhfA72JPC3fw43Wx5).

### Features

The Explorer is a full-featured GraphQL client that comes out of the box with schema documentation and developer-friendly editor features like linting, autocomplete, cmd-click, peek definitions, HTTP metadata, and more.

#### Documentation for Query Building

In addition to the core editor, the Explorer provides a way to build and manage your queries from checkboxes in your Documentation tab.

![Screen Recording 2020-05-15 at 03 49 PM](https://user-images.githubusercontent.com/5922187/82102248-d126ee00-96c3-11ea-8c06-51e846112f5e.gif)

#### Spotlight Search

The Explorer comes with search designed to help you find what you're looking for extremely quickly. It also provides a way for you to add search results directly to your queries.

![Screen Recording 2020-05-15 at 04 53 PM](https://user-images.githubusercontent.com/5922187/82104685-a725f980-96cc-11ea-8b90-830c94ebfcb9.gif)

#### History Rewind

The Explorer remembers what you previously ran, allowing you to easily run queries you've run before.

![Screen Recording 2020-05-15 at 04 57 PM](https://user-images.githubusercontent.com/5922187/82104824-36331180-96cd-11ea-9a40-28ddbd1b7a06.gif)

## Try the demo

If you aren't an Apollo user already or don't have a graph available to try the Explorer with, you can join our demo account (Example Co.) to try out the Explorer. To do that, visit <https://demo.apollo.dev>, create an account, then [visit the `acephei` graph in Studio](https://studio.apollographql.com/studio/acephei?schemaTag=production).

An example query you can try on the `acephei` graph:

```
query {
  products {
    edges {
      product {
        name
        price
      }
    }
  }
}
```

#### Try Studio with the GitHub graph

Once you're a member of Example Co., you will also be able to [visit the `github` graph in the Explorer](https://studio.apollographql.com//graph/github/explorer) and run queries against that.

To authenticate with the GitHub graph properly, you will need to [get a personal access token](https://github.com/settings/tokens) and change your headers in Studio to this:

```
{
  "Content-Type": "application/json",
  "Authorization": "bearer XX-GH-PERSONAL-ACCESS-TOKEN-XX"
}
```

Note that the GitHub API does not like the Explorer's default `apollographql-client-name` header, so you will need to remove that one.

## Reminder: We'd love your feedback

If you made it to the end of this README, thank you for coming on this journey with us! Please remember that we're eager to hear any thoughts you have through our [feedback form](https://forms.gle/hhfA72JPC3fw43Wx5) and the Issues on this repository.
