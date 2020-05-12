# Environment configuration

All of the configuration variables for the FoodTiger project are stored in the **`.env`** file.

FoodTiger installation, the root directory of your application will contain a **`.env.example`** file. You will need to rename it manually to **`.env`**

  
List of all custom environment variables FoodTiger uses. We will see them one by one.

{% hint style="info" %}
Remove the comments // when you add some environment variable
{% endhint %}

### **1. Localization** 

{% page-ref page="../define-basics/localization.md" %}

### **2. Mail server**

{% page-ref page="../define-basics/obtain-smtp.md" %}

### **3. Payments**

{% page-ref page="../define-basics/payments.md" %}

### 4. Google Maps

{% page-ref page="../define-basics/google-maps.md" %}

### 5. Google authentication

{% page-ref page="../define-basics/google-authentication.md" %}

### 6. Facebook authentication

{% page-ref page="../define-basics/facebook.md" %}

### 8. Subdomain

When you run your site in subdomain, you need to declare that subdomain in your .env file. This is needed to be clarified, since this project can be used with subdomains for each restaurant.

```text
IGNORE_SUBDOMAINS="www,yoursubdomain,anothersubdomain"
```

### 9. Import from CSV

Enable importing data from Excel files.

{% page-ref page="../define-basics/import-from-csv.md" %}

### 10. Additional variables

There are also few variables that for now only we will mentioned and later we will explain more about them.

* Working with excel files  
  
  FoodTiger also support integration and working with excel files. By default is set to **false** and if you want to enable change it to **true**.

  ```text
  ENABLE_IMPORT_CSV=false //Enable importing restaurants from excel files
  ```

* Automatically approving the orders  
  
  No need admin to aprove the orders if **true**. By default is set to **false**.

  ```text
  APP_ORDER_APPROVE_DIRECTLY=false //No need admin to approve the oorders if true
  ```

* Restaurants will deliver orders on their self's

  ```text
  APP_ALLOW_SELF_DELIVER=true //Restaurants will deliver orders on their selfs
  ```

  
  
  In the end you should have a list of variables like the list below.

## Full list of supported environment variables

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
GOOGLE_MAPS_GEOCODING_API_KEY="" //Geocoding enabled API KEY

GOOGLE_CLIENT_ID="" //Used for google login
GOOGLE_CLIENT_SECRET="" //Used for go0gle login
GOOGLE_REDIRECT="" //Used for google login

FACEBOOK_CLIENT_ID="" //Used for facebook login
FACEBOOK_CLIENT_SECRET="" //Used for facebook login
FACEBOOK_REDIRECT="" //Used for facebook login

ENABLE_IMPORT_CSV=false //Enable importing restaurants from excel files
APP_ORDER_APPROVE_DIRECTLY=false //No need admin to approve the oorders if true
APP_ALLOW_SELF_DELIVER=true //Restaurants will deliver orders on their selfs

ENABLE_PICKUP=true //Do we have the option client to make PICKUP
GOOGLE_ANALYTICS="" //Google Analytcis code

URL_ROUTE="restaurant" //URL route on frontend
```

