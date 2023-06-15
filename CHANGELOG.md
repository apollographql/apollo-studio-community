[comment]: <> "NOTE! Ensure all images are added via the \[label\]\(link\) syntax!"

## 2023-06-15
| What's new | |
| :--------- | :-: |
| **Schema Linter is now available in Studio 🎉!** Lint checks will now run as part of the check workflows, allowing you to enforce formatting conventions and GraphQL schema design best practices. Easily configure the severity of each rule in the linter settings under the checks workflow configuration per graph. You can additionally perform one off linting with Rover CLI. Learn more [here](https://www.apollographql.com/docs/graphos/delivery/schema-linter/).  | ![schema linter](https://github.com/apollographql/apollo-studio-community/assets/10705986/9115e72a-779d-481c-8872-c9ec6abc510a) |

## 2023-05-01
| What's new | |
| :--------- | :-: |
| Easily find operations with an empty operation name using the **new "Unnamed operations" filter!**| ![unnamed operations](https://user-images.githubusercontent.com/9868979/235502626-161eefd5-d2ba-47ed-aa50-43f58143342e.gif) |

## 2023-04-13
| What's new | |
| :--- | :-: |
| **📓 Schema Checks in Launches have been removed.** Studio no longer supports Schema Checks as a part of Launches. We strongly recommend that users use rover and our full featured Checks offering to prevent Launches which will negatively impact your traffic, as this is the best way to control changes to your Supergraph. If you would like to see Checks and change management in Launches, please get ahold of your account rep, we'd love to hear from you! | |

## 2023-04-03
| What's new | |
| :--- | :-: |
| **File upload is now supported in Explorer 🎉!** For servers that support file upload, you can now send operations with files using the 'Add files' button on the Variables tab in Explorer. Toggle multi file support on if you are running an operation that supports multi file upload.| ![example use of the new file upload 'add files' button](https://user-images.githubusercontent.com/14367451/229630103-9070ac8e-174d-4168-a362-d59548d06802.png) |


## 2023-03-14
| What's new | |
| :--- | :-: |
| **Entities are now easily distinguishable in the Schema Reference Page!** | ![example of new schema reference page](https://user-images.githubusercontent.com/24704789/224794960-3854bc34-6777-4a51-a1a1-d56f64c517aa.png) |

## 2023-03-07
| What's new | |
| :--- | :-: |
| **The graph list now has search!** Also, if your account is on our Serverless plan and you had a combination of Supergraphs and Classic Graphs in your account, you will now find all your graphs unified under a single **Graphs** tab. | ![example of using new studio search bar](https://user-images.githubusercontent.com/5922187/223514626-fc6eba25-fdae-42ad-a927-928b5c75745a.gif) |

## 2023-02-23
| What's new | |
| :--------- | :-: |
| **Easily distinguish which types are entities in Explorer with an `E` icon!**| ![image](https://user-images.githubusercontent.com/86634858/221050891-627be4aa-6d4a-4087-8d0c-ec897a8627db.png)
| **Extract or wrap with inline `@defer` fragment** in Explorer by right clicking on the operation. No need to learn any syntax, simply defer away! | ![image](https://user-images.githubusercontent.com/86634858/218832989-b82c034e-dab9-4a44-b2a6-f4a6c9a8e278.png)

## 2023-02-20
| What's new | |
| :--------- | :-: |
| Apollo Studio now allows you to **disable operation checks** for a graph variant. Some users may find it useful to skip operation checks when working in a development variant. If you use this setting, please make sure you are using **Rover v0.12.0** or higher.    | ![image](https://user-images.githubusercontent.com/9286598/219827562-a5eb5d55-7260-4112-a361-3564a1d10844.png)

## 2023-02-11
| What's new | |
| :--------- | :-: |
| **Add a Variant right from Studio**, via the new 'Add Variant' button in your Graph Settings. | ![image](https://user-images.githubusercontent.com/14367451/218590889-d8aaa9d8-f11f-4c54-8b2d-18c880798e8a.png)
| **Subgraphs Page for supergraphs**, a new page in Studio, is now available in Studio! Browse the subgraphs that make up your supergraph, and add or remove subgraphs right from Studio. | ![image](https://user-images.githubusercontent.com/14367451/218590885-2fa01e5b-cce2-4440-a377-d18611847698.png)

## 2023-02-08
| What's new | |
| :--------- | :-: |
| Based on popular request, Apollo Studio now supports [Operations Scripts](https://www.apollographql.com/docs/graphos/explorer/connecting-authenticating/#operation-scripts)! Operation scripts can be used for performing complex automations or for testing [sequence of operations](https://www.apollographql.com/docs/graphos/explorer/connecting-authenticating#chaining-operations). This feature comes with powerful IntelliSense capability that you can use to find the exact graphref, collection and operation to use in the script! |![image](https://user-images.githubusercontent.com/86634858/218589899-e97f7eb2-2fb9-450c-9b2a-48fa1d5073f0.png)


## 2023-01-11
| What's new | |
| :--------- | :-: |
| **Automatically hiding unreachable schema elements**, a contracts feature, is now available in Studio! Up until today, tagging schema elements was very inconvenient especially when there were schema elements like inputs and enums that were unreachable anyway. Now we provide an option to automatically hide those unreachable elements to create a more pleasant user experience, helping you build faster and more efficiently!   | ![image](https://user-images.githubusercontent.com/10705986/213568890-6b0543e1-6c88-45de-b480-52bf82c7ff5a.png)

## 2023-01-09
| What's new | |
| :--------- | :-: |
| Observers+ will now see the keys of an entity on the schema reference page   | ![image](https://user-images.githubusercontent.com/3953093/211340734-9c979f70-75e0-4bcd-8dc8-289b406c2e4c.png)

## 2023-01-09 We now flatten objects in an array if they are all simple values in the object!
| What's new | **Table Mode** in Explorer will now collapse arrays of simple objects into individual columns in the table. This should make CSVs exported from Table Mode much more pleasant to work with. | 
| :--------- | :-: |
| Before | ![image](https://user-images.githubusercontent.com/3953093/209742555-a01f5e1d-f3a7-4f91-aa13-d6dc1c67887f.png) |
| After | ![image](https://user-images.githubusercontent.com/3953093/209742580-99d73a06-e941-4127-b8f9-07af457269c1.png)

## 2023-01-03 Happy new year! 🥳
| What's new | |
| :--------- | :-: |
| We have added a new column called **Updates Available** to the **Graphs** card of the **Champion Dashboard**, which lets you see update notices for the GraphQL servers you're running at a glance.  | ![image](https://user-images.githubusercontent.com/5922187/210436128-ddc665c1-2ba3-4383-9ab6-21310bd04a46.png) |
| When you click on an upgrade notice, you can see which version of Apollo Server or Apollo Router your graph is running. You can see what level of long-term support Apollo is providing for that server and wether there's a new version to upgrade to with a link to the changelog. | ![image](https://user-images.githubusercontent.com/5922187/210436038-4399cd5b-19fd-42ed-b644-40f03bc64dd2.png)

---
For entries before 2023 see the [changelog archives](https://github.com/apollographql/apollo-studio-community/tree/main/changelog-archives).
