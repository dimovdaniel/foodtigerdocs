# Changelog

## 1.3 - 2020-05-28

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
  
You should also add OneSignal keys  in [environment variable](https://mobidonia.gitbook.io/mresto/docs/environment-configuration)  to have functional web push notification.

```text
ONESIGNAL_APP_ID="" //Onesignal app id
ONESIGNAL_REST_API_KEY="" //Onesignal rest api key 
```



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



