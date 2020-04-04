# Client API

{% api-method method="post" host="https://yourdomain.com" path="/api/clientgettoken" %}
{% api-method-summary %}
Get Token
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get client token.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="email" type="string" required=true %}
Client's email.
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
Client's password.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
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

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://yourdomain.com" path="/api/client/register" %}
{% api-method-summary %}
Register
{% endapi-method-summary %}

{% api-method-description %}
This endpoint register new client.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="email" type="string" required=true %}
Email.
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
Password.
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Full Name.
{% endapi-method-parameter %}

{% api-method-parameter name="phone" type="number" required=true %}
Phone.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
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

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://yourdomain.com" path="/api/restorantslist" %}
{% api-method-summary %}
Get Restaurants
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will retrieve all restaurants.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="api\_token" type="string" required=true %}
The authentication token.
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

{% api-method method="get" host="https://yourdomain.com" path="/api/restorant/{id}/items" %}
{% api-method-summary %}
Get Restaurant Items
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will retrieve restaurant items.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The restaurant id.
{% endapi-method-parameter %}

{% api-method-parameter name="api\_token" type="string" required=true %}
The authentication token.
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

{% api-method method="post" host="https://yourdomain.com" path="/api/make/order" %}
{% api-method-summary %}
Make order
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will make new order.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="items" type="array" required=true %}
Items array.
{% endapi-method-parameter %}

{% api-method-parameter name="addressID" type="integer" required=true %}
Address ID.
{% endapi-method-parameter %}

{% api-method-parameter name="restID" type="integer" required=true %}
Restaurant ID.
{% endapi-method-parameter %}

{% api-method-parameter name="deliveryPrice" type="string" required=true %}
Delivery price.
{% endapi-method-parameter %}

{% api-method-parameter name="orderPrice" type="string" required=true %}
Order price.
{% endapi-method-parameter %}

{% api-method-parameter name="comment" type="string" required=true %}
Comment.
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

{% api-method method="get" host="https://yourdomain.com" path="/api/myorders" %}
{% api-method-summary %}
My Orders
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will retrieve client orders.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="api\_token" type="string" required=true %}
The authentication token.
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

{% api-method method="get" host="https://yourdomain.com" path="/api/myaddresses" %}
{% api-method-summary %}
My Addresses
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will retrieve client addresses.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="api\_token" type="string" required=true %}
The authentication token.
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

