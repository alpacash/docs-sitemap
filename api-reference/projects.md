---
description: >-
  You can create, update, delete and execute sitemap generation through our API,
  for each of your projects.
---

# Projects

{% api-method method="get" host="https://sitemap.sh/api" path="/projects/:key" %}
{% api-method-summary %}
Retrieve a project
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will provide a specific project you specify.
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

{% api-method method="get" host="https://sitemap.sh/api" path="/projects" %}
{% api-method-summary %}
Retrieve all projects
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will provide all the projects you own.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

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

{% api-method method="get" host="https://sitemap.sh/api" path="/projects/:key/locations" %}
{% api-method-summary %}
Retrieve locations for a project
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will provide the locations for a specific endpoint you specify. These are included in the `/projects/:key` request as well, but a separate endpoint for the locations may come in handy.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
The project key to identify the project.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Project's locations successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
[
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
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://sitemap.sh/api" path="/projects/:key" %}
{% api-method-summary %}
Create a project
{% endapi-method-summary %}

{% api-method-description %}
You can create a new project through this endpoint.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
The key to identify your project.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="primary\_url" type="string" required=true %}
The primary URL for your project, which we will use to crawl your site for URL's to add to your sitemap.
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
The name for your new project.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully created a new project.
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://sitemap.sh/api" path="/projects/:key" %}
{% api-method-summary %}
Update a project
{% endapi-method-summary %}

{% api-method-description %}
You can update an existing project through this endpoint. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
The key to identify the project you want to update.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="locations" type="array" required=false %}
Your project's locations.
{% endapi-method-parameter %}

{% api-method-parameter name="primary\_url" type="string" required=false %}
Your project's primary url.
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
Your project's name.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully updated your project.
{% endapi-method-response-example-description %}

```javascript
{ "message": "Successfully updated" }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://sitemap.sh/api" path="/projects/:key/locations" %}
{% api-method-summary %}
Update a project's locations
{% endapi-method-summary %}

{% api-method-description %}
You can update an existing project's locations
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
The key used to identify your project.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="locations" type="array" required=true %}
Your new locations. Use the same format they appear in for retrieving locations.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully updated the specified project's locations.
{% endapi-method-response-example-description %}

```javascript
{ "message": "Successfully updated" }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://sitemap.sh/api" path="/projects/:key/process" %}
{% api-method-summary %}
Generate the sitemap for a project
{% endapi-method-summary %}

{% api-method-description %}
Start generating a fresh sitemap file, which you can download later on.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
The key to identify your project.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
The process is queued and will generate your sitemap shortly. Use the provided job id to request it's status.
{% endapi-method-response-example-description %}

```javascript
{ "message": "Successfully queued", "job_id": "your-job-id" }
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}
This project is currently busy, probably generating a sitemap. Use the provided job id to request it's status.
{% endapi-method-response-example-description %}

```javascript
{ "message": "Project state conflicts", "job_id": "your-job-id" }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

