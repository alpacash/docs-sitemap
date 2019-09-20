---
description: You can manage your additional location rules through our API.
---

# Locations

{% api-method method="delete" host="https://sitemap.sh/api" path="/locations/:location-id" %}
{% api-method-summary %}
Delete an additional location rule
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to delete an existing additional location by it's ID.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="location-id" type="string" %}
The id of the location you want to delete.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Include your bearer token in order to authenticate for this request.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully deleted.
{% endapi-method-response-example-description %}

```javascript
{ "message": "Successfully deleted." }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



