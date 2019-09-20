---
description: >-
  You can create, update, delete and execute sitemap generation through our API,
  for each of your projects.
---

# Projects

{% hint style="info" %}
**All authorization is done through a single api token.** You can generate and/or revoke an api token at any time. To manage your api tokens, log in to your account and navigate to your settings panel. You'll find the API tab in the left sidebar. Remember to include your bearer token in the **Authorization header** for every API request.
{% endhint %}

```javascript
{ "Authorization": "Bearer: your-secure-bearer-token-here" }
```

{% api-method method="get" host="https://sitemap.sh/api" path="/projects/" %}
{% api-method-summary %}
Retrieve all projects
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will provide all the projects you own.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Include your bearer token in the authorization header for every request.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Projects successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
[
  {
    "user_id": 1,
    "key": "ekajd98u12j",
    "name": "example",
    "primary_url": "https:\/\/www.example.com",
    "status": "idle",
    "enabled": 0,
    "processed_at": null,
    "created_at": "yyyy-mm-dd h:m:s",
    "updated_at": "yyyy-mm-dd h:m:s",
    "image_url": "https:\/\/www.gravatar.com\/avatar\/37ffc9301f7b2497941f6b8bdc3904db.jpg?s=200&d=identicon",
    "last_run_date": "yyyy, mmm dd",
    "last_run_time": "m:s",
    "locations": [
      {
        "id": 2,
        "project_id": 1,
        "priority": null,
        "change_frequency": null,
        "last_modification_date": null,
        "type": "exclude",
        "url": "https:\/\/www.example.com\/contact-us",
          "created_at": "created_at",
          "updated_at": "created_at"
        }
      ]
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://sitemap.sh/api" path="/projects/:key" %}
{% api-method-summary %}
Retrieve a project
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will provide a specific endpoint you specify.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
The project key to identify which project we will retrieve.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Project successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
  {
    "user_id": 1,
    "key": "ekajd98u12j",
    "name": "example",
    "primary_url": "https:\/\/www.example.com",
    "status": "idle",
    "enabled": 0,
    "processed_at": null,
    "created_at": "yyyy-mm-dd h:m:s",
    "updated_at": "yyyy-mm-dd h:m:s",
    "image_url": "https:\/\/www.gravatar.com\/avatar\/37ffc9301f7b2497941f6b8bdc3904db.jpg?s=200&d=identicon",
    "last_run_date": "yyyy, mmm dd",
    "last_run_time": "m:s",
    "locations": [
      {
        "id": 2,
        "project_id": 1,
        "priority": null,
        "change_frequency": null,
        "last_modification_date": null,
        "type": "exclude",
        "url": "https:\/\/www.example.com\/contact-us",
          "created_at": "created_at",
          "updated_at": "created_at"
        }
      ]
    }
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{ "message": "Not found" }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://sitemap.sh/api" path="/projects/:key" %}
{% api-method-summary %}
Retrieve locations for a project
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

