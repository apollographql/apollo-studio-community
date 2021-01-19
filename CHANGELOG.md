## 2021-01-19
| What's new |    |
| :--------- | -- |
| We've enhanced the [user roles system](https://apollographql.com/docs/studio/org/members/) available to Enterprise customers! <ul><li>Users can be granted a **role on a specific graph** with more permissions than their organization-level role.</li><li>A graph can be **hidden** from non-Organization Admin users that have not been explicitly granted a role on that graph.</li><li>Each [**graph API key**](https://apollographql.com/docs/studio/api-keys/#setting-permissions) now has a role (Graph Admin, Contributor, Observer, or Consumer) which limits their permissions. (Existing graph API keys retain their existing permissions.)</li><li>A new **Graph Admin** role has complete control over graphs (including managing graph-specific roles) but no organization-level administrative permissions. Existing Contributors have been changed to this role.</li><li>The Contributor role now is very similar to the Observer role, plus the ability to push new versions of the graph's schema. You can now mark individual variants as **protected**; you need to be a **Graph Admin** to push schemas to these variants.</li><ul> | <img width="600" src="https://user-images.githubusercontent.com/16724/105080845-406c9300-5a46-11eb-8c22-94122e4a5a93.png"> |

## 2021-01-12
| What's new |    |
| :--------- | -- |
| You can now hard delete organizations on your organization's **Settings** page. Previously, you needed to contact Apollo support to do this. When you hard delete an organization, the following things will happen:<ul><li>If your organization is on a Team plan or Team trial, your subscription willl be immediately canceled. We can't issue refunds for this unfortunately.</li><li>All users memberships in your organization will be removed. Users of your organization will maintain their user accounts, but they will no longer be members of your org.</li><li>All graphs in your organization will be hard deleted. To keep your data secure, their graph IDs will be tombstoned and you will not be able to create new graphs with the same ID in the future.</li></ul>| <img width="600" src="https://user-images.githubusercontent.com/5922187/104364461-76040000-54cb-11eb-929f-7bf935128f39.png"> |

## 2021-01-07
| What's new |    |
| :--------- | -- |
| We have transitioned our underlying support system at Apollo from **Intercom** to **Zendesk**. If you need to get in touch with us, please file a ticket with our new **Contact Support** form (available in the top right corner of the Studio UI). | <img width="400" alt="Screen Shot 2021-01-07 at 10 01 45 AM" src="https://user-images.githubusercontent.com/5922187/103927585-70737800-50cf-11eb-9cae-8ba0003be642.png"> |

## 2021-01-05
| What's new |    |
| :--------- | -- |
| We have updated the visual presentation of our Graphs list. Each graph is now represented as a card, we've added a settings link directly from the graph list, and we now represent links with blue to make them look more clickable. | <img width="960" alt="Screen Shot 2021-01-05 at 9 32 14 AM" src="https://user-images.githubusercontent.com/5922187/103678896-fdd09400-4f38-11eb-92f3-6da406b14ee4.png"> |

## 2020-12-10
| What's new |    |
| :--------- | -- |
| New layout for metrics filtering tools! Instead of an overlapping sidebar, we've embedded the controls for filtering by time range, clients, and operations directly into the page header. Now you can simply adjust the knobs without having to context-switch out of your current view. | ![Updated Filter UX](https://user-images.githubusercontent.com/1831709/101563762-f7282d00-3a1d-11eb-9a89-012280710c52.gif) |

## 2020-11-16

