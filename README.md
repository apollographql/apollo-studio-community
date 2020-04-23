# Preview: Apollo Studio

Welcome to Apollo Studio, a browser-based tool for exploring GraphQL schemas, composing queries, and testing responses.


## Before you start: IMPORTANT DISCLAIMER

The documentation here is currently only a preview of pre-release software. You may use it at will, but this evaluation product is not yet fully supported or considered generally available. While we will try to avoid breaking changes once a feature is in use, until the features discussed herein are taken out of preview we could make breaking changes. Please be aware of the heightened risk of using preview software.

Use of anything described in these preview docs (current as of April 2020) is done at your own risk and is governed by [The Apollo Terms of Service](https://www.apollographql.com/Apollo-Terms-of-Service.pdf).

PREVIEWS ARE PROVIDED "AS-IS," "WITH ALL FAULTS," AND "AS AVAILABLE," AND ARE EXCLUDED FROM ANY SERVICE LEVEL AGREEMENTS AND LIMITED WARRANTY. Previews may not be covered by customer support. Previews may be subject to reduced or different security, compliance and privacy commitments, as further explained in the Terms of Service, Privacy Policy and any additional notices provided with the Preview. We may change or discontinue Previews at any time without notice. We also may choose not to release a Preview into "General Availability."

## Getting Started

If you are reading this, you are part of a small number of folks we are showing this to early with the explicit purpose of working with you to solve the problems your graph consumers face. 

To try the pre-release version of Apollo Studio visit <https://engine.apollographql.com/studio>. You will need to login with your Apollo user account. If you have not created a graph and published your schema to Apollo before, you will need to do that before you can use Studio. Studio is currently only accessible by visiting this URL –– there are no links to it from within Graph Manager.

### Try the demo

Join our demo account, Acephei Corporation, by visiting <https://demo.apollo.dev> and creating an account. Then, [visit the `acephei` graph in Studio](https://engine.apollographql.com/studio/acephei?schemaTag=production) and try making your first query.

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

## Set up your graph

Studio is a client for querying your graph. To use it, you will need to provide a URL to the graph that Studio can send your constructued queries to.

### CORS considerations

The queries you construct will be sent directly from the web app in your browser at https://engine.apollographql.com to your server. Many servers have [CORS protections enabled](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) that prevent requests from unknown URLs from being responded to. If your server has these protections enabled, you will likely need to safe-list (whitelist) https://engine.apollographql.com in your CORS policy so that your requests from Studio are not rejected.

We are extremely interested in hearing your thoughts on CORS, so [please don't hold back from sharing if you have them](https://forms.gle/hhfA72JPC3fw43Wx5).

### Authentication

Studio does not explicity support any forms of authentication with endpoints. If you need to authenticate with your graph, you can do that by setting headers on your requests. The headers you set will be saved in your browser's local storage, one object entry per graph/variant pair.

We are extremely interested in hearing how you authenticate with your graph and what type of auth experience you would find ideal for a tool like Studio, so [please don't hold back from sharing them with us](https://forms.gle/hhfA72JPC3fw43Wx5).

## Motivations for building a hosted GraphQL client

We seek to solve a set of problems that we've heard from graph administrators:
1. A simple way to provision access to a query design tool to consumers of my graph without needing to run additional software on my production systems.
2. An expressive and pleasant tool that incorporates reference documentation with an operation authoring experience, so consumers of the graph can quickly formulate the right query for their problem. 
3. Provide tooling that can accommodate very large graphs, including nice ways to let certain consumers reason about subsets of the total graph while formulating their operations.
4. Provide stateful features like saved operations, collaboration, and incorporation of performance data and graph metadata into the experience. 

## We'd love to hear your feedback

We are very interested in seeing if the current experience is useful by itself and/or what other problems you want your graph exploring tools to provide.

_We are eager for your feedback, so please reach out._

1. Please [fill out our structured form](https://forms.gle/hhfA72JPC3fw43Wx5) after you have had a chance to use Studio for a few tasks if you are interested in sharing structured feedback.
2. For open-ended suggestions or bug reports, submit an Issue in this repository.
