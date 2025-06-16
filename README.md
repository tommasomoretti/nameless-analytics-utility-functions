<picture>
  <source srcset="https://github.com/user-attachments/assets/6af1ff70-3abe-4890-a952-900a18589590" media="(prefers-color-scheme: dark)">
  <img src="https://github.com/user-attachments/assets/9d9a4e42-cd46-452e-9ea8-2c03e0289006">
</picture>

---

# Utility functions
The Nameless Analytics Utility Functions is a set of functions used by [Nameless Analytics Client-side tracker tag](https://github.com/tommasomoretti/nameless-analytics-client-side-tracker-tag/).

For an overview of how Nameless Analytics works [start from here](https://github.com/tommasomoretti/nameless-analytics/).

Start from here:
- [Get client id and session id value](#get-client-id-and-session-id-value)
- [Get the current Consent Mode values](#get-the-current-consent-mode-values)
- [Get user agent details](#get-user-agent-details)
- [Format timestamp](#forma-timestamp)
- [Get Channel grouping](#get-channel-grouping) 



## Get client id and session id value 
Send a request to the Server-side GTM Client Tag, which reads the cookies and returns the values of client_id, session_id, and page_id.

Usage:

```javascript
const full_endpoint_domain = 'https://gtm.namelessanalytics.com/tm/nameless'
const payload = {
  "event_name": "get_user_data", 
  "event_origin": "Website"
}
await get_user_data(full_endpoint_domain, payload)
```


## Get the current Consent Mode values
Get the last consent type and values pushed into the dataLayer.

Usage:
```javascript
get_last_consent_values()
```


## Get user agent details
Parse user agent details using [UA Parser js library](https://www.jsdelivr.com/package/npm/ua-parser-js).

Usage:
```javascript
parse_user_agent()
```


## Format timestamp
Format timestamp into datetime string.

Usage:
```javascript
const timestamp = Date.now()
format_datetime(timestamp)
```


## Get Channel grouping 
Giving a source and a campaign name, calculate the standard channel grouping of those values.

Usage:
```javascript
const source = 'facebook'
const campaign_name = 'test'
get_channel_grouping(source, campaign_name)
```

---

Reach me at: [Email](mailto:hello@tommasomoretti.com) | [Website](https://tommasomoretti.com/?utm_source=github.com&utm_medium=referral&utm_campaign=nameless_analytics) | [Twitter](https://twitter.com/tommoretti88) | [Linkedin](https://www.linkedin.com/in/tommasomoretti/)
