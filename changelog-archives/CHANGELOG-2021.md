
## 2021-12-30

| What's new | |
| :--------- | :-: |
| The Fields page can now display how many operations textually reference fields in addition to how many times the fields are executed. This can reveal connections hidden by field executions alone, and it enables you to use the page with federated graphs even if your subgraphs do not all support federated tracing. This new feature requires Apollo Server 3.6 or later. For details, see [the Fields page docs](https://www.apollographql.com/docs/studio/metrics/field-usage/).| ![image](https://user-images.githubusercontent.com/16724/147708671-6b6d15e3-80ce-411f-996f-b8f3d09b1046.jpeg) |

## 2021-12-16

| What's new | |
| :--------- | :-: |
| You can now click the `only` link to quickly filter the clients to the only one you need.| ![image](https://user-images.githubusercontent.com/639025/146469684-d3c0a9f3-bf25-4913-89ef-bff95fc2a184.png) |

## 2021-12-15

| What's new | |
| :--------- | :-: |
| Now you can publish your local schema to the Apollo registry directly from Sandbox! No need to go anywhere, just click `Publish` in Sandbox.| ![image](https://user-images.githubusercontent.com/86634858/146322113-5a9333a3-dd7c-4fff-a34a-46d16324c0fb.png)|

## 2021-12-14

| What's new | |
| :--------- | :-: |
| You can now opt in to using several different Datadog regions to forward metrics! | ![image](https://user-images.githubusercontent.com/6365997/146055693-5300f628-a602-4332-9ea8-7be2cdc0f096.png) |

## 2021-12-10
| What's new | |
| :--------- | :-: |
| You can now sort fields in Explorer docs. Simply click on the arrow next to `Fields`. |![image](https://user-images.githubusercontent.com/86634858/145644410-246e5223-bdd0-42e9-a93f-71eb05e112f4.png)|


## 2021-12-02
| What's new | |
| :--------- | -- |
| Now you can diff your local schema against any registered schema in Apollo Studio, right from Sandbox and understand the changes made. |![image](https://user-images.githubusercontent.com/86634858/144535994-5c31d241-8004-4716-aafa-c90400aabe65.png) |
| You can also run operation checks right from Sandbox! While developing locally in Sandbox, make sure there are no breaking changes by running operation checks before pushing the updated schema to Studio. | ![image](https://user-images.githubusercontent.com/86634858/144536075-9cd9b2d0-4bb9-4b3e-8081-262a7e813a1e.png)|

## 2021-11-01
| What's new | |
| :--------- | :-: |
| We have upgraded the data visualization charts across Studio. This upgrade includes performance improvements, interaction upgrades, and numerous bug fixes. | ![image](https://user-images.githubusercontent.com/5922187/139733140-2b1fdb7f-2cf5-4b43-b563-416f077378e5.png) |


## 2021-10-29
| 🐛 Bug fix |
| :--------- |
| We fixed a bug in Explorer where field latency approximation editor hints were displaying latencies 1000 times larger than the actual latency.  |

## 2021-10-26
| What's new | |
| :-- | :-: |
| We have made embedding Explorer MUCH easier! With our first release, you had to read and understand the full documentation and copy a volume of code in order to get started. But now you can just generate the code in a few clicks. Head over to Explorer for any public graph, and under Explorer Settings, find **Embed Explorer**. Toggle on/off options as you like, use the operation in your editor as the default and copy the code snippet to paste - that is it!! Embed Explorer to enable consumers to test out the graph from your own website, blog posts, documentation, etc. using the amazing Explorer experience. Read more [here](https://www.apollographql.com/docs/studio/embed-explorer/). |![image](https://user-images.githubusercontent.com/86634858/139114580-9edb0cff-a7ae-425c-964c-eeb33386fc26.png)

## 2021-10-20
| 🐛 Bug fix |
| :--------- |
| We fixed a bug in Schema Checks where excluding multiple client versions would cause the Schema Check to always fail.  |

## 2021-10-14
| What's new | |
| :-- | :-: |
| Graphs can now have avatar images, which you can set on your graph's settings page. | ![image](https://user-images.githubusercontent.com/5922187/137417468-3c7f52b1-873c-4a11-9c25-e3d519f1f16b.png) |

## 2021-10-07
| 🐛 Bug fix |
| :--------- |
| We fixed a bug on the Operations tab where changing the selected operation would also cause the client filter to lose its state.  |

## 2021-09-30
| What's new | |
| :-- | :-: |
| **Admins** can now share their graphs with users outside of their Studio organization. On the Graph Settings page, under the Access tab, toggle the switch for the specific graph variant you want to make public and share the public graph URL with consumers external to the Studio organization! Read more [here](https://www.apollographql.com/docs/studio/org/graphs/#public-variants). | ![image](https://user-images.githubusercontent.com/86634858/135554900-22c6e099-b879-47d3-b062-f602261cf9fa.png) |
| Given a public variant, graph producers can now embed Apollo Studio Explorer on any webpage to share that public variant with consumers! This will enable consumers to test out the graph from your own website, blog posts, documentation, etc. Read more [here](https://www.apollographql.com/docs/studio/embed-explorer/). |![image](https://user-images.githubusercontent.com/86634858/135555343-42c673e0-f189-4000-8906-a82ddcbe58c3.png)|

## 2021-09-29 — ✨ The Champion Dashboard ✨
| What's new | |
| :-- | :-: |
| **Org Admins** now have access to a new page on their account, the **Dashboard**, which gives an overview of your Studio account's usage. The **Dashboard Page** shows your plan and its features, how many users you have and their roles, the support tickets submitted by members of your org, the request volumes sent by your graphs, the number of graphs and variants in your account, the schema publish volumes across your graphs, the number of checks being run by your graphs, and their success/failure rate. | ![image](https://user-images.githubusercontent.com/5922187/135341580-088bab2e-63f3-4424-b920-a07cdf40a410.png) |

## 2021-09-23 — ✨ Tabs in Apollo Studio Explorer ✨
| What's new | |
| :-- |  :-: |
| Test out multiple operations in different tabs when exploring your GraphQL API in Apollo Studio Explorer!!| ![image](https://user-images.githubusercontent.com/86634858/134574846-0572013c-4e4f-4615-a0f5-761eb99f24d0.png) |

## 2021-09-20 — ✨ The README - A new graph landing page ✨
| What's new | |
| :-- |  :-: |
| Graph maintainers can now provide information about the graph and how to get started with the graph natively in Apollo Studio with the new README page. The README appears as a new icon in the left nav in Apollo Studio and will now be the default page shown when navigating to any graph variant in Apollo Studio. README is not just another markdown, it also has one-click access to graph shortcodes - graph variables such as name, ref, SDL, endpoint, etc. that can be easily referred to in the README content. We have provided some default README content to get you started, so check it out today in Apollo Studio and get editing!| ![image](https://user-images.githubusercontent.com/86634858/134107643-1afac63f-33ec-475d-8f8b-18cbb26c58c0.png) |

## 2021-09-15 — ✨ Be offline and develop locally on Apollo Sandbox ✨
| What's new |
| :--------- |
| [Offline support](https://www.apollographql.com/docs/studio/explorer/#offline-sandbox) for local development with Apollo Sandbox is now available! 🎉 If you are developing locally using Sandbox, you can continue to work without any internet connection. In order to see this change, please reload at least one Sandbox tab while still connected to the internet one time (to update to the latest bundle) and after that continue to work without any internet connection.

## 2021-08-25
| What's new | |
| :-- |  :-: |
| On the Launches page, you can now see which subgraphs changed as part of your launch, as well as whether they were modified, added, or removed! | ![image](https://user-images.githubusercontent.com/6365997/130810679-b073b485-84c2-4a06-bc03-549f0586063b.png) |

## 2021-08-19
| What's new 🌔 🌕 🌚  | |
| :--------- | -- |
| We've updated Studio's top nav to be dark instead of light. We hope you enjoy this in particular when using the Explorer in dark mode :) | ![image](https://user-images.githubusercontent.com/5922187/130103185-f4e74045-75f3-46e3-997b-126f73ae02c6.png) |
| We've updated Studio's new Launches feature to include a diff view of the supergraph schema! You can now see all schema-level changes in this view, and we'd love any [feedback](https://forms.gle/woXCdtyz1PFqcP7q7) you have on how to enrich your experience further in the new Launches page. | ![image](https://user-images.githubusercontent.com/6365997/130291167-361340bb-8550-4a1e-8215-c8506cec9e6d.png) |

## 2021-08-18
| 🐛 Bug fix |
| :--------- |
| We fixed a recently introduced Schema Checks bug where users were unable to mark changes as safe for "broken" operations. |

## 2021-08-17 — ✨ New Feature: Launches ✨
| What's new | |
| :-- |  :-: |
| For Studio Enterprise teams, there is a new tab within Studio that lets you observe the history and status of releases to your federated graph. Look for the rocket icon in your graph's home page to explore your federated launches in more detail! | ![image](https://user-images.githubusercontent.com/6365997/129747238-e7ebe13e-6ee8-4d90-bbc5-41df5ff4e70a.png) |

## 2021-08-05 — ✨ New Feature: Audit Logs ✨
| What's new | |
| :-- |  :-: |
| For Studio Enterprise teams, it is now possible to export a data file with key actions taken within your organization. You can find the Audit Log interface under the "Audit" tab of your organization's home page. You can [read more about the feature here](https://www.apollographql.com/blog/announcement/platform/audit-logs-now-available-in-apollo-studio-enterprise/). | ![image](https://user-images.githubusercontent.com/5922187/128379498-e65cb4c4-1d3c-4384-8d7e-ca15ab432033.png) |


## 2021-08-04
| What's new | |
| :-- |  :-: |
| It's now possible to delete variants that do not have active publishes or have invalid characters in their names | ![image](https://user-images.githubusercontent.com/6365997/128200389-c1b2c409-7b5f-4e1b-b775-2c9e079a518c.png) |

## 2021-07-26
| What's new | |
| :-- |  :-: |
| Default Headers are now generally available! In the Explorer Settings tab, Graph Administrators can specify headers that will be applied to every Explorer request executed by every user in your organization. | ![image](https://user-images.githubusercontent.com/24704789/127037888-2c0c5de2-3ffb-44f1-95c1-ca4888907c73.png) |
| You can now also provide sensitive tokens and information to header values in Explorer's Environment Variables tab. | ![image](https://user-images.githubusercontent.com/24704789/127039872-c3aebc49-387a-4ac0-b6d5-8eab92cff71c.png) |

## 2021-07-20 — Organization Reorganization
| What's new | |
| :-- | -- |
|  It's now simpler than ever to navigate your organization (or multiple orgs) in Studio thanks to the new org picker. From the menu, you can switch organization context (if you are signed in to multiple orgs), create a new organization, or return to your organization index by selecting the organization item. | ![image](https://user-images.githubusercontent.com/1319791/126541995-36f0233f-290e-4edb-b590-28f487223bd5.png) |

## 2021-06-15 — ✨ New Page: Sandbox ✨

We have released [Sandbox](https://studio.apollographql.com/sandbox), making the Apollo Explorer openly available to any developer, with no login required.

Full details on the release in our announcement post: [Apollo Sandbox: an open GraphQL IDE for local development
](https://www.apollographql.com/blog/announcement/platform/apollo-sandbox-an-open-graphql-ide-for-local-development/).

[![image](https://user-images.githubusercontent.com/743976/122124968-fe315d00-cdfd-11eb-91df-910408dc8d9c.png)](https://www.apollographql.com/blog/announcement/platform/apollo-sandbox-an-open-graphql-ide-for-local-development/)


## 2021-06-14
| What's new | |
| :-- | -- |
| You can now cancel your Studio Team subscription, re-activate a canceled subscription, and switch between Monthly and Annual billing on your Organization's Settings page. No need to write into customer support for this anymore :) | ![image (117)](https://user-images.githubusercontent.com/5922187/121956576-26459100-cd16-11eb-8856-14d582e6bec4.png) |

## 2021-06-02
| What's new | |
| :-- | -- |
| Headers in the Explorer can now be disabled so you can swap back and forth between them while you are testing without having to delete any. Additionally, any default headers added by your Graph Administrator will now show up as unmodifiable. | ![image](https://user-images.githubusercontent.com/24704789/120672777-9a537f80-c460-11eb-8001-9fb14397dc54.png) |


## 2021-05-24
| 🐛 Bug fix |
| :--------- |
| We had a bug where there were some circumstances where users couldn't rename their organizations. This is now fixed! |

## 2021-05-20
| What's new | |
| :-- | -- |
| The Checks page now includes a "status" filter to show only checks that match a specific status, making it easy to surface failed checks from your graph's check history. | ![image](https://user-images.githubusercontent.com/1831709/118909465-652a3600-b966-11eb-86a6-f67db623f74f.png) |

## 2021-05-07
| What's new | |
| :-- | -- |
| The Schema > SDL page now features a type outline that you can use to quickly get to the type you are looking for without having to scroll through the entire SDL contents. | ![image](https://user-images.githubusercontent.com/6412529/117553733-05e43180-b008-11eb-9f8f-85478c743f0e.png) |

## 2021-04-26
| What's new | |
| :-- | -- |
| Role-specific invitation links are now available. You can create or manage invite links from you org's settings page. | ![image](https://user-images.githubusercontent.com/743976/116169961-d530fd80-a6d3-11eb-8e55-35dd0582f7a9.png) |

## 2021-04-20
| What's new |
| :-- |
| Studio's onboarding has been significantly simplified. It now takes only one step to create an account and log in, as opposed to our previous multi-step onboarding wizard. |

## 2021-04-19
| What's new |
| :-- |
| The Checks page now includes schema composition details for federated graphs! Additionally, the Checks page now displays checks for all variants in the same area, and new filters allow you to find relevant checks by author, branch and subgraph.  [Read more in our announcement post](https://www.apollographql.com/blog/announcement/build-checks-webhooks-apollo-studio/). |

## 2021-04-06
| What's new | |
| :-- | -- |
| All plans on Apollo Studio now include unlimited read-only "Consumer" seats! You can now invite everyone in your organization to view your graphs in the registry, with access to Explorer, the schema reference, and the schema changelog. [Read more in our announcement post](https://www.apollographql.com/blog/sharing-your-graph-just-got-a-whole-lot-easier-announcing-unlimited-consumer-seats/).  | ![image](https://user-images.githubusercontent.com/3953093/113786973-3171b480-9708-11eb-8092-c02cec840b8e.png)|

## 2021-04-01
| What's new | |
| :-- | --|
| Studio now includes several new features to improve the experience of working with Federated graphs. | ![image](https://user-images.githubusercontent.com/1319791/113793030-36c90200-96fc-11eb-918e-1822897ad179.png) |
| The Schema > Reference tab in Studio displays a table of your federated schema’s types and fields. This table now includes a Subgraph column | ![image](https://user-images.githubusercontent.com/1319791/113791127-d20ba880-96f7-11eb-9818-4d196152912e.png) |
| Federated graphs will now also display their Subgraphs on the **Schema > SDL tab** (the older experience at the Services tab has moved here). This includes support for... | ![image](https://user-images.githubusercontent.com/1319791/113793069-4b0cff00-96fc-11eb-9d48-84fa03ca52f8.png) |
| ...[linking directly to types, fields, arguments and directives](https://www.apollographql.com/docs/studio/federated-graphs/#viewing-a-fields-originating-subgraph) | ![image](https://user-images.githubusercontent.com/1319791/113791542-be147680-96f8-11eb-93d9-4692bde0a0d1.png) |
| ...filtering out comments & deprecated fields from view for a cleaner browsing experience | ![image](https://user-images.githubusercontent.com/1319791/113791570-d2f10a00-96f8-11eb-805e-2304c5b6951f.png) |
| ...and using Studio search to jump directly to objects in your SDL | ![image](https://user-images.githubusercontent.com/1319791/113791654-f9af4080-96f8-11eb-95c9-235dad476684.png) |
| Users with preview features enabled in personal settings will also be able to see the [Supergraph SDL](https://www.apollographql.com/docs/studio/federated-graphs/) on the SDL page after your next schema push. | ![image](https://user-images.githubusercontent.com/1319791/113791825-57438d00-96f9-11eb-845b-b3a73a458422.png) |
| You can now designate a contact person or team for each subgraph by [using the `@contact` directive](https://www.apollographql.com/docs/studio/federated-graphs/#subgraph-contact-info) in your Subgraph SDL. | ![image](https://user-images.githubusercontent.com/1319791/113792192-29ab1380-96fa-11eb-8db9-748f68cc4863.png) |
| ...when you do, you'll see the Subgraph owner info displayed in the Subgraph SDL meta info on the **Schema > SDL** tab... | ![image](https://user-images.githubusercontent.com/1319791/113792259-595a1b80-96fa-11eb-9658-8d9816da99fa.png) |
| ...and when you hover over the Subgraph column for Schema objects in the **Schema > Reference** tab. | ![image](https://user-images.githubusercontent.com/1319791/113792350-97573f80-96fa-11eb-8171-bf75cc40f8bb.png) |
| If your graph has composition errors, the label on your Federated graph will display in an error state. |![image](https://user-images.githubusercontent.com/1319791/113792563-1ba9c280-96fb-11eb-8758-ded1f7c0ef56.png)|
| Clicking the label will open the composition errors modal so you can [see the errors from anywhere within Studio](https://www.apollographql.com/docs/studio/federated-graphs/#viewing-composition-errors). | ![image](https://user-images.githubusercontent.com/1319791/113792942-fd909200-96fb-11eb-81f6-2813737aecca.png) |
| The **Schema > SDL** page also displays a warning banner on the API schema and the Supergraph schema when composition has failed... | ![image](https://user-images.githubusercontent.com/1319791/113792756-865afe00-96fb-11eb-8b37-254a76fcb549.png) |
| ...and error banners on the Subgraphs. | ![image](https://user-images.githubusercontent.com/1319791/113792783-95da4700-96fb-11eb-9f4b-c0911ef3c749.png) |
| Learn more about the new features for Federated graphs at the [Federated Graphs in Studio](https://www.apollographql.com/docs/studio/federated-graphs/) Apollo Docs article. ||

## 2021-03-19
| What's new | |
| :-- | -- |
| When creating a graph you can now see and change the id of your graph | ![Screen Recording 2021-03-19 at 02 58 PM](https://user-images.githubusercontent.com/3953093/111830001-c92b7200-88c3-11eb-9a19-c911e5c6b051.gif) |

## 2021-03-15
| What's new | |
| :-- | -- |
| You can now see your **Graph Reference** on the Schema Reference page, which is useful when running commands with the Apollo CLI. | <img width="924" alt="Screen Shot 2021-03-15 at 1 14 21 PM" src="https://user-images.githubusercontent.com/5922187/111215598-4e9be300-85a1-11eb-9790-f86d79eb2440.png"> |
| You can now see your **Graph ID** on your graph's settings page. | <img width="1125" alt="Screen Shot 2021-03-15 at 1 15 05 PM" src="https://user-images.githubusercontent.com/5922187/111215602-4fcd1000-85a1-11eb-8ccb-8c8b3ff2f34d.png"> |

## 2021-03-09
| What's new |
| :--------- |
| ⚡️ Significantly improved Schema Page's performance for very large schemas |



## 2021-03-08
| What's new | |
| :--------- | :--: |
| The `creator` and `createdAt` time for your Graph API keys are now visible in your Graph Settings.  | ![image](https://user-images.githubusercontent.com/5922187/110336558-98f1f280-7fea-11eb-9503-d5bef3cba8f0.png) |
| You can now write and save descriptions on your Graphs, which lets you differentiate them and describe them to your users more easily. | ![image](https://user-images.githubusercontent.com/5922187/110337838-f8043700-7feb-11eb-8cb9-74c7b5e0a755.png) |
| You can now send headers along with your Introspection Queries when using Dev Graphs. | ![image](https://user-images.githubusercontent.com/5922187/110374431-4b8b7a80-8016-11eb-8df2-f704121a04b2.png) |

## 2021-03-04
| Security Upgrade |
| :--------------- |
| We have made a change to the way you use API keys with Studio: API keys are no longer be visible in plain text in your Graph and User Settings pages. You will only be able to see your API key secret in the moment that you first create it in Studio. This is security change we have made to reduce the probability of keys being accidentally leaked from our system. If you need to recover a token you have previously created, you can request help from us at support@apollographql.com. We recommend you just make a new token though. All existing keys will continue to work as-is, and no action is necessary as part of this change. |

## 2021-02-26
| What's new |
| :--------- |
| Community and Team plans can now assign users [the Billing Manager role](https://www.apollographql.com/docs/studio/org/members/#organization-wide-member-roles), in addition to the default Org Admin role. You can change this on your organization's membership page. |

## 2021-02-18
| What's new | |
| :--------- | :-: |
| We added a feature to introduce Dev Graphs. If you have opened a Dev Graph recently you may see an informative popup! | ![image](https://user-images.githubusercontent.com/14367451/108418344-f6620300-71e5-11eb-804c-229cf2793651.png) |

## 2021-02-17
| What's new |
| :--------- |
| We make a performance improvement to the Operations page; it should no longer slow down dramatically and/or become unresponsive when your graph has a very large number of clients. |

## 2021-02-15
| What's new |
| :--------- |
| 🚥 We shipped a small change to how Development Graphs poll their status so that they’re no longer polling for connectivity status on the Graph List page. When you're using a Dev Graph, you can also turn off its polling with the controls in the global nav. |


## 2021-02-10
| What's new | |
| :--------- | :--: |
| Defer loading of some data to making initial render of graph list faster | ![Screen Recording 2021-02-15 at 06 55 15 PM](https://user-images.githubusercontent.com/5922187/108012921-680c3800-6fbf-11eb-9707-c9ec5adeb5d0.gif) |


## 2021-02-08
| Security Upgrade |
| :--------- |
| We are upgrading our minimum TLS version to 1.2 for communications with our APIs. This is being done as 1.1 has largely been deprecated industry wide for some time now, and our client's security is a top concern for us. For more information, please see our [StatusPage maintenance notice here](https://status.apollographql.com/incidents/chgzx4ppw5z9) |

| What's new | |
| :--------- | :--: |
| Protected variants and hidden graphs are now labeled as such in the Graph List page. | ![image](https://user-images.githubusercontent.com/5922187/107260189-baaf8800-69f2-11eb-9f0a-da2b1aef37a5.png) |
| You can now turn on a setting in the Explorer to inline the timings from your traces next to your operation's fields when you run your operation. | <img width="1254" alt="Screen Shot 2021-01-28 at 6 34 12 PM" src="https://user-images.githubusercontent.com/6856868/106212069-c9e33a00-6197-11eb-844f-a663c64881b8.png"> |



## 2021-02-03
| What's new |
| :--------- |
| We have moved all of our integrations configurations to the Graph Settings area. Please visit your graph's settings page if you are you looking to set up Slack notifications, Datadog forwarding, etc. |

## 2021-02-01
| What's new |
| :--------- |
| We've added **Schema Change Webhooks** ![webhooks icon](https://studio-staging.apollographql.com/icons/webhook.svg) for our Enterprise customers! We also updated Studio to remove the *Integrations* section and integrate it into *Settings*.<ul><li>You can now find Datadog settings under *Settings > General*.</li><li>Notification integrations including PagerDuty, Slack, and now Webhooks for Enterprise customers can be found under *Settings > Notifications*.</li><li>To setup a webhook for schema changes click *Add Notification*, select *Schema Change*, select the Variant you're interested in, *Create new channel*, *Webhook*.</li><li>Schema Change Webhooks will contain a string description of the schema change as well as a temporary URL which you can use to fetch the full updated schema. This link remains active for 24 hours.</li><li>See our updated [documentation](https://www.apollographql.com/docs/studio/notification-setup/#custom-webhooks-enterprise-only) for more information, and [let us know](https://github.com/apollographql/apollo-studio-community/issues/new) if you have any feedback - or interesting integrations - to share!</li>|

## 2021-01-29
| What's new |    |
| :--------- | -- |
| The Recent Checks page has a new treatment of implementing services, along with clearer indications of the case when the "branch" or "author" is left un-set. Check it out! | ![image](https://user-images.githubusercontent.com/6365997/106220710-f051a700-6190-11eb-9115-394109288864.png) |

## 2021-01-28
| 🐛 Bug fix |
| :--------- |
| We have fixed a **(very)** long-standing bug with our GitHub logins. Previously, if you changed your GitHub username and tried to log in to Studio again, you’d end up with a brand new unrelated account. (Also if your username was somebody else’s “old username” who had logged in to Studio from GH with that username, you were locked out of using Studio entirely.) We’ve fixed this: you can change your GitHub username as much as you want and you can still log in.|

## 2021-01-27
| What's new |    |
| :--------- | -- |
| The graph gelector dropdown in the top nav now extracts your **favorites** and **current graph** to the top of the options list. | ![image](https://user-images.githubusercontent.com/5922187/106041335-8520ab80-6090-11eb-9756-0cdc421e11a5.png) |

## 2021-01-26
| What's new |    |
| :--------- | -- |
| In federated graphs, you can now see which subgraph(s) each field in your operations comes from in the Explorer. | <img width="1359" alt="Screen Shot 2021-01-25 at 2 49 16 PM" src="https://user-images.githubusercontent.com/5922187/105948444-ccbb1f00-601f-11eb-9147-8cc840972db6.png"> |
| Headers in the Explorer are now managed using input fields, instead of JSON :) | <img width="492" alt="Screen Shot 2021-01-25 at 6 13 11 PM" src="https://user-images.githubusercontent.com/5922187/105948442-cb89f200-601f-11eb-867e-e740ecc83470.png"> |

## 2021-01-19
| What's new |    |
| :--------- | -- |
| We've enhanced the [user roles system](https://apollographql.com/docs/studio/org/members/) available to Enterprise customers! <ul><li>Users can be granted a **role on a specific graph** with more permissions than their organization-level role.</li><li>A graph can be **hidden** from non-Organization Admin users that have not been explicitly granted a role on that graph.</li><li>Each [**graph API key**](https://apollographql.com/docs/studio/api-keys/#setting-permissions) now has a role (Graph Admin, Contributor, Observer, or Consumer) which limits their permissions. (Existing graph API keys retain their existing permissions.)</li><li>A new **Graph Admin** role has complete control over graphs (including managing graph-specific roles) but no organization-level administrative permissions. Existing Contributors have been changed to this role.</li><li>The Contributor role now is very similar to the Observer role, plus the ability to push new versions of the graph's schema. You can now mark individual variants as **protected**; you need to be a **Graph Admin** to push schemas to these variants.</li></ul> | <img width="600" src="https://user-images.githubusercontent.com/16724/105080845-406c9300-5a46-11eb-8c22-94122e4a5a93.png"> |

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
