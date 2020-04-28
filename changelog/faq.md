# FAQ

## How customer can register?

They can register via email with password. They can also register via Facebook and Google login. At the moment there is no [phone verification](https://trello.com/c/3aBr8Iay/61-phone-verification-when-user-registers).  

## After order is paid, where money goes. 

At the moment we have **Cash On Delivery** and **Stripe** card payments.

 With **COD**, the money are collected by the driver. And it us to you how you will manage the payments to the restaurants. The system can calculate static and/or percentage based fee that you can export and make calculations.  
  
With **Stripe Card** payments, money goes to you as admin/owner of the project. And it us to you how you will manage the payments to the restaurants. The system can calculate static and/or percentage based fee that you can export and make calculations.  
  
Soon we will integrate [Stripe Connect ](https://trello.com/c/NNeTIodn/19-stripe-connect-payments)payments where on your account will stay the money for the fee + delivery and the money will go directly to the restaurants automatically. 

## How restaurants owner registers.

At the moment, you should create [TypeForm](https://www.typeform.com/) form and put it in the settings. The interested restaurants will fill the form, and you get the submitted responses. If response looks ok, the administrator creates restaurant + account for that restaurant.   
  
The restaurant owner will need to reset the password \( it is unknown on the process of creation \) and start filling the items / categories for his restaurant. 

## Who can order, are the area / radius limitations?

Any registered client. At the moment, we don't have the functionality to limit the ordering based on client are. But you can[ vote for it.](https://trello.com/c/CPMufGvy/34-add-the-delivery-radius-at-the-restaurant) It is in our todo.  

## Once order arrives, what is the flow?

1. Client makes order  - JUST\_CREATED
2. Admin approves  - APPROVED\_BY\_ADMIN &lt;-- This can be automated  
3. Restaurant approves  - APPROVED\_BY\_RESTAURANT
4. Admin assigns to driver  - ASSIGNED\_TO\_DRIVER
5. Restaurant says they did the order - PREPARED
6. Driver pick ups  - PICKED\_UP
7. Driver delivers - DELIVERED
8. Admin can reject - REJECTED\_BY\_ADMIN
9. Restaurant can reject - REJECTED\_BY\_RESTAURANT 

Please look into our environment variables, we have few settings how this can work.    
For example if you put APP\_ALLOW\_SELF\_DELIVER - restaurants can deliver orders on their own.

## How does driver process works.

Drivers are employees to the project owner. They are created by the admin. After they are created, admin can assign jobs / orders to them. They can do the work via the Web Version, but in order to have the location of order tracking, drivers will need to use the [Driver Companion App](https://codecanyon.net/item/driver-companion-app-for-foodtiger-delivery/26415042). 

## How is the restaurant notified for new orders.

Soon as there is new order for restaurant. 

1. They will get an email
2. They can see that new order in the "Live orders" section. 

Vote for your desired features

* [SMS](https://trello.com/c/wPhhfQNR/62-sms-on-new-orders)
* [Sound Ring + Web Push Notification](https://trello.com/c/xGpn3ju9/39-add-alarm-sound-when-a-new-order-received-at-owner-backend)

## What languages the site works in?

The site operates in 1 language that can be defined from the .env variable. We have the site translated in

* [x] English
* [x] French
* [x] German
* [x] Spanish
* [ ] Italian
* [ ] Russian
* [ ] Portuguese 

Easy to translate to any language. All strings are in 1 file.

## What technology is used

### WEB \( Storefront and Dashboard \)

* Laravel - PHP Framework
* MySQL Database
* Bootstrap - Based on Argon Design from Creative Tim
* Mobile ready - Both storefront and dashboard

### Driver Mobile app

* React Native with Expo.io - Generates native iPhone and native Android app
* Based on Argon Design with Galio.io

### Customer Mobile app

* React Native with Expo.io - Generates native iPhone and native Android app
* Based on Argon Design with Galio.io





