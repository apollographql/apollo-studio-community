---
### 🎉 Update! We have released [Operation Collections](https://www.apollographql.com/blog/announcement/platform/save-and-share-your-graphql-operations-in-apollo-explorer/) in Apollo Explorer that solve the first two use cases mentioned below.
---

# Operations Catalog

## ⚠️ BEFORE YOU START: IMPORTANT DISCLAIMER

>The documentation here is all speculative, future looking, and subject to change. It should not be taken as any sort of product commitment and is only being shared here to gather early feedback on what is on our minds. 

# Why an operations catalog?

Our long term mission has been to empower organizations with a developer toolkit that enables them to move fast, allowing them to keep up with the competition and meet their customers’ expectations. We do this by advocating for a unified data graph and providing the means to do so, so that developers can get universal access to fragmented and disparate data and services, without needing to understand the underlying architecture and the role of each service. 

As part of this developer toolkit, we provide Apollo Studio Explorer, where developers can create, run and manage operations executed against the graph. _A critical piece of this experience is the ability to save, organize and share operations, which enables cross team collaboration._

Following are some of the use cases that we are considering for solutioning operations catalog in Apollo Studio. We would love to get your feedback on whether these will be useful for your organization and how they might fit in graph exploration, collaboration and consumption experience. If you're reading this, **please fill out our feedback form! We are grateful for your feedback and read every response that comes in: [Feedback Survey](https://www.surveymonkey.com/r/ApolloOperationsCatalog).** 

# Proposed use cases

1. **Save and organize operations as collections:** A collection is a set of operations. Developers will be able to save the operations that they write in Studio for later use and easy access and organize them as collections. They can create, update, delete and read the collections of operations. Collections will have description that can be used to explain their purpose. 
2. **Share with other members of the team:** Developers can share the collection/s of operations with other members of the team that have at least read access to the graph. For public graphs, sharing can be possible outside of the members of the Studio Org. Sharing of collections is made possible by:
    1. Share the collection directly with other members of the org that have access to Studio: The shared collection will be visible in the operations catalog of each member that it is shared with. Any graph or org admin can edit the collection to make changes to the collection or any of the operation. 
    2. Share the collection with a link: A unique link for that collection will be generated that can be distributed for sharing. Any permitted user who has access to the link will be able to view the collections. For public graphs, link sharing can be used for sharing a collection outside of the Studio org. The link is always up to date with the changes made to the collection.
    3. Share the collection in variant README: Using graph shortcodes, operation collections or saved operations can be embedded for use in variant README. The collections and saved operations are always kept up to date with any changes made.  
3. **Reference and download:** A GraphQL document that represents the collection can also be easily exported for distribution. A particular operation or collection of operations can also be used in markdown for inline rendering. 
4. **Production data access:** Certain operations or collections can be marked as “secure”, meaning that they are good for pulling production data, allowing non-technical users who want to query graph data easy access to parameterize those operations. A specific list of users or a user with a secret token can query data using secure operations/collections.
5. **Schema checks:** An operation or a collection of operations can be used as part of an integration test suite or to ensure that a given schema state is OK to deploy by automatically validating whether the given schema state can fulfill that collection of operations.
6. **Secure gateway:** An operation or a collection of operations can be used to block the gateway so that only certain types and shapes of operations can make it through.

> 🙏 **We would love to hear what you think. Please fill out our feedback form! We are grateful for your feedback and read every response that comes in: [Feedback Survey](https://www.surveymonkey.com/r/ApolloOperationsCatalog).** 
