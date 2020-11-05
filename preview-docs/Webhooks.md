# RFC: Webhooks for schema change notifications

To help you better integrate Apollo Studio into your unique workflow, we are starting some work to offer standard webhooks for certain events. The first of those events will be schema changes - any time we detect a change to the schema for your graph.

We are looking for your feedback!

If you have a related need that is not captured below, or if you see things we might be missing or problematic, please engage with us and ask questions through issues on this repository.

## Plan restrictions

Webhooks are available only to customers on our Enterprise plan.

## How this works

We will create a new integration channel: Webhooks.
From our Integrations page you can create new Webhooks channels and select which types of events you want sent to your integration endpoint. Today we're launching with support for Schema Change Events.

### Terms
**Event:** Something that happens in Apollo Studio.

**Event Type:** Events have specific types that denote what happened, including 'schema.change'.

**Event Subscription:** An event subscription is configured to do something when it sees a particular type of event. It is the thing that connects an event to a notification.
*For example: when a `schema.change` event happens, send a webhook notification to a specified destination.*

**Notification:** The message we send to an external service.

**Webhook:** A type of notification sent via a generic HTTP POST request.

**Channel:** The place where we send the notification. 
For webhooks this will be a server endpoint URL. 
For Slack messages this will be a particular Slack channel endpoint.

### Setup

You can configure a Webhook channel at the Graph level. This ability will be restricted to Admins and Contributors in your organization.

You will be asked to specify a name and a destination URL for your webhook channel. You can edit these after initial setup.

Once you've done that you will have the option send a test notification to confirm that your destination service is receiving notifications from us.

When we see a schema change to your Graph we will make an HTTP POST request to the URL specified.
The body of that request will contain a JSON representation of the changes we identified - fields added, fields removed, fields changed, etc as well as a link to retrieve the update schema.

```json
{
  "eventType": "SCHEMA__PUBLISHED",
  "eventID": "dbf6fb65-a418-4e4a-be50-cbc579845913",
  "changes": [
    { "description": "type ServiceMutation: field deleteChannel added" },
    { "description": "type ServiceMutation: field upsertSlackChannel added" },
    { "description": "type AccountMutation: field upsertSlackChannel deprecated" },
  ],
  "schemaURL": "https://graph.api.apollographql.com/<SECRET>",
  "schemaQuery": "query SchemaLookup(secret: <SECRET>) { document }",
  "apiURL": "https://graph.api.apollographql.com/graphql",
  "schemaURLExpiresAt": "2020-12-01:12:00:00.0000Z"
}
```

### Troubleshooting

Sometimes things don't work how you expect them to. To this end, we're including some resiliency in our webhooks.

1. Retries: We will try to send a webhook notification five times before we move on. We will wait a little bit longer each time (exact retry timing TBD).

2. Disabled state: If a particular channel has been failing to receive our notifications for a full day we will disable that channel for you. It will still exist and you will be able to re-enable it whenever you're ready. You can also choose to manually disable a notification channel to stop requests from being sent while you troubleshoot.

### Authenticating webhook notifications

If your destination needs a token or key to ensure that the requests are coming from us you can include it in the URL - either as part of the path (e.g. https://example.com/webhooks/tokenhere) or in a query string parameter (e.g. https://example.com/webhooks/apollo?token=somethingunguessable).

We also provide the option of validating webhook requests with a hash signature. See [GitHub's docs](https://developer.github.com/webhooks/securing/) for reference.

You can also take advantage of [Basic Authentication](https://developer.mozilla.org/en-US/docs/Web/HTTP/Authentication#Basic_authentication_scheme) with a special syntax e.g. https://username:password@example.com/webhooks/apollo. This will cause the provided username and password to be sent in a standard Basic Auth header encoded in base64.

*We strongly encourage you to secure your destination endpoint with HTTPS, particularly when sending credentials in the URL.*

