## 2023-02-20
| What's new | |
| :--------- | :-: |
| Apollo Studio now allows you to **disable operation checks** for a graph variant. Some users may find it useful to skip operation checks when working in a development variant. If you use this setting, please make sure you are using **Rover v0.12.0** or higher.    | ![image](https://user-images.githubusercontent.com/9286598/219827562-a5eb5d55-7260-4112-a361-3564a1d10844.png)

## 2023-02-11
| What's new | |
| :--------- | :-: |
| **Add a Variant right from Studio**, via the new 'Add Variant' button in your Graph Settings. | ![image](https://user-images.githubusercontent.com/14367451/218590889-d8aaa9d8-f11f-4c54-8b2d-18c880798e8a.png)

## 2023-02-11
| What's new | |
| :--------- | :-: |
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
