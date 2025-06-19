<picture>
  <source srcset="https://github.com/user-attachments/assets/6af1ff70-3abe-4890-a952-900a18589590" media="(prefers-color-scheme: dark)">
  <img src="https://github.com/user-attachments/assets/9d9a4e42-cd46-452e-9ea8-2c03e0289006">
</picture>

---

# Utility functions
The Nameless Analytics utility functions is a set of javascript functions used by [Nameless Analytics Client-side tracker tag](https://github.com/tommasomoretti/nameless-analytics-client-side-tracker-tag/). 

They can be used to get the client and session id, get user agent details, format fimestamp, get channel grouping or get last consent status.

For an overview of how Nameless Analytics works [start from here](https://github.com/tommasomoretti/nameless-analytics/).

Table of contents:
- [Get client id and session id value](#get-client-id-and-session-id-value)
- [Get the current Consent Mode values](#get-the-current-consent-mode-values)
- [Get user agent details](#get-user-agent-details)
- [Format timestamp](#format-timestamp)
- [Get channel grouping](#get-channel-grouping)



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

Expected output:
```json
{
  "event_name": "get_user_data",
  "client_id": "iURYgLE478F7TZU",
   "session_id": "iURYgLE478F7TZU_yt726CejxG8pyDW",
   "page_id": "X9zgxcyvbNwM0qt"
}
```



## Get the current Consent Mode values
Get the last consent type and values pushed into the dataLayer.

Usage:
```javascript
get_last_consent_values()
```

Expected output:
```json
{
  "consent_type": "update",
  "ad_user_data": false,
  "ad_personalization": false,
  "ad_storage": false,
  "analytics_storage": true,
  "functionality_storage": false,
  "personalization_storage": false,
  "security_storage": false
}
```



## Get user agent details
Parse user agent details using [UA Parser js library](https://www.jsdelivr.com/package/npm/ua-parser-js).

Usage:
```javascript
parse_user_agent()
```

Expected output:
```json
{
  "ua": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/137.0.0.0 Safari/537.36",
  "browser": {
    "name": "Chrome",
    "version": "137.0.0.0",
    "major": "137",
    "language": "it-IT"
  },
  "engine": {
    "name": "Blink",
    "version": "137.0.0.0"
  },
  "os": {
    "name": "Mac OS",
    "version": "10.15.7"
  },
  "device": {
    "vendor": "Apple",
    "type": null,
    "model": "Macintosh"
  },
  "cpu": {
    "architecture": null
  }
}
```



## Format timestamp
Format timestamp into datetime string.

Usage:
```javascript
const timestamp = Date.now()
format_datetime(timestamp)
```

Expected output:
```json
{
  "date": "2025-06-19",
  "date_time": "2025-06-19T13:52:05",
  "date_time_millis": "2025-06-19T13:52:05.420",
  "date_time_micros": "2025-06-19T13:52:05.420000",
  "year": 2025,
  "month": "06",
  "day": "19",
  "hours": "13",
  "minutes": "52",
  "seconds": "05",
  "milliseconds": ".420",
  "microseconds": ".420000"
}
```



## Get channel grouping 
Giving a source and a campaign name, calculate the standard channel grouping of those values.

Usage:
```javascript
const source = 'facebook'
const campaign_name = 'test'
get_channel_grouping(source, campaign_name)
```

Expected output:
```json
"paid_social"
```


---

Reach me at: [Email](mailto:hello@tommasomoretti.com) | [Website](https://tommasomoretti.com/?utm_source=github.com&utm_medium=referral&utm_campaign=nameless_analytics) | [Twitter](https://twitter.com/tommoretti88) | [Linkedin](https://www.linkedin.com/in/tommasomoretti/)
