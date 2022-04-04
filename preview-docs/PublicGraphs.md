---
### 🎉 Update! [First phase](https://www.apollographql.com/docs/studio/org/graphs/#public-variants) of this proposal is available now!
---

## ⚠️ BEFORE YOU START: IMPORTANT DISCLAIMER

>The documentation here is all speculative, future looking and subject to change. It should not be taken as any sort of product commitment and only being shared to gather early feedback on what is on our minds. 

# Making graph the default for any developer looking to integrate with your organization’s data

Per feedback, we are doing work towards public graphs and thinking about how that might potentially lead to a graph developer portal in the future. We are looking for feedback on whether our thinking will fit the needs of your organization.

If you're reading this, please fill out our feedback form - _takes less than 10 minutes_! We are grateful for your feedback and read every response that comes in: [Feedback Survey](https://www.surveymonkey.com/r/apollo-pggdp-feedback). 

## Why a graph developer portal?

Our long term mission has been to empower organizations with a developer toolkit that enables them to move fast allowing them to keep up with the competition and meet their customers’ expectations. We do this by advocating for a unified data graph and providing the means to do so, so that developers can get universal access to fragmented and disparate data and services, without needing to understand the underlying architecture and the role of each service. 

Today, we see enterprises and organizations adopting graph across different verticals for developers within the organization. We want to go beyond that by giving you the ability to create a graph developer portal, where you can easily expose all the necessary graph information to any developer, even external to the organization, who will need to use your graph. Developers will be able to understand what that graph schema looks like, try it out with mock data, explore how-to-guides, tutorials, examples and so much more all on your own custom branded graph developer portal. 

## Proposed Phases

### Phase 1: Introduce public graphs

On Apollo Studio’s graph settings page, a specific variant can be declared as “public”. You can preview the public view of that variant. The URL will be shareable and the variant will then be available for any consumer to access without needing to be a part of the Apollo Studio organization. Public graphs will additionally come with the following two capabilities:

1. **Support for adding a graph home page:** Add a README for this variant (and any other “non-public” variant) where producers of the graph can specify how to get started with using the graph variant. Default content for README will be provided, which can be easily edited. In the beginning, README will support markdown only.
2. **Embeddable explorer experience for webpages:** Embed Apollo Studio’s explorer on any web page. A public graph can then be exposed through the embedded explorer on that web page. A visitor to that website will be able to browse the schema of that graph and execute queries. The schema of the public graph will be available for any visitor to explore, but depending on the security mechanism on the graph’s endpoint, user will need to enter the appropriate authentication credentials to receive a successful response for their queries.

_Note_: We are also considering the future possibility of adding the ability to embed variants that are not “public” on webpages. If this is of interest to you, please provide feedback here: [Feedback Survey](https://www.surveymonkey.com/r/apollo-pggdp-feedback).

### Phase N: Potential future offerings

Following are some other things we are considering as we continue to evolve our public graph offering. We would love to get your feedback on whether these are solutions that will be useful for your organization’s use cases and how they might fit in your graph strategy. If this is of interest, please fill out this feedback form: [Feedback Survey](https://www.surveymonkey.com/r/apollo-pggdp-feedback). 

1. **Central repository for the most popular and highest ranked public graphs:** Once organizations start creating and publishing public graphs, and most importantly, developers start taking advantage of this new, seamless way of consuming their data - we will add an ability for the developers to star and rate the public graphs they use. We can then create a single view for top, highest rated public graphs - incentivizing more graph usage and better graph production, both at the same time! Reap the benefits of all that network effect!
2. **Customize your public graphs with custom domain and branding:** What is better than public graphs for consumers external to your organization? Public graphs that have your own branding with colors, logo, text formatting and custom domain. This will ensure that consumers have the same sense of familiarity as they get when interacting with other products offered by your organization. Customize it to your heart’s content!
3. **Introduction of graph developer portal:** Offer a full service developer portal for your graph consumers with additional documentation, articles, tutorials, how-to-guides, customizable branding and improved SEO. With try outs using mocked data, enhanced search and ability to give feedback on schemas, comment in-line and ask questions, integration with Slack, Jira or PagerDuty (!!) graph developer portal will become the go-to, default landing page for every developer looking to integrate and interact with your organization’s data - the interface between your organization and the developer. 
4. **Publish different public graphs for different audiences:** Maybe you are thinking, how can I expose different public graphs to different consumers - maybe a partner needs a different set of information than a vendor. However, at the same time if the graphs can be centrally located then based on their profile, a consumer can discover and get access to the appropriate public graph.

#### Working assumptions

1. When a specific graph variant is marked as “public”, anyone with the link to the public variant can access its schema. However, the endpoint to query data could require authentication depending on the graph endpoint configuration.
