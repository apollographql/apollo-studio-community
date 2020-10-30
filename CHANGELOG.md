## 2020-10-30

- You can now mock data from your operations in the Explorer with the "Mock responses" option in the Explorer's settings. This will return naively mocked data rather than sending requests to your endpoint. This is useful if you need to generate test data or if you want to try out queries without having and endpoint to send to.

![image](https://user-images.githubusercontent.com/5922187/97745141-a11eac00-1aa5-11eb-9a47-c9f8a2037ce2.png)


## 2020-10-29

- You can now inline and extract variables from your operations in the Explorer by right-clicking in the Explorer's editor and selecting the "Inline" and "Extract" options from the context menu there:
![Screen Recording 2020-10-29 at 03 32 29 PM](https://user-images.githubusercontent.com/5922187/97639919-cc998c00-19fc-11eb-8c17-754e3494c566.gif)


## 2020-10-28

- You can now display query response data in both JSON and in a table view using toggles at the top of the response pane:
![table-view-gif](https://user-images.githubusercontent.com/8431868/97485038-f5078480-192f-11eb-8dcd-adc5cac4ad9d.gif)


## 2020-10-26

- We've introduced a new experience in Studio that's optimized for bringing Studio's tools to you during local development. We have [written some preview docs](https://github.com/apollographql/apollo-studio-community/blob/main/preview-docs/DevGraphs.md) and the experience are accessible at studio.apollographql.com/dev. We willl be launching this experience more formally in November.

## 2020-10-23

- Building off of recent updates to schema checks, you can now rerun checks from inside Studio. When you rerun a check, the latest check configuration is applied. The new check uses an updated time window for operations — in addition, any changes made to excluded / included clients, checked variants, and any operations already marked safe / ignored are incorporated when rerunning. If you are using the Github Action to trigger checks, a rerun of the check also updates the status of the check in Github.
  ![Rerun Checks Screenshot](https://user-images.githubusercontent.com/1831709/97130183-c30deb00-1794-11eb-8b03-a79818ac78db.png)

## 2020-10-22

- You can now see field latency performance stats inline in the Explorer as you write queries by turning this on in the Explorer's settings pane.
![ElTA31CUwAAvPuK](https://user-images.githubusercontent.com/5922187/97661451-9b877e80-1a31-11eb-9323-b2a31f33630e.jpeg)

## 2020-10-19

- Timestamps: additional timezone information is now included in many places where it was not before. In addition, hovering over a timestamp in the app will reveal both local time and UTC / [ISO8601](https://en.wikipedia.org/wiki/ISO_8601) time with "copy to clipboard" capability for sharing or syncing with other tools.
  ![Timestamps](https://user-images.githubusercontent.com/1831709/96394656-4916b880-120e-11eb-8054-dcb94dda8249.gif)

## 2020-10-06

- Schema Reference will now detect comments containing text matching the pattern of "TypeName.fieldName" and turn those into navigable links
  ![Screen Recording 2020-10-06 at 09 56 11 PM](https://user-images.githubusercontent.com/743976/95278712-cdd10200-081e-11eb-8afd-e55d1f7afe86.gif)

## 2020-10-02

- The [Datadog integration](https://www.apollographql.com/docs/studio/datadog-integration/) now sends metrics that start with `apollo.operations` instead of `apollo.engine.operations` and tags them with `graph:` rather than `service:`, to match our current naming scheme. This change affects newly configured Datadog integrations only. Graphs currently sending metrics to Datadog continue to use the old names; you can change to use the new names by clicking "Transition to modern mode" on your graph's Integrations page.

## 2020-09-24

- Federation: you can now see composition errors on implementing services published to your variant. You can see these composition errors, if present, by clicking on the "services" tab of the variant in question.

## 2020-09-23

- Creating new graphs with the Apollo Server integration is now simpler. Running your server with the `APOLLO_KEY` and
  `APOLLO_SCHEMA_REPORTING` environment variables will now automatically report metrics and schema to Studio, with no configuration in `ApolloServer` itself necessary.

## 2020-09-16

- Studio welcomes a new and improved check details page, featuring...
  - Request usage graphs of affected operations
  - Differentiation between operations that are broken vs. changing behavior
  - One-click views of operation bodies, change details, and check configuration
  - A brand new visual feel
  - ... and more! We hope you enjoy

## 2020-09-08

- Explorer now supports subscriptions, you can set a separate subscription URL in the variant settings

## 2020-09-01

- When setting the endpoint url to be used in explorer, you now have the option of configuring it to include cookies for all users.
- The history and checks pages in Studio now link to the commit you were on when you ran `service:push`/`service:check` for GitHub and Bitbucket users.

## 2020-08-31

- We'll make a best guess at reconstructing any unrecognized directives, so schemas that don't include definitions for directives should no longer crash the Schema or Explorer pages.
- Improved experience for path selection in Explorer page's search
- You can now favorite graph variants, which will pin the variant to the top of the graphs list page.
  Favorited variants are saved to your individual account, so you'll be able to see them when logging in on a new device.
  To favorite a graph, hover over your desired variant on the graph list page, and click the star icon on the left side:
  ![favorite-graphs](https://user-images.githubusercontent.com/8431868/91739780-64573700-eb80-11ea-8073-4d66d0f0c443.gif)

## 2020-08-28

- You can now use [graphql-lodash](https://github.com/APIs-guru/graphql-lodash) directives in studio to apply transformations to your results.
- "Cancel" button now added to Upload Schema modal in Schema tab.

## 2020-08-26

- User roles and permissions are now available in Studio by request –– email support@apollographql.com if you're interested. Take a look at our [official documentation](https://www.apollographql.com/docs/studio/org/members) for the feature for a detailed breakdown on what permissions each role has.

## 2020-08-21

- 🐛 Bug fix: SSO users should see their name and avatar in Studio now (provided they've set up the attribute mapping via PingOne)

## 2020-08-20

- 🐛 Bug fix: schema checks no longer skip anonymous operations

## 2020-08-18

- "Type Browser" has been renamed to "Reference"
- Directives are now visible in "Reference" ![image](https://user-images.githubusercontent.com/743976/90544698-82bb3c80-e155-11ea-8b30-bba588564705.png)
- Types and Fields that appear in Changelog now link to their place in Reference
- Reference is now searchable via `⌘ + K` (`Ctrl + K` for PC) ![image](https://user-images.githubusercontent.com/743976/90545321-78e60900-e156-11ea-819d-df7374e6c494.png)

## 2020-08-05

New in general:

- You can now do a _one-time_ schema upload to Studio by introspecting a URL or pasting a schema to get started **much** more quickly.
- You can now do a one-time upload of your schema at any point by clicking the "Upload Schema" button on the Schema page.

![Screen Recording 2020-08-05 at 10 32 09 AM](https://user-images.githubusercontent.com/5922187/89444869-3c9ebb80-d707-11ea-9afe-2ad911843933.gif)

| New in the Explorer:                                                           |                                                                                                                                                    |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| You can copy an operation to CURL from the Explorer's "meatball" context menu. | ![Screen Recording 2020-08-03 at 12 22 39 PM](https://user-images.githubusercontent.com/5922187/89219182-2ddbcb80-d584-11ea-9e21-4950c86306a8.gif) |

## 2020-07-29 –– ✨New Page: Schema ✨

We have released a new home page for your graph in Studio that contain's your graph's docs, changelog, and SDL.

|                                                                                                                                                            |                                                 New information about your schema:                                                 |                                                                                                                                    |
| :--------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------: |
|                                                Auto-generated documentation for type and field references.                                                 |                                                Changelog –– what changed and when.                                                 |                                                             Full SDL.                                                              |
| <img width="1284" alt="Screenshot of Types page" src="https://user-images.githubusercontent.com/743976/88816756-bcb6a580-d18a-11ea-9188-7c51ecfe0362.png"> | <img width="1284" alt="" src="https://user-images.githubusercontent.com/743976/88817042-11f2b700-d18b-11ea-903c-e0e0cb975439.png"> | <img width="1284" alt="" src="https://user-images.githubusercontent.com/743976/88818141-5c286800-d18c-11ea-83a6-e69106ec6520.png"> |

## 2020-07-22 –– ✨New Page: Checks ✨

We have released the new Checks page for our schema [checks feature](https://www.apollographql.com/docs/studio/schema-checks/). You can now **see recent checks** that have been run against and **configure your check parameters** from directly within the UI.

<img width="1284" alt="Screen Shot 2020-07-27 at 6 18 29 PM" src="https://user-images.githubusercontent.com/5922187/88608003-96cbbc80-d035-11ea-931c-1fc3a1901ea1.png">

## 2020-07-21

| New in the Explorer:                                                                                                                                               |                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| You can now see inlined response hints in the Explorer. As you add fields to your query or change variables, the Explorer will make partial requests for new data. | ![Screen Recording 2020-07-27 at 06 15 22 PM](https://user-images.githubusercontent.com/5922187/88607871-2de44480-d035-11ea-81d6-2e7094ae23fb.gif) |

## 2020-07-14

| New in Integrations:                                                                                                                                    |                                                                                                                                                    |
| :------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| By popular request, you can now use the Datadog-forwarder with Datadog instances in the EU. Head to your graph's Integrations page to configure this 🌍 | ![Screen Recording 2020-08-03 at 01 17 38 PM](https://user-images.githubusercontent.com/5922187/89223506-c1fd6100-d58b-11ea-8e51-0f047d3757ea.gif) |

| New in the Explorer:                                                                                              |                                                                                                                                                    |
| :---------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| You can now configure requests to authenticate with your domain through cookies in the Explorer's settings tab 🍪 | ![Screen Recording 2020-08-03 at 01 21 30 PM](https://user-images.githubusercontent.com/5922187/89223825-536cd300-d58c-11ea-82d5-052c62c66044.gif) |

## 2020-07-07

| New in the Explorer:                                                                                                  |                                                                                                                                                    |
| :-------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| You can now manage operations individually using a "meatball" context menu, even when other operations are invalid 🍝 | ![Screen Recording 2020-08-03 at 01 23 27 PM](https://user-images.githubusercontent.com/5922187/89223976-9038ca00-d58c-11ea-8058-a225faf6a2b6.gif) |
| You can now generate variables for your query using autocomplete in the editor.                                       | ![Screen Recording 2020-08-03 at 01 24 22 PM](https://user-images.githubusercontent.com/5922187/89224079-b9f1f100-d58c-11ea-8666-412be8f8bf83.gif) |

## 2020-06-30 –– ✨ New Page: Explorer ✨

We have released the Explorer, available as a top-level page for graphs. The Explorer is a full-featured query building IDE that connects to the registry and can be configured uniquely for each of your variants.

Full details on the release in our announcement post: [Introducing the Apollo Explorer](https://www.apollographql.com/blog/introducing-the-apollo-explorer/).

![Building a query using the Explorer's query builder.](https://user-images.githubusercontent.com/5922187/88606849-954cc500-d032-11ea-8fac-218e391f134d.gif)

## 2020-06-29

We have formally [renamed the product from Graph Manager to Studio](https://www.apollographql.com/blog/graph-manager-is-now-studio/), moved our URL from engine.apollographql.com to studio.apollographql.com, and have updated our website, docs, and in-product references to reflect the change.
