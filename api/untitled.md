# Driver API

{% api-method method="post" host="https://yourdomain.com" path="/api/drivergettoken/" %}
{% api-method-summary %}
Get Token
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get driver token
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="email" type="string" required=true %}
Driver's emaiil
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
Driver's password
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```text
{
    "status": true,
    "token": "THE_TOKEN",
    "id": 3
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://yourdomain.com" path="/api/driverorders" %}
{% api-method-summary %}
Get orders
{% endapi-method-summary %}

{% api-method-description %}
Get today's orders
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="api\_token" type="string" required=false %}
The authentication token
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://yourdomain.com" path="/api/updateorderstatus/:order\_id/:status\_id" %}
{% api-method-summary %}
Order Update
{% endapi-method-summary %}

{% api-method-description %}
Update order status
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name=":status\_id" type="string" required=true %}
the status id
{% endapi-method-parameter %}

{% api-method-parameter name=":order\_id" type="string" required=true %}
the order id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="comment" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="api\_token" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://yourdomain.com" path="/api/updateorderlocation/:order\_id/:lat/:lng" %}
{% api-method-summary %}
Update location of order 
{% endapi-method-summary %}

{% api-method-description %}
Updates order location  
Since v1.1
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="lng" type="string" required=false %}
lng
{% endapi-method-parameter %}

{% api-method-parameter name="lat" type="string" required=false %}
lat
{% endapi-method-parameter %}

{% api-method-parameter name="order\_id" type="number" required=true %}
the order id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="api\_token" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
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