| What's new in the Explorer |    |
| :------------------------- | -- |
| Don’t send unused variables over the wire                                                        | ![Screen Recording 2020-11-16 at 04 00 42 PM](https://user-images.githubusercontent.com/5922187/99323038-246e2a80-2826-11eb-9e86-01e8c6cd9b47.gif) |
| Visual Query Plans (rendered using mermaid)                                                      | ![image](https://user-images.githubusercontent.com/5922187/99334771-b893be00-2835-11eb-89ef-593a061060ee.png)                                      |
| Table Mode column sorting                                                                        | ![Screen Recording 2020-11-16 at 06 03 23 PM](https://user-images.githubusercontent.com/5922187/99336192-20e29f80-2836-11eb-8e2a-7c650834bc64.gif) |
| Download arrays from Table Mode to CSVs                                                          | ![image](https://user-images.githubusercontent.com/5922187/99335997-12948380-2836-11eb-8a34-8ae4c8ab2442.png)                                      |
| Choose the percentile (p50, p90, p99, etc) that you want your field latency hints displayed from | ![image](https://user-images.githubusercontent.com/5922187/99337060-6ef7a300-2836-11eb-81eb-32f0ecfdf7e3.png)                                      |

## 2020-11-13
| What's new |    |
| :--------- | -- |
| You can now inline and extract fragments from your operations in the Explorer by using the right-click context menu. | ![Screen Recording 2020-11-11 at 02 49 40 PM](https://user-images.githubusercontent.com/5922187/99136885-673cc200-25dc-11eb-9237-4de29f6af31f.gif) |

## 2020-11-06
| What's new |    |
| :--------- | -- |
| You can now see and browse traces from your responses in the Explorer if you're using Apollo Server 2.18+ and add the `ApolloServerPluginInlineTrace` plugin | ![Screen Recording 2020-11-06 at 02 43 57 PM](https://user-images.githubusercontent.com/5922187/98421915-5241bb00-203f-11eb-8dd2-37132fc70c24.gif) |
| Better handle un-executable operation. Shows information tooltips and italicizes the constant identifiers for un-executable operations that we're added in [Apollo Server 2.19.0](https://github.com/apollographql/apollo-server/blob/main/CHANGELOG.md#v2190) | ![Screen Shot 2020-11-06 at 5 35 09 PM](https://user-images.githubusercontent.com/14363000/98426684-0a2e9280-2057-11eb-985f-73299c5ebed8.png) |

## 2020-11-05
| What's new |    |
| :--------- | -- |
| Small enhancement to Operations / Errors UX: links from errors to traces are now able to be opened in a new tab using CMD+click / CTRL+click. | ![image](https://user-images.githubusercontent.com/1831709/98312158-37fae380-2025-11eb-8d0c-4768c47cd1ae.png) |

## 2020-10-31
| What's new |    |
| :--------- | -- |
| Happy Halloween! Here's our present to you (no trick, just treat). In graphs using managed federation, you can now see query plans inlined next to your operations in the Explorer as you write them. The Explorer calculates query plans on the fly with your implementing services as input. | ![Screen Recording 2020-10-30 at 04 43 32 PM](https://user-images.githubusercontent.com/5922187/97766759-1bb2f000-1ad5-11eb-9c9b-44322217fcdd.gif) |

## 2020-10-30
| What's new |    |
| :--------- | -- |
| You can now mock data from your operations in the Explorer with the "Mock responses" option in the Explorer's settings. This will return naively mocked data rather than sending requests to your endpoint. This is useful if you need to generate test data or if you want to try out queries without having and endpoint to send to. | ![image](https://user-images.githubusercontent.com/5922187/97745141-a11eac00-1aa5-11eb-9a47-c9f8a2037ce2.png) |

## 2020-10-29
| What's new |    |
| :--------- | -- |
| You can now inline and extract variables from your operations in the Explorer by right-clicking in the Explorer's editor and selecting the "Inline" and "Extract" options from the context menu there. | ![Screen Recording 2020-10-29 at 03 32 29 PM](https://user-images.githubusercontent.com/5922187/97639919-cc998c00-19fc-11eb-8c17-754e3494c566.gif) |  

## 2020-10-28
| What's new |    |
| :--------- | -- |
| You can now display query response data in both JSON and in a table view using toggles at the top of the response pane in the Explorer. | ![table-view-gif](https://user-images.githubusercontent.com/8431868/97485038-f5078480-192f-11eb-8dcd-adc5cac4ad9d.gif) |

## 2020-10-26
| What's new |
| :--------- |
| We've introduced a new experience in Studio that's optimized for bringing Studio's tools to you during local development. We have [written some preview docs](https://github.com/apollographql/apollo-studio-community/blob/main/preview-docs/DevGraphs.md) and the experience are accessible at studio.apollographql.com/dev. We willl be launching this experience more formally in November. |

## 2020-10-23
| What's new |    |
| :--------- | -- |
| Building off of recent updates to schema checks, you can now rerun checks from inside Studio. When you rerun a check, the latest check configuration is applied. The new check uses an updated time window for operations — in addition, any changes made to excluded / included clients, checked variants, and any operations already marked safe / ignored are incorporated when rerunning. If you are using the Github Action to trigger checks, a rerun of the check also updates the status of the check in Github. | ![Rerun Checks Screenshot](https://user-images.githubusercontent.com/1831709/97130183-c30deb00-1794-11eb-8b03-a79818ac78db.png) |

## 2020-10-22
| What's new |    |
| :--------- | -- |
| You can now see field latency performance stats inline in the Explorer as you write queries by turning this on in the Explorer's settings pane. | ![ElTA31CUwAAvPuK](https://user-images.githubusercontent.com/5922187/97661451-9b877e80-1a31-11eb-9323-b2a31f33630e.jpeg) |

## 2020-10-19
| What's new |    |
| :--------- | -- |
| Timestamps: additional timezone information is now included in many places where it was not before. In addition, hovering over a timestamp in the app will reveal both local time and UTC / [ISO8601](https://en.wikipedia.org/wiki/ISO_8601) time with "copy to clipboard" capability for sharing or syncing with other tools. | ![Timestamps](https://user-images.githubusercontent.com/1831709/96394656-4916b880-120e-11eb-8054-dcb94dda8249.gif) |

## 2020-10-06
| What's new |    |
| :--------- | -- |
| Schema Reference will now detect comments containing text matching the pattern of "TypeName.fieldName" and turn those into navigable links. | ![Screen Recording 2020-10-06 at 09 56 11 PM](https://user-images.githubusercontent.com/743976/95278712-cdd10200-081e-11eb-8afd-e55d1f7afe86.gif) |

## 2020-10-02
| What's new |
| :--------- |
| The [Datadog integration](https://www.apollographql.com/docs/studio/datadog-integration/) now sends metrics that start with `apollo.operations` instead of `apollo.engine.operations` and tags them with `graph:` rather than `service:`, to match our current naming scheme. This change affects newly configured Datadog integrations only. Graphs currently sending metrics to Datadog continue to use the old names; you can change to use the new names by clicking "Transition to modern mode" on your graph's Integrations page. |

## 2020-09-24
| What's new |
| :--------- |
| Federation: you can now see composition errors on implementing services published to your variant. You can see these composition errors, if present, by clicking on the "services" tab of the variant in question. |

## 2020-09-23
| What's new |
| :--------- |
| Creating new graphs with the Apollo Server integration is now simpler. Running your server with the `APOLLO_KEY` and
  `APOLLO_SCHEMA_REPORTING` environment variables will now automatically report metrics and schema to Studio, with no configuration in `ApolloServer` itself necessary. |

## 2020-09-16
- Studio welcomes a new and improved check details page, featuring...
  - Request usage graphs of affected operations
  - Differentiation between operations that are broken vs. changing behavior
  - One-click views of operation bodies, change details, and check configuration
  - A brand new visual feel
  - ... and more! We hope you enjoy

## 2020-09-08
| What's new |
| :--------- |
| Explorer now supports subscriptions, you can set a separate subscription URL in the variant settings. |

## 2020-09-01
| What's new |
| :--------- |
| When setting the endpoint url to be used in Explorer, you now have the option of configuring it to include cookies for all users. |
| The history and checks pages in Studio now link to the commit you were on when you ran `service:push`/`service:check` for GitHub and Bitbucket users.|

## 2020-08-31
| What's new |   |
| :--------- | - |
| We'll make a best guess at reconstructing any unrecognized directives, so schemas that don't include definitions for directives should no longer crash the Schema or Explorer pages. | |
| Improved experience for path selection in Explorer page's search | |
| You can now favorite graph variants, which will pin the variant to the top of the graphs list page. Favorited variants are saved to your individual account, so you'll be able to see them when logging in on a new device. To favorite a graph, hover over your desired variant on the graph list page, and click the star icon on the left side. | ![favorite-graphs](https://user-images.githubusercontent.com/8431868/91739780-64573700-eb80-11ea-8073-4d66d0f0c443.gif) |

## 2020-08-28
| What's new |
| :--------- |
| You can now use [graphql-lodash](https://github.com/APIs-guru/graphql-lodash) directives in studio to apply transformations to your results. |
| "Cancel" button now added to Upload Schema modal in Schema tab. |

## 2020-08-26
| What's new |
| :--------- |
| User roles and permissions are now available in Studio by request –– email support@apollographql.com if you're interested. Take a look at our [official documentation](https://www.apollographql.com/docs/studio/org/members) for the feature for a detailed breakdown on what permissions each role has. |

## 2020-08-21
| 🐛 Bug fix |
| :--------- |
| SSO users should see their name and avatar in Studio now (provided they've set up the attribute mapping via PingOne) |

## 2020-08-20
| 🐛 Bug fix |
| :--------- |
| Schema Checks no longer skip anonymous operations |

## 2020-08-18
| What's new |    |
| :--------- | -- |
| "Type Browser" has been renamed to "Reference" |
| Directives are now visible in "Reference" | ![image](https://user-images.githubusercontent.com/743976/90544698-82bb3c80-e155-11ea-8b30-bba588564705.png) |
| Types and Fields that appear in Changelog now link to their place in Reference | |
| Reference is now searchable via `⌘ + K` (`Ctrl + K` for PC) | ![image](https://user-images.githubusercontent.com/743976/90545321-78e60900-e156-11ea-819d-df7374e6c494.png) |

## 2020-08-05
| New in general |    |
| :------------- | -- |
| You can now do a _one-time_ schema upload to Studio by introspecting a URL or pasting a schema to get started **much** more quickly. | |
| You can now do a one-time upload of your schema at any point by clicking the "Upload Schema" button on the Schema page. | ![Screen Recording 2020-08-05 at 10 32 09 AM](https://user-images.githubusercontent.com/5922187/89444869-3c9ebb80-d707-11ea-9afe-2ad911843933.gif) |


| New in the Explorer: |     |
| -------------------- | --- |
| You can copy an operation to CURL from the Explorer's "meatball" context menu. | ![Screen Recording 2020-08-03 at 12 22 39 PM](https://user-images.githubusercontent.com/5922187/89219182-2ddbcb80-d584-11ea-9e21-4950c86306a8.gif) |

## 2020-07-29 –– ✨New Page: Schema ✨

We have released a new home page for your graph in Studio that contain's your graph's docs, changelog, and SDL.

|        |                                                 New information about your schema:                                                 |                                                                                                                                    |
| :--------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------: |
|                                                Auto-generated documentation for type and field references.                                                 |                                                Changelog –– what changed and when.                                                 |                                                             Full SDL.                                                              |
| <img width="1284" alt="Screenshot of Types page" src="https://user-images.githubusercontent.com/743976/88816756-bcb6a580-d18a-11ea-9188-7c51ecfe0362.png"> | <img width="1284" alt="" src="https://user-images.githubusercontent.com/743976/88817042-11f2b700-d18b-11ea-903c-e0e0cb975439.png"> | <img width="1284" alt="" src="https://user-images.githubusercontent.com/743976/88818141-5c286800-d18c-11ea-83a6-e69106ec6520.png"> |

## 2020-07-22 –– ✨New Page: Checks ✨

We have released the new Checks page for our schema [checks feature](https://www.apollographql.com/docs/studio/schema-checks/). You can now **see recent checks** that have been run against and **configure your check parameters** from directly within the UI.

<img width="1284" alt="Screen Shot 2020-07-27 at 6 18 29 PM" src="https://user-images.githubusercontent.com/5922187/88608003-96cbbc80-d035-11ea-931c-1fc3a1901ea1.png">

## 2020-07-21

| New in the Explorer:   |            |
| ---------------------- | ---------- |
| You can now see inlined response hints in the Explorer. As you add fields to your query or change variables, the Explorer will make partial requests for new data. | ![Screen Recording 2020-07-27 at 06 15 22 PM](https://user-images.githubusercontent.com/5922187/88607871-2de44480-d035-11ea-81d6-2e7094ae23fb.gif) |

## 2020-07-14

| New in Integrations:      |      |
| :------------------------ | ---- |
| By popular request, you can now use the Datadog-forwarder with Datadog instances in the EU. Head to your graph's Integrations page to configure this 🌍 | ![Screen Recording 2020-08-03 at 01 17 38 PM](https://user-images.githubusercontent.com/5922187/89223506-c1fd6100-d58b-11ea-8e51-0f047d3757ea.gif) |

| New in the Explorer: |     |
| :------------------- | --- |
| You can now configure requests to authenticate with your domain through cookies in the Explorer's settings tab 🍪 | ![Screen Recording 2020-08-03 at 01 21 30 PM](https://user-images.githubusercontent.com/5922187/89223825-536cd300-d58c-11ea-82d5-052c62c66044.gif) |

## 2020-07-07

| New in the Explorer: |     |
| :------------------- | --- |
| You can now manage operations individually using a "meatball" context menu, even when other operations are invalid 🍝 | ![Screen Recording 2020-08-03 at 01 23 27 PM](https://user-images.githubusercontent.com/5922187/89223976-9038ca00-d58c-11ea-8058-a225faf6a2b6.gif) |
| You can now generate variables for your query using autocomplete in the editor.                                       | ![Screen Recording 2020-08-03 at 01 24 22 PM](https://user-images.githubusercontent.com/5922187/89224079-b9f1f100-d58c-11ea-8666-412be8f8bf83.gif) |

## 2020-06-30 –– ✨ New Page: Explorer ✨

We have released the Explorer, available as a top-level page for graphs. The Explorer is a full-featured query building IDE that connects to the registry and can be configured uniquely for each of your variants.

Full details on the release in our announcement post: [Introducing the Apollo Explorer](https://www.apollographql.com/blog/introducing-the-apollo-explorer/).

![Building a query using the Explorer's query builder.](https://user-images.githubusercontent.com/5922187/88606849-954cc500-d032-11ea-8fac-218e391f134d.gif)

## 2020-06-29

We have formally [renamed the product from Graph Manager to Studio](https://www.apollographql.com/blog/graph-manager-is-now-studio/), moved our URL from engine.apollographql.com to studio.apollographql.com, and have updated our website, docs, and in-product references to reflect the change.
