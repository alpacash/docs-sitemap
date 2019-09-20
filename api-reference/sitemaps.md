---
description: >-
  You can list your sitemaps and download the corresponding xml file any time
  through our API.
---

# Sitemaps

{% api-method method="get" host="https://sitemap.sh/api" path="/sitemaps" %}
{% api-method-summary %}
List Sitemaps
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to list your generated sitemap files.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Include your bearer token in this request.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
  "sitemaps": [
    {
      "id": 7,
      "uuid": "ioaci2u83u2re98fd",
      "filename": "mxjdu9i273dc_2019_06_17_15_34_07.xml",
      "project_id": 1,
      "created_at": "yyyy-mm-dd h:m:s",
      "updated_at": "yyyy-mm-dd h:m:s",
      "project": {
        // The project details, including locations
      }
    }
  ]  
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://sitemap.sh/api" path="/:uuid" %}
{% api-method-summary %}
Download a Sitemap
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will provide the XML contents of a specific sitemap file. You can then store it in your local web directory and proceed to send it to the search engines.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="uuid" type="string" required=true %}
The uuid to identify the specific sitemap you want to download.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```markup
<?xml version="1.0" encoding="UTF-8"?>
<urlset
  xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
  xmlns:xhtml="http://www.w3.org/1999/xhtml">
  <url>
    <loc>https://www.example.com/</loc>
    <lastmod>2019-06-17T15:33:47+00:00</lastmod>
    <changefreq>daily</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://www.example.com/contact-us</loc>
    <lastmod>2019-06-17T15:33:47+00:00</lastmod>
    <changefreq>daily</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://www.example.com/knowledgebase</loc>
    <lastmod>2019-06-17T15:33:47+00:00</lastmod>
    <changefreq>daily</changefreq>
    <priority>0.8</priority>
  </url>
</urlset>

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

