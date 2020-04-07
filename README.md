# Preview: Apollo Studio

Welcome to Apollo Studio, a browser-based tool for exploring GraphQL schemas, composing queries, and testing responses.

## Before you start: IMPORTANT DISCLAIMER

The documentation here is currently only a preview of pre-release software. You may use it at will, but this evaluation product is not yet fully supported or considered generally available. While we will try to avoid breaking changes once a feature is in use, until the features discussed herein are taken out of preview we could make breaking changes. Please be aware of the heightened risk of using preview software.

Use of anything described in this preview docs (current as of March 2020) is done at your own risk and is governed by [The Apollo Terms of Service](https://www.apollographql.com/Apollo-Terms-of-Service.pdf).

PREVIEWS ARE PROVIDED "AS-IS," "WITH ALL FAULTS," AND "AS AVAILABLE," AND ARE EXCLUDED FROM ANY SERVICE LEVEL AGREEMENTS AND LIMITED WARRANTY. Previews may not be covered by customer support. Previews may be subject to reduced or different security, compliance and privacy commitments, as further explained in the Terms of Service, Privacy Policy and any additional notices provided with the Preview. We may change or discontinue Previews at any time without notice. We also may choose not to release a Preview into "General Availability."

## Getting Started

If you are reading this, you are part of a small number of folks we are showing this "too early" with the explicit purpose of working you to solve the problems your graph consumers face. 

To try the pre-release version of Apollo Studio visit <https://engine.apollographql.com/studio>. You will need to login with your Apollo user account.

## Motivations for building a hosted GraphQL client

We seek to solve a set of problems that we've heard from graph administrators:
1. A simple way to provision access to a query design tool to consumers of my graph without needing to run additional software on my production systems.
2. An expressive and pleasant tool that incorporates reference documentation with an operation authoring experience, so consumers of the graph can quickly formulate the right query for their problem. 
3. Provide tooling that can accommodate very large graphs, including nice ways to let certain consumers reason about subsets of the total graph while formulating their operations.
4. Provide stateful features like saved operations, collaboration, and incorporation of performance data and graph metadata into the experience. 

## We'd love to hear your feedback

We are interested in seeing if the current experience is useful by itself and/or what other problems you want your graph exploring tools to provide.

_We are eager for your feedback, so please reach out._

1. Please [fill out our structured form](https://forms.gle/hhfA72JPC3fw43Wx5) after you have had a chance to use Studio for a few tasks if you are interested in sharing structured feedback.
2. For open-ended suggestions or bug reports, submit an Issue in this repository.
