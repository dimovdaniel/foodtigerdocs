# Client API

{% api-method method="get" host="https://yourdomain.com" path="/api/user/data" %}
{% api-method-summary %}
Get User Data - Logged user data
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get logged user data.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="api\_token" type="string" required=true %}
The user api token
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "name": "User name",
    "email": "user@email.com",
    "phone": "001122334455"
  }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://yourdomain.com" path="/api/clientgettoken" %}
{% api-method-summary %}
Get Token - Login user via email
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get client token.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-form-data-parameters %}
{% api-method-parameter name="password" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
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
Register - Register user via email
{% endapi-method-summary %}

{% api-method-description %}
This endpoint register new client.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-form-data-parameters %}
{% api-method-parameter name="app\_secret" type="string" required=true %}
The app secret
{% endapi-method-parameter %}

{% api-method-parameter name="phone" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
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

{% api-method method="post" host="https://yourdomain.com" path="/api/client/loginfb" %}
{% api-method-summary %}
Login or register with Facebook
{% endapi-method-summary %}

{% api-method-description %}
Login or register user via Facebook
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-form-data-parameters %}
{% api-method-parameter name="email" type="string" required=true %}
Email
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Name
{% endapi-method-parameter %}

{% api-method-parameter name="phone" type="string" required=true %}
Phone
{% endapi-method-parameter %}

{% api-method-parameter name="app\_secret" type="string" required=true %}
The app secret
{% endapi-method-parameter %}

{% api-method-parameter name="fb\_id" type="string" required=true %}
The Facebook ID
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://yourdomain.com" path="/api/client/logingoogle" %}
{% api-method-summary %}
Login or register via Google
{% endapi-method-summary %}

{% api-method-description %}
Login or register via Google
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-form-data-parameters %}
{% api-method-parameter name="email" type="string" required=true %}
Email
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Name
{% endapi-method-parameter %}

{% api-method-parameter name="phone" type="string" required=true %}
Phone
{% endapi-method-parameter %}

{% api-method-parameter name="google\_id" type="string" required=true %}
The google id
{% endapi-method-parameter %}

{% api-method-parameter name="app\_secret" type="string" required=true %}
The app secret
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
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
{% api-method-query-parameters %}
{% api-method-parameter name="lng" type="string" required=false %}
The longitude of the user
{% endapi-method-parameter %}

{% api-method-parameter name="lat" type="string" required=false %}
The latitude of the user
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

{% api-method method="post" host="https://yourdomain.com" path="/api/app/settings" %}
{% api-method-summary %}
Get settings 
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-form-data-parameters %}
{% api-method-parameter name="app\_secret" type="string" required=true %}
Get app settings
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Get project data, like what kind of payment methods should we show. 
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
{% api-method-form-data-parameters %}
{% api-method-parameter name="timeslot" type="string" required=false %}
The time slot for delivery or pickup
{% endapi-method-parameter %}

{% api-method-parameter name="order\_price" type="number" required=true %}
Total order price with delivery if delivery
{% endapi-method-parameter %}

{% api-method-parameter name="delivery\_method" type="string" required=true %}
delivery or pickup
{% endapi-method-parameter %}

{% api-method-parameter name="stripe\_token" type="string" required=false %}
The stripe payment id method. Required if payment method is stripe.
{% endapi-method-parameter %}

{% api-method-parameter name="payment\_method" type="string" required=true %}
cod \| stripe
{% endapi-method-parameter %}

{% api-method-parameter name="api\_token" type="string" required=true %}
The user api token
{% endapi-method-parameter %}

{% api-method-parameter name="comment" type="string" required=false %}
Comment on order
{% endapi-method-parameter %}

{% api-method-parameter name="restaurant\_id" type="integer" required=true %}
The restaurant id
{% endapi-method-parameter %}

{% api-method-parameter name="address\_id" type="integer" required=true %}
The address id
{% endapi-method-parameter %}

{% api-method-parameter name="items" type="array" required=true %}
The order items ex \[{id:1,qty:1}\]
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
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

{% api-method method="post" host="https://yourdomain.com" path="/api/make/address" %}
{% api-method-summary %}
Make address
{% endapi-method-summary %}

{% api-method-description %}
Makes an address for this user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-form-data-parameters %}
{% api-method-parameter name="api\_token" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="lng" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="lat" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="address" type="string" required=true %}
The address name
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
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

{% api-method method="post" host="https://yourdomain.com" path="/api/delete/address" %}
{% api-method-summary %}
Delete address
{% endapi-method-summary %}

{% api-method-description %}
Delete an address of user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-form-data-parameters %}
{% api-method-parameter name="id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="api\_token" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
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

{% api-method method="get" host="https://yourdomain.com" path="/api/mynotifications" %}
{% api-method-summary %}
Get Notifications
{% endapi-method-summary %}

{% api-method-description %}
Get notifications
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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

