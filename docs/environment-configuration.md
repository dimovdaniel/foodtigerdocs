# Environment configuration

All of the configuration variables for the FoodTiger project are stored in the **`.env`** file.

FoodTiger installation, the root directory of your application will contain a **`.env.example`** file. You will need to rename it manually to **`.env`**

  
List of all custom environment variables FoodTiger uses. We will see them one by one.

{% hint style="info" %}
Remove the comments // when you add some environment variable
{% endhint %}

### **1. Database**

{% page-ref page="../define-basics/database.md" %}

### **2. Mail server**

{% page-ref page="../define-basics/obtain-smtp.md" %}

### **4. Localization and Time format**

{% page-ref page="../define-basics/localization.md" %}

### **5. Payments**

{% page-ref page="../define-basics/payments.md" %}

### 6. Google Maps and Places API

{% page-ref page="../define-basics/google-api.md" %}

### 7. Google Analytics

From version 1.2 we enable tracks and reports website traffic using Google Analytics. This is optionally and if you want to enable on your site you need to create Google Analytics code.

{% page-ref page="../define-basics/google-analytics.md" %}

### 8. Google authentication

{% page-ref page="../define-basics/google-authentication.md" %}

### 9. Facebook authentication

{% page-ref page="../define-basics/facebook.md" %}

### 10. One Signal Push notifications

{% page-ref page="../define-basics/one-signal-push-notifications.md" %}

### 11. Subdomain

When you run your site in subdomain, you need to declare that subdomain in your .env file. This is needed to be clarified, since this project can be used with subdomains for each restaurant.

```text
IGNORE_SUBDOMAINS="www,yoursubdomain,anothersubdomain"
```

### 12. Import from CSV

FoodTiger also support integration and working with excel files. 

{% page-ref page="../define-basics/import-from-csv.md" %}

### 13. Additional variables

There are also few variables that for now only we will mentioned and later we will explain more about them.    

* Automatically approving the orders  No need admin to approve the orders if **true**. By default is set to **false**.

```
APP_ORDER_APPROVE_DIRECTLY=false //No need admin to approve the oorders if true
```



* Restaurants will deliver orders on their self's

```text
APP_ALLOW_SELF_DELIVER=true //Restaurants will deliver orders on their selfs
```



* Option for adding/deleting demo data in your project

  
  If you want to skip the adding the demo data that you will find on the [demo version](https://foodtiger.site/) you can make that with adding variable in the configuration.

```text
DEMO_DATA=false //By default it's true, if false the data won't be added
```

       Additionally if you add the demo data in the process of installation later you can delete manually but   
       maybe you will have some conflicts during this process.   
        
       You can find about it on the following [link](https://mobidonia.gitbook.io/mresto/changelog/faq#how-to-delete-the-demo-data).  


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

GOOGLE_MAPS_API_KEY="" //Uses Google Maps and Places API
ENABLE_LOCATION_SEARCH=false // if true, will enable the delivery area search

GOOGLE_ANALYTICS="" //Google Analytcis code

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


URL_ROUTE="restaurant" //URL route on frontend

ONESIGNAL_APP_ID="" //Onesignal app id
ONESIGNAL_REST_API_KEY="" //Onesignal rest api key 

DEMO_DATA=false //Enable od disable demo data
TIME_FORMAT="24hours" //Display time 24hours or AM/PM
DATETIME_DISPLAY_FORMAT="d M Y H:i" // "d M Y H:i" -is for 24h  "d M Y h:i A" is for am/pm  - Look for carbon format

ONESIGNAL_APP_ID= //One Signal App Id 
ONESIGNAL_REST_API_KEY= //One Signal Rest Api Key

APP_SECRET="" //String use to secure your Client Mobile API - can be any string

MAIL_DRIVER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null

MAIL_FROM_ADDRESS=''
MAIL_FROM_NAME=''

SINGLE_MODE=false //If true, the site will open open single restaurant
SINGLE_MODE_ID=1 //Single Restaurant mode id

TWILIO_ACCOUNT_SID=SID
TWILIO_AUTH_TOKEN=TOKEN
TWILIO_FROM="NUMBER"
SEND_SMS_NOTIFICATIONS=false

TIME_ZONE=UTC
```

