# Preview: Apollo Studio

Welcome to Apollo Studio, a browser-based tool for exploring GraphQL schemas, composing queries, and testing responses.

> *The documentation here is currently only a preview of pre-release software. You may use it at will, but this evaluation product is not yet fully supported or considered generally available. While we will try to avoid breaking changes once a feature is in use, until the features discussed herein are taken out of preview we could make breaking changes. Please be aware of the heightened risk of using preview software.*

> *Use of anything described in these preview docs (current as of May 2020) is done at your own risk and is governed by [The Apollo Terms of Service](https://www.apollographql.com/Apollo-Terms-of-Service.pdf).*

> *PREVIEWS ARE PROVIDED "AS-IS," "WITH ALL FAULTS," AND "AS AVAILABLE," AND ARE EXCLUDED FROM ANY SERVICE LEVEL AGREEMENTS AND LIMITED WARRANTY. Previews may not be covered by customer support. Previews may be subject to reduced or different security, compliance and privacy commitments, as further explained in the Terms of Service, Privacy Policy and any additional notices provided with the Preview. We may change or discontinue Previews at any time without notice. We also may choose not to release a Preview into "General Availability."*

## We'd love to hear your feedback

Before you start, please keep in mind that **we are very eager to hear your feedback**. We are very interested in seeing if the current experience is useful by itself and/or what other problems you want your graph exploring tools to provide.

1. Please [fill out our structured form](https://forms.gle/hhfA72JPC3fw43Wx5) after you have had a chance to use Studio for a few tasks if you are interested in sharing structured feedback.
2. For open-ended suggestions or bug reports, please submit an Issue in this repository.

## Getting Started

If you are reading this, you are someone we are showing this to "too early" with the explicit purpose of working with you to solve the problems that graph developers face. 

To try Apollo Studio, visit <https://engine.apollographql.com/studio>. You will need to login with your Apollo user account, create a graph, and publish your schema if you haven't done that before. Studio is currently only accessible by visiting this URL directly, so there are no links to it from within the rest of the Apollo app.

### Set up your graph

Studio is a client for querying your graph, much like GraphiQL and GraphQL Playgroud, but built by Apollo and hosted in the cloud.

#### Motivations for building a hosted GraphQL client

We seek to solve a set of problems that we've heard from graph administrators:
1. A simple way to provision access to a query design tool to consumers of my graph without needing to run additional software on my production systems.
2. An expressive and pleasant tool that incorporates reference documentation with an operation authoring experience, so consumers of the graph can quickly formulate the right query for their problem. 
3. Provide tooling that can accommodate very large graphs, including nice ways to let certain consumers reason about subsets of the total graph while formulating their operations.
4. Provide stateful features like saved operations, collaboration, and incorporation of performance data and graph metadata into the experience.

#### Authentication

Studio does not explicity support any forms of authentication with endpoints. If you need to authenticate with your graph, you can do that by setting headers on your requests. The headers you set will be saved in your browser's local storage, one object entry per graph/variant pair.

We are extremely interested in hearing how you authenticate with your graph and what type of auth experience you would find ideal for a tool like Studio, so [please don't hold back from sharing them with us](https://forms.gle/hhfA72JPC3fw43Wx5).

#### CORS considerations

The queries you construct will be sent directly from the web app in your browser at https://engine.apollographql.com to your server. Many servers have [CORS protections enabled](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) that prevent requests from unknown URLs from being responded to. If your server has these protections enabled, you will likely need to safe-list (whitelist) https://engine.apollographql.com in your CORS policy so that your requests from Studio are not rejected.

We are extremely interested in hearing your thoughts on CORS, so [please don't hold back from sharing if you have them](https://forms.gle/hhfA72JPC3fw43Wx5).

### Features

Studio is a full-featured GraphQL client that comes out of the box with schema documentation and developer-friendly editor features like linting, autocomplete, cmd-click, peek definitions, HTTP metadata, and more.

#### Documentation for Query Building

In addition to the core editor, Studio provides a way to build and manage your queries from checkboxes in your Documentation tab.

![Screen Recording 2020-05-15 at 03 49 PM](https://user-images.githubusercontent.com/5922187/82102248-d126ee00-96c3-11ea-8c06-51e846112f5e.gif)

#### Spotlight Search

Studio comes with search designed to help you find what you're looking for extremely quickly. It also provides a way for you to add search results directly to your queries.

![Screen Recording 2020-05-15 at 04 53 PM](https://user-images.githubusercontent.com/5922187/82104685-a725f980-96cc-11ea-8b90-830c94ebfcb9.gif)


#### History Rewind

Studio remembers what you previously ran, allowing you to easily run queries you've run before.

![Screen Recording 2020-05-15 at 04 57 PM](https://user-images.githubusercontent.com/5922187/82104824-36331180-96cd-11ea-9a40-28ddbd1b7a06.gif)


## Try the demo

If you aren't an Apollo user already or don't have a graph available to try Studio with, you can join our demo account (Acephei Corporation) to try out Studio. To do that, visit <https://demo.apollo.dev>, create an account, then [visit the `acephei` graph in Studio](https://engine.apollographql.com/studio/acephei?schemaTag=production).

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


## Reminder: We'd love your feedback

If you made it to the end of this README, thank you for coming on this journey with us! Please remember that we're eager to hear any thoughts you have through our [feedback form](https://forms.gle/hhfA72JPC3fw43Wx5) and the Issues on this repository.
