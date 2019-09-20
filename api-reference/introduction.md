---
description: >-
  Learn how to use our API and build your own custom sitemaps workflow, just the
  way you like to.
---

# Getting Started

## API Authentication

{% hint style="info" %}
**All authorization is done through a single API token.** You can generate and/or revoke an api token at any time. To manage your api tokens, log in to your account and navigate to your settings panel. You'll find the API tab in the left sidebar. Remember to include your bearer token in the **Authorization header** for every API request.
{% endhint %}

```javascript
{ "Authorization": "Bearer: your-secure-bearer-token-here" }
```

## Example with curl

You can use `curl` to do API requests. Here's an example, including the required `Authorization` header.

```bash
API_TOKEN="your-api-token-here";
curl -XGET \
    -H "Authorization: Bearer ${API_TOKEN}" \ # Authenticate with Bearer token
    https://sitemap.sh/api/projects > ./results.json
```

{% hint style="info" %}
Use `json_pp` to beautify JSON output from your command line. [Here's the manpage](http://manpages.ubuntu.com/manpages/disco/man1/json_pp.1.html).
{% endhint %}

#### Beautify JSON output

```bash
echo '[{"key":"value"},{"key2":"value2"}]' | json_pp
```

This should result into the following output.

```javascript
[
   {
      "key" : "value"
   },
   {
      "key2" : "value2"
   }
]
```

