# RFC: Pre-request scripts and environment variables for [Apollo Studio's Explorer](https://www.apollographql.com/blog/introducing-the-apollo-explorer/).

We received feedback that manually setting static headers in Explorer is not sufficient for organizations with more complex authentication requirements, specifically when tokens are short-lived and manually updating headers is prohibitively cumbersome.

We are looking for further feedback on whether the contents of this proposal will solve those problems.

If you have a need that is not encapsulated below, or if you see things we might be missing, please engage with us and ask questions through issues on this repository.

### The current flow

Explorer collects the "graphql operation", "operation variables", and "headers" from the editor and sends a network request.

<img width="400" alt="current" src="https://user-images.githubusercontent.com/743976/91210001-96791c80-e6da-11ea-9e34-a06b9adfa7fd.png">

There are a few inconveniences with this approach that this proposal hopes to address

- Since "Copy Link to Operation" doesn't include headers, headers that a shared operation requires would need to be shared separately. If you would prefer not to include secrets, those would need to be manually removed.
- Operation in the list of historic operations each contain the raw header values; when secrets expire, each operation's headers would need to be manually updated when they're restored.
- This can be especially frustrating for endpoints where tokens are short-lived, and if the method for obtaining a copy-able token is not convenient.

### Proposed addition part 1: environment variables

A new key-value store would be made available, which can be referenced in Explorer's "operation variables" and "headers" using mustache/handlebars delimiters, i.e. `{{ variable_name }}`. This should feel familiar for users from [postman](https://learning.postman.com/docs/sending-requests/variables/), [insomnia](https://support.insomnia.rest/article/18-environment-variables), or [altair](https://altair.sirmuel.design/docs/features/environment-variables.html)

<img width="700" alt="environment" src="https://user-images.githubusercontent.com/743976/91210006-97aa4980-e6da-11ea-8706-721ba35a9f1a.png">

This partially solves those inconveniences in that now there is only one place to update when tokens expire, and the contents of the "headers" section no longer needs to contain raw secrets and can thus be freely shared.

This also makes it possible for us to create server-persisted shared operations for orgs without needing to solve secret-storage, since the sensitive bits can be stored as `"Authorization": "Bearer {{ token }}"`, and the operation will work as long as the user has the `token` environment variable populated

**Persistence**
- Environment varilables can be persisted in localStorage
- We can make persisting to localStorage opt-in with messaging
- We can make it easy to export and import these values to and/from files (which can be shared using a company's internal sharing infrastructure)

### Proposed addition part 2: pre-request scripts

A [javascript execution sandbox]((https://www.html5rocks.com/en/tutorials/security/sandboxed-iframes/)) will be made available for running user-supplied scripts ahead of each request. Its purpose is mainly to automate authentication steps so org members can explore the graph with less friction. 

The pre-request script will be able to read from and write to environment variables.

Here's an example of what such a script might look like:

```js
if (new Date().getTime() > context.environment.get('token_expires_at') {
  context.sendRequest(
    {
      url: "https://example.com/token",
      header: { ... },
      body: '...',
    },
    function cb(err, res) {
      if (err) {
        throw err;
      } else {
        const json = JSON.parse(res.body);
        context.environment.set('token', json.access_token);
        context.environment.set('token_expires_at', json.expires_at);
      }
    },
  );
}
```

This diagram illustrates how these pieces work together

<img width="1064" alt="pre-request script" src="https://user-images.githubusercontent.com/743976/91210009-98db7680-e6da-11ea-97e6-f7d25d775289.png">

The long-term goal is 
- graph admins would determine whether pre-request scripts is enabled as a feature
- graph admins would provision pre-request scripts (on a per-graph or per-org level), which can then be used by other members of the graph in Explorer.

## Open questions
- "environment variables" is a somewhat overloaded/baggage-laden word in computing, typically refering to the variables made available to processes. It's also what this feature is named in analogous tools (postman/insomnia/altair), possibly chosen because of their parallels. 

  Would the potential for confusion from the term's baggage be large enough to outweigh familiarity for users from analogous tools? ("context" is the current leading contender)
- would we want to persist these environment variables server-side? if so, how can we do that securely?


### References

The proposed workflow heavily references from and should feel familiar to existing tooling from Postman and Insomnia
