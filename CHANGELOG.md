[comment]: <> (NOTE! Ensure all images are added via the \[label\]\(link\) syntax!)

## 2022-08-01 
| What's new | |
| :--------- | :-: |
| Announcing a new landing page for field insights! With this release, you can navigate from the Fields page or the schema browser to the field insights page, which provides a high-level overview of a field's usage, includng request count, latency, and error rate over time. Stay tuned for improvements and [share your feedback](https://forms.gle/P6pMJebLWrnyZMNaA) with us on the new experience! | ![Screen Shot of the Field Landing Page Feature](https://user-images.githubusercontent.com/6365997/185142459-b3d2e9e0-294f-49ed-adce-d9417fc54ef7.png)


## 2022-08-01 
| What's new | |
| :--------- | :-: |
| We have made some improvements to the Trace View for operations.  We now show an accurate gap in the timing between when the gateway / router sends a request and when the subgraph starts processing it. We also show a warning and adjust the timings if the subgraph reported times are out of range of the gateway reported times, which can happen if the subgraph is using a different clock.  As an added aesthetic improvement, subgraphs are now displayed with an icon in the trace instead of using the `subgraph:` prefix. | ![Screen Shot 2022-08-02 at 2 43 29 pm](https://user-images.githubusercontent.com/1110099/182294213-0f7ecc02-5d4b-47f3-8dd3-1b30091dfe47.png)


## 2022-07-28 Schema Reference Filtering 🥳
| What's new | |
| :--------- | :-: |
| You can now filter Schema Reference on subgraphs, directives, tags, arguments and return types - AND across multiple filter types, OR within a single filter type. | ![image](https://user-images.githubusercontent.com/86634858/182259987-5e816d88-f31b-4d5a-83fd-172a5bf69718.png) |
| When typing a word, see hints for existing filters. | ![image](https://user-images.githubusercontent.com/86634858/182258535-de22aae4-861c-460e-979e-029f760a5698.png) |
| Type a word and see the schema filtered with the text highlighted. If the word is prefixed or suffixed with a `.` then schema is only filtered for type or field respectively. | ![image](https://user-images.githubusercontent.com/86634858/182259081-0ae96b60-ac10-4a06-9ba7-478c8a54f248.png) |
| Easily share the filter query with your teammates | ![image](https://user-images.githubusercontent.com/86634858/182259174-3c7386f1-d859-4cd6-9451-75a95001c8c2.png)


## 2022-07-12
| What's new | |
| :--------- | :-: |
| You can now configure whether to pass `@tag` directives defined in your subgraphs through to consumers in Schema Reference and Explorer. These tags can help your API's consumers better understand your schema. To enable tags to pass through, update the build configuration for your variant. | ![image](https://user-images.githubusercontent.com/2107126/178511185-fba66590-6129-4dd3-a7a7-e09242204cc3.png)


## 2022-06-27
| What's new | |
| :--------- | :-: |
| We have made some changes to the Recent Checks Page UI. In the first column, instead of referring to the branch, the UI now displays the variant name. Also, branch now has its own column. | ![image](https://user-images.githubusercontent.com/86634858/176597150-afb10a4b-70e2-42f1-80aa-4dd85ed951db.png)


## 2022-06-24
| What's new | |
| :--------- | :-: |
| The Organization Memberships table now shows badges for members who have achieved Associate or Professional certifications through Apollo Odyssey! To learn how to get your team certified, visit [Apollo Odyssey](https://www.apollographql.com/tutorials/#certifications). | ![image](https://user-images.githubusercontent.com/24704789/175658830-f3adca0a-87de-4ea5-a70c-65888ea91bca.png) |
| You can now edit the default build configuration for your graph in the Settings page under the "This Graph" tab. New variants will use this track by default. On the other hand, existing variants will not be affected by updates to the default configuration. | ![image](https://user-images.githubusercontent.com/9286598/175666032-6fa67014-4372-4a8c-823e-70fddde46f08.png) 

## 2022-05-26
| What's new | 
| :--------- | 
| Contract build status webhooks now supported. For details, see [docs](https://www.apollographql.com/docs/studio/build-status-notification/).

## 2022-05-09
![image](https://user-images.githubusercontent.com/10705986/167469204-6f17e9d0-dec5-4690-90c8-46fe19a4a357.png)

| What's new | |
| :--------- | :-: |
| Since the release of public preview we have been working hard to improve the overall quality of life for Contracts. With GA you’ll find some fresh and nifty tools like the filter preview that allows you to view the “before” and “after” contract schema when you apply your filter configurations, support for tagging **additional schema elements** with Federation 2, the ability to view downstream contract launches via the Launches page, and many bug fixes! | ![image](https://user-images.githubusercontent.com/10705986/167470093-bdcc56e9-1fdb-4a5c-9c5f-012f483e015a.png) |
| Generate a filter preview so you can easily visualize the result of your filter configuration and tags to product your contract schema! | ![image](https://user-images.githubusercontent.com/10705986/167469691-4e1aa0e8-cb77-401c-95b5-6e77a44d482b.png) |
| Reason about contract launches triggered from your base variant via the Launches page! | ![image](https://user-images.githubusercontent.com/10705986/167470344-69181d26-7e5a-4114-a9d7-becee2dec4f6.png) 

## 2022-04-11
| What's new | |
| :--------- | :-: |
| Federation 2 is now in General Availability! | ![image](https://user-images.githubusercontent.com/6365997/162807130-d9f561e7-1df4-4b11-971a-97d329d085e9.png) |
| We've updated the new graph on-boarding experience to have a fresh new look, and now federation 2 is the default on-boarding experience. There is no impact to existing graphs with this update. | ![image](https://user-images.githubusercontent.com/6365997/162784055-ec577ae6-18ff-4719-b1e1-3602362198e2.png) |
| You are now prompted to select a default build pipeline track for your graph during on-boarding. All new variants will use this track by default. Individual variants can still override the graph-level default in the variant settings page. | ![image](https://user-images.githubusercontent.com/6365997/162784409-f42b48b9-a521-4f9f-a2e8-07e3380a723d.png) |

## 2022-04-08
| What's new | |
| :--------- | :-: |
| Access collections from other variants on your current graph using the select at the top of the collections panel. | ![image](https://user-images.githubusercontent.com/6856868/162516154-82834b65-1447-4109-900b-0def573d1f7b.png)

## 2022-04-07
| What's new | |
| :--------- | :-: |
| Directly save a copy of an operation to a collection from Operations View in Studio. | ![image](https://user-images.githubusercontent.com/86634858/162484861-810824de-41a8-488c-b09a-b5508939dbec.png)

## 2022-04-01
| What's new | |
| :--------- | :-: |
| Explorer's [Preflight Scripts](https://www.apollographql.com/docs/studio/explorer/connecting-authenticating/#preflight-scripts) can now open dialogs with markdown content using [`explorer.prompt`](https://www.apollographql.com/docs/studio/explorer/connecting-authenticating/#explorerprompt)! |![image](https://user-images.githubusercontent.com/743976/159772224-66b57c8e-4675-4a35-8b3d-c586a7626081.png)

## 2022-03-31
| What's new | |
| :--------- | :-: |
| [README](https://www.apollographql.com/blog/announcement/platform/create-a-readme-to-onboard-developers-to-the-graph/) for your graph/variants on Apollo Studio now has a table of contents that is generated based on headings in the README and makes the README easier to navigate. | ![image](https://user-images.githubusercontent.com/86634858/161134583-76928fb1-3c3d-443a-82ce-c9ca177a0518.png)| 

## 2022-03-30
| What's new | |
| :--------- | :-: |
| Explorer now has an option to “select all” fields for a given type. Recursively select all fields, or just add the scalar fields for a given type to your query. Find it next to `Fields` under the docs tab in Explorer. We hope this will saves y'all time next time you visit. | ![image](https://user-images.githubusercontent.com/86634858/160898153-d5cf13d2-70dd-4be5-9090-5adc1c743da2.png)| 

## 2022-03-24
[![Save and share Explorer operations with Operation Collections](https://user-images.githubusercontent.com/743976/159976790-a1e7f7f3-e9d4-4393-92bc-9856ad94da86.png)](https://www.apollographql.com/blog/announcement/platform/save-and-share-your-graphql-operations-in-apollo-explorer/?utm_campaign=2022-03-22_save-and-share-graphql-operations-blog&utm_medium=studio&utm_source=changelog)

## 2022-02-16
We've shipped some recent upgrades to Operation Insights in Apollo Studio. This update features three significant enhancements which make it easier to understand the usage and data flow of operations in your graph. [See the complete blogpost here.](https://www.apollographql.com/blog/announcement/platform/new-operation-insights-with-client-usage-and-federation-query-plans/)

| What's new | |
| :--- | ---- |
| First, we brought the operation signature front and center so that you can quickly understand the shape of fields being requested by the operation. The signature now appears as a side-panel that you can resize instead of hidden behind another tab. | ![image](https://wp.apollographql.com/wp-content/uploads/2022/03/operation-blog-1-1024x621.png) |
| In the same panel, we added the ability to view the federation query plan for an operation. The query plan lets you see how Apollo Gateway or Router is working under the hood, describing how data from your subgraphs is woven together to build a full query response. | ![image](https://www.apollographql.com/blog/static/0ad0380c2fe95a1267a5e0f752f60701/operation-blog-2.png) |
| Last but not least, we introduced a way to understand which clients are using an operation in a new Client Usage display. The most active clients are sorted to the top of the list based on the number of requests reported to Apollo Studio via usage reporting. | ![image](https://wp.apollographql.com/wp-content/uploads/2022/03/operation-blog-3-1024x621.png) |

## 2022-02-15
| What's new | |
| :--- | ---- |
| We have added support for using subgraphs in Sandbox! If the endpoint that you add to Sandbox points to a subgraph, a SUBGRAPH badge will appear. |![image](https://user-images.githubusercontent.com/14367451/154155677-b83f2f30-7291-41d0-b1d7-f083f5b8866d.png) |
| You can then run operations against your local subgraph schema, diff your changes against a registered subgraph schema and run checks to ensure that your changes do not affect composition or any running operations to the corresponding federated graph. Learn more [here](https://www.apollographql.com/docs/studio/explorer/sandbox/#subgraph-checks). | ![subgraph-sandbox-one-check-failed](https://user-images.githubusercontent.com/14367451/154148356-2fabcd82-1124-4a3b-bd70-5820e33f7895.jpg)|

## 2022-02-10
| What's new | |
| :-- | --- |
| You can now view **Query Plan Previews** for registered [Federation 2](https://www.apollographql.com/docs/federation/v2/) graphs in Apollo Studio Explorer. | ![image](https://user-images.githubusercontent.com/86634858/153515255-cc7276a8-3114-499d-9bae-740c6ed2ca7a.png) | 

## 2022-02-01
| What's new | |
| :-- | --- |
| The **Protected Variant**, **Public Variant**, and **Delete Variant** settings have been moved to a new "This Variant" tab of the Graph Settings page. | ![image](https://user-images.githubusercontent.com/5922187/153106696-1d15b528-9e23-4998-984e-502f0c5151e6.png) | 

## 2022-02-01
| What's new | |
| :-- | --- |
| Preflight scripts now expose the graphql POST request body and the crypto-js project. You can use the request body by referencing `explorer.request.body`, and crypto-js can be accessed with `explorer.CryptoJS` | ![image](https://user-images.githubusercontent.com/3953093/152077068-7d2c9dc8-4c13-464f-960d-1e8bc38c5991.png) | 

## 2022-01-25
| What's new | |
| :-- | --- |
| Operation names can now be excluded from schema checks. Sometimes an operation ID is not enough to prevent failures while checking schemas, and to ignore expected failures on certain operations, we've introduced the ability to exclude operations by name from the Checks Config page. | ![Excluded Operation Names](https://user-images.githubusercontent.com/639025/151235036-cc195e6a-480f-4cf0-a05f-ca44df4cec4d.gif) | 

## 2022-01-11

| What's new | |
| :--------- | :-: |
| We've updated the Graph Settings to be spread out across 5 tabs. We previously had just **General** and **Access**, and now we have **General**, **Permissions**, **API Keys**, **Reporting**, and **Variants**. | ![image](https://user-images.githubusercontent.com/5922187/149028499-df4239ab-163e-4d6b-bc25-17a46e8dd66b.png) |

## 2022-01-03 Happy new year! 🥳

| What's new | |
| :--------- | :-: |
| Preflight scripts are now available in Explorer! Preflight scripts are really useful for managing authentication before operations are run. As graph producers, you can automate authentication against your graph endpoints to reduce friction for your graph consumers as much as possible, increasing graph usage and adoption. Simply click to add the code snippets and get started with your preflight scripts today! For details, see [docs](https://www.apollographql.com/docs/studio/explorer/connecting-authenticating/#preflight-scripts).| ![image](https://user-images.githubusercontent.com/86634858/147967983-7573674b-cdb8-4d37-8879-375cf771c54a.png) |
