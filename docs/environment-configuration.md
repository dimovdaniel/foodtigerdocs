# Environment configuration

All of the configuration variables for the FoodTiger project are stored in the **`.env`** file.

FoodTiger installation, the root directory of your application will contain a **`.env.example`** file. You will need to rename it manually to **`.env`**

  
List of all custom environment variables FoodTiger uses. We will see them one by one.

{% hint style="info" %}
Remove the comments // when you add some environment variable
{% endhint %}

* **Localization**  
* **Ignore subdomains** If your run your site as sub domain, add the sub domain in this variable.

```text
IGNORE_SUBDOMAINS='www.yoursubdomain' 
```

* **Payments** At this moment FoodTiger comes with two methods to make payments: Pay cash on delivery, Pay via Stripe. To enable or disable this methods there are several variables that you will need to configure.  By default the two methods are set to false and to enable you need to change them to true.  **Cash on Delivery** `HIDE_CODE` can be true or false.  **Stripe Gateway  This meth**

  


```text
HIDE_COD=false //Hide or Show Cash on Delivery payment
ENABLE_STRIPE=false //Do you want to use Stripe Payment
STRIPE_KEY="" //Stripe API key
STRIPE_SECRET="" //Stripe API Secret
ENABLE_STRIPE_IDEAL=false //Should we have stripe ideal payment
```





* `adasdasdasdasadsads`
* `as`
* `ads`
* `adsa`
* `aasdas`
* `da`
* `asdasd`
* `asdada`

```text
APP_LOCALE=en // en | fr | de | es
IGNORE_SUBDOMAINS='www' //If you run your site as subdomain, add the subdomain here

HIDE_COD=false //Hide Show Cash on Delivery
ENABLE_STRIPE=false //Do you want to use Stripe Payment
STRIPE_KEY="" //Stripe API key
STRIPE_SECRET="" //Stripe API Secret
ENABLE_STRIPE_IDEAL=false //Should we have stripe ideal payment

DEFAULT_PAYMENT="cod" //Default payment method - Cash On Delivery default cod|stripe
CASHIER_CURRENCY="usd" //usd,eur etc.. 
GOOGLE_MAPS_API_KEY="" //Display google maps

GOOGLE_CLIENT_ID="" //Used for google login
GOOGLE_CLIENT_SECRET="" //Used for go0gle login
GOOGLE_REDIRECT="" //Used for google login

FACEBOOK_CLIENT_ID="" //Used for facebook login
FACEBOOK_CLIENT_SECRET="" //Used for facebook login
FACEBOOK_REDIRECT="" //Used for facebook login

ENABLE_IMPORT_CSV=false //Enable importing restaurants from excel files
APP_ORDER_APPROVE_DIRECTLY=false //No need admin to approve the oorders if true
APP_ALLOW_SELF_DELIVER=true //Restaurants will deliver orders on their selfs


```

