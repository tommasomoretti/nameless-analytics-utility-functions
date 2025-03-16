![Na logo beta](https://github.com/tommasomoretti/nameless-analytics/assets/29273232/7d4ded5e-4b79-46a2-b089-03997724fd10)

---

# Utility functions
The Nameless Analytics Utility Functions is a set of functions used by [Nameless Analytics Client-side tracker tag](https://github.com/tommasomoretti/nameless-analytics-client-side-tracker-tag).

For an overview of how Nameless Analytics works [start from here](https://github.com/tommasomoretti/nameless-analytics).

Start from here:
- [Get client id and session id value](#get-client-id-and-session-id-value)
- [Get the current Consent Mode values](#get-the-current-consent-mode-values)
- [Get user agent details](#get-user-agent-details)
- [Format timestamp](#forma-timestamp)
- [Get Channel grouping](#get-channel-grouping) 



## Get client id and session id value 
Send a request to the Server-side GTM Client Tag, which reads the cookies and returns the values of client_id, session_id, and page_id.

<img width="1512" alt="Screenshot 2024-11-03 alle 13 08 16" src="https://github.com/user-attachments/assets/51169268-dbc7-4a64-b09a-74b3b778155f">

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

<img width="1512" alt="Screenshot 2024-11-03 alle 13 11 35" src="https://github.com/user-attachments/assets/cfb3314a-3a7d-4938-84e3-9e4c861cc581">

Usage:
```javascript
get_last_consent_values()
```


## Get user agent details
Parse user agent details using [UA Parser js library](https://www.jsdelivr.com/package/npm/ua-parser-js).

<img width="1512" alt="Screenshot 2024-11-03 alle 13 16 02" src="https://github.com/user-attachments/assets/0907137c-c94e-4497-9cd3-484a78f3c396">

Usage:
```javascript
parse_user_agent()
```


## Format timestamp
Format timestamp into datetime string.

<img width="284" alt="Screenshot 2024-11-03 alle 13 20 07" src="https://github.com/user-attachments/assets/f0ccd66b-77f1-47cc-ae6b-7a61a4563eb9">

Usage:
```javascript
const timestamp = Date.now()
format_datetime(timestamp)
```


## Get Channel grouping 
Giving a source and a campaign name, calculate the standard channel grouping of those values.

<img width="1512" alt="Screenshot 2024-11-03 alle 13 49 09" src="https://github.com/user-attachments/assets/cf6692ac-fd11-44bb-9cbf-22960a9b89e2">

Usage:
```javascript
const source = 'facebook'
const campaign_name = 'test'
get_channel_grouping(source, campaign_name)
```

---

Reach me at: [Email](mailto:hello@tommasomoretti.com) | [Website](https://tommasomoretti.com/?utm_source=github.com&utm_medium=referral&utm_campaign=nameless_analytics) | [Twitter](https://twitter.com/tommoretti88) | [Linkedin](https://www.linkedin.com/in/tommasomoretti/)
