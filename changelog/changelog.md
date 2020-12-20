# Changelog

## 1.9.7 - 2020-12-17 

This is a combined update from 1.8.0 to 1.9.7

### Fixes

* Variant selection bug fix
* Plus button in the cart was not showing on mobile
* Updated menus privileges on the front end
* Delete user when an admin deletes restaurant
* Admin order accepting 
* Checkbox when placing an order to accept T&S
* Sound on pusher notification
* Category delete when there are no items
* Thank you page after successful payment
* Fixes for Paystack
* Fixes on saving the delivery area

### Updating

To update from the previous release, follow the [standard update procedure](https://mobidonia.gitbook.io/mresto/changelog/updating-shared-hosting). 

After that, log in as admin 

## 1.5.0 - 2020-09-14

### Added

* [TOP REQUESTED](https://trello.com/c/ok5MuZcH/27-set-the-cost-per-distance-for-delivery): Cost per distance of deliver
* [TOP REQUESTED](https://trello.com/c/V0Og1dtP/43-restaurant-and-food-reviews): Reviews
* [TOP REQUESTED](https://trello.com/c/jX4YW7Tr/46-multi-city-version-like-food-panda): Multi city version
* [TOP REQUESTED](https://trello.com/c/NNeTIodn/19-stripe-connect-payments): Stripe connect payments
* [TOP REQUESTED](https://trello.com/c/nV0KgtiG/48-item-variants): Item variants
* PWA
* Welcome email
* Minimal orders
* Paystack payment gateway
* Link to categories
* New finances dashboard
* VAT reports
* Restaurant details on click  and more info on restaurant page

### Updating

To update from previous release, follow the [standard update procedure](https://mobidonia.gitbook.io/mresto/changelog/updating-shared-hosting). 

After that, login as admin 

### Enable Features from this update

#### Enable Cost per distance

In your env editor add this two new variables

```text
ENABLE_COST_PER_DISTANCE=true
COST_PER_KILOMETER=1
```

#### Enable Multi city

In your env editor add this  new variable

```text
MULTI_CITY=true
```

#### Enable stripe connect

In your env editor add this new variable

```text
ENABLE_STRIPE_CONNECT=true
```

#### Enable Paystack

[Here](https://mobidonia.gitbook.io/mresto/define-basics/paystack-gateway) is the article for enabling Paystack payment gateway.

In your env editor add this new variable

```text
PAYSTACK_PUBLIC_KEY=""
PAYSTACK_SECRET_KEY=""
ENABLE_PAYSTACK=false
MERCHANT_EMAIL=""
PAYSTACK_PAYMENT_URL=https://api.paystack.co
```

## 1.4.0 - 2020-07-29 \( [video](https://www.loom.com/share/5c1791ec6614466f838008f98435fb07) \)

### Added

* [TOP REQUESTED](https://trello.com/c/VdsFiwma): Item extras
* [TOP REQUESTED](https://trello.com/c/CPMufGvy): Delivery radius
* [TOP REQUESTED](https://trello.com/c/zJPWWd3N): Nearby restaurant search
* [TOP REQUESTED](https://trello.com/c/wPhhfQNR): SMS on new orders
* [TOP REQUESTED](https://trello.com/c/qJTcLgNg): Results based on distance
* Single Restaurant mode
* .env Editor for admin
* Featured restaurants

### Updating

To update from previous release, follow the [standard update procedure](https://mobidonia.gitbook.io/mresto/changelog/updating-shared-hosting). 

After that, login as admin 

#### SMS notifications

To enable **SMS notifications**,  create [Twilio](https://www.twilio.com/) account and add the following ENV variables. You can now use the .env editor from your admin panel. 

[Here](https://mobidonia.gitbook.io/mresto/define-basics/twilio-sms-notifications) is the article for enabling SMS nofitications.

```text
TWILIO_ACCOUNT_SID=SID
TWILIO_AUTH_TOKEN=TOKEN
TWILIO_FROM="NUMBER"
SEND_SMS_NOTIFICATIONS=true
```

#### Location based search

To enable **location based search** change set .env variable ENABLE\_LOCATION\_SEARCH to true. You will also need to login to you google cloud project and enable [GEO Coding](https://developers.google.com/maps/documentation/geocoding/start) api for your key.  
  
[Here](https://app.gitbook.com/@mobidonia/s/mresto/define-basics/google-api) you can check updated version for enabling Geocoding API based on the previous used APIs

```text
ENABLE_LOCATION_SEARCH=true
GOOGLE_MAPS_GEOCODING_API_KEY="" //your API Key
```

{% hint style="danger" %}
Location based search takes into account the restaurant delivery area. So before enabling it, make sure restaurants had setup the delivery area. 
{% endhint %}

## 1.3.2 - 2020-06-11

### Fixed

* Live orders incorrect order date
* Status update permissions

### Updating 

To update from previous release, follow the [standard update procedure](https://mobidonia.gitbook.io/mresto/changelog/updating-shared-hosting). 

Note that this is minor update, so you don't have to update **vendor** and **node\_modules** folder.  
If you are updating from version 1.3.1 you can just update this files from the updated code  


* app/Http/Controllers/OrderController.php
* config/app.php

## 1.3.1 - 2020-06-09

### Added

* After driver is created,  email is sent with the credentials info
* Order information for address details
* Show version of the code

### Fixed

* Restaurant categories and items show
* Order checkout 
* Items price conversion in menu 
* Translations
* Orders status check 
* Search improvements/ fixes
* Response for no addresses for mobile app

### **Updating**

To update from previous release, follow the [standard update procedure](https://mobidonia.gitbook.io/mresto/changelog/updating-shared-hosting). 

Note that this is minor update, so you don't have to update **vendor** and **node\_modules** folder

## 1.3 - 2020-05-29

### Added

* [TOP REQUESTED](https://trello.com/c/xGpn3ju9): Alarm sound on new order - [Video](https://www.loom.com/share/296835747f7d43898a1c32e2d488e913)
* Web Push notification on order  - Powered by [OneSignal](https://onesignal.com)
* Customer Mobile app \( [separate project ](https://codecanyon.net/item/food-delivery-reactnative-foodtiger/26796029)\)

### Changed 

* Improved search
* Option to disable import of demo data
* CKEditor more options
* More statistics on Dashboard
* Improved restaurant adding
* Mobile browser improvements

### Fixed

* Missing option to modify restaurant address
* More robust order creation
* Payment status not updating 

### Updating

To update from previous release, follow the [standard update procedure](https://mobidonia.gitbook.io/mresto/changelog/updating-shared-hosting).   
  
You should also add One Signal keys in [environment variable](https://mobidonia.gitbook.io/mresto/docs/environment-configuration) to have functional web push notification.  
You can find more [here](https://mobidonia.gitbook.io/mresto/define-basics/one-signal-push-notifications) about the setup for One Signal.

```text
ONESIGNAL_APP_ID="" //Onesignal app id
ONESIGNAL_REST_API_KEY="" //Onesignal rest api key 
```

Also from this version we made a changes on the Google Maps and Places API.

Until this versions we have two different configurations for these API's and now it's more simple.

You can check [here](https://mobidonia.gitbook.io/mresto/define-basics/google-maps-and-places-api-version-1.3) more about it.

## 1.2 - 2020-05-12

### Added

* [TOP REQUESTED](https://trello.com/b/QqLlZCxM/foodtiger): Pickup option
* [TOP REQUESTED](https://trello.com/b/QqLlZCxM/foodtiger): Restaurant closing and opening time
* [TOP REQUESTED](https://trello.com/b/QqLlZCxM/foodtiger): Register restaurant on site, later approve it
* [TOP REQUESTED:](https://trello.com/b/QqLlZCxM/foodtiger) Time slots on order
* Set availability of items
* Calculate static - fixed commission on the order
* Calculate dynamic - percent based commission on the order
* Google Analytics
* Italian, Portuguese, Russian languages added

### Changed

* Dynamic url structure for restaurants
* Improved app sections - modify/show from admin
* Complete checkout redesign
* Improved address entering

### Fixed

* Long description not visible
* Better import via CSV
* Better search
* Error on entering price - always was step 1
* Error on map on restaurant 
* Description with special characters and new lines
* Able to add html characters on front welcome message
* Side cart was not mobile ready
* Adding categories in restaurant as admin
* Multiple orders created
* Multiple address created

### Updating

To update from previous release, follow the [standard update procedure](https://mobidonia.gitbook.io/mresto/changelog/updating-shared-hosting). 

After that, login as admin or notify your restaurant owners that they have to set working times.  
You should also add Google Places Enabled API key in [environment variable](https://mobidonia.gitbook.io/mresto/docs/environment-configuration)  to have functional address entering.

```text
GOOGLE_MAPS_GEOCODING_API_KEY
```

## 1.1 - 2020-04-16

### Added

* Languages en \| es \| de \| fr
* Subdomains ex restaurantname.yoursite.com
* Stripe Payments
* Live orders - Kanban style view in realtime
* Track order on Map \( updated from driver companion app \)
* Reporting - Export orders in excel
*  Social login with Facebook and Google
* Admin can modify restaurant items

### Changed

* Currency is not set in .env
* Google Maps key in .env

## 1.0 - 2020-04-09

### Initial Version



