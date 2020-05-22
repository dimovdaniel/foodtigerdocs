---
description: Frequently Asked Questions (FAQs)
---

# FAQ

## How customer can register?

They can register via email with password. They can also register via Facebook and Google login. At the moment there is no [phone verification](https://trello.com/c/3aBr8Iay/61-phone-verification-when-user-registers).  

## After order is paid, where money goes?

At the moment we have **Cash On Delivery** and **Stripe** card payments.

With **COD**, the money are collected by the driver. And it us to you how you will manage the payments to the restaurants. The system can calculate static and/or percentage based fee that you can export and make calculations.  
  
With **Stripe Card** payments, money goes to you as admin/owner of the project. And it us to you how you will manage the payments to the restaurants. The system can calculate static and/or percentage based fee that you can export and make calculations.  
  
Soon we will integrate [Stripe Connect ](https://trello.com/c/NNeTIodn/19-stripe-connect-payments)payments where on your account will stay the money for the fee + delivery and the money will go directly to the restaurants automatically. 

## How restaurants owner registers?

At the fronted part of the script you will find the button **Register your restaurant**. The interested restaurants will fill the form, and you get the submitted responses. If response looks okay, the administrator accept the restaurant and account for that restaurant. After acceptance the restaurant owner receives email with details.   
  
The restaurant owner will need to login with the email and password \(generated password can change if he wants in profile page\). After that the owner can start filling the items / categories for his restaurant. 

## Who can order, are the area / radius limitations?

Any registered client. At the moment, we don't have the functionality to limit the ordering based on client are. But you can[ vote for it.](https://trello.com/c/CPMufGvy/34-add-the-delivery-radius-at-the-restaurant) It is in our to-do list.  

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

## How does driver process works?

Drivers are employees to the project owner. They are created by the admin. After they are created, admin can assign jobs / orders to them. They can do the work via the Web Version, but in order to have the location of order tracking, drivers will need to use the [Driver Companion App](https://codecanyon.net/item/driver-companion-app-for-foodtiger-delivery/26415042). 

## How is the restaurant notified for new orders?

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
* [x] Italian
* [x] Russian
* [x] Portuguese 

Easy to translate to any language. All strings are in 1 file.

## What are static and dynamic fee commissions?

The project owner will have two options to get money from the restaurants for using the site services.

* Calculate static - fixed commission on the order.
* Calculate dynamic - percent based commission on the order.

This commissions are visible only for the admin in every restaurant. It's recommended to use only one of the options not both. This fees are not related to the total cost of the client.

**How it works?**

* Calculate static fee - For example if the static fee is 5$ for that restaurant the fee for the orders from that orders will be also 5$.
* Calculate dynamic fee - For example if we have order with total price of 45$ and the fee percent is 5% for that restaurant, the order fee will be 2.25$.

## What technology is used?

### WEB \( Storefront and Dashboard \)

* Laravel - PHP Framework
* MySQL Database
* Bootstrap - Based on Argon Design from Creative Tim
* VUE JS
* Mobile ready - Both storefront and dashboard



### Driver Mobile app

* React Native with Expo.io - Generates native iPhone and native Android app
* Based on Argon Design with Galio.io

### Customer Mobile app

* React Native with Expo.io - Generates native iPhone and native Android app
* Based on Argon Design with Galio.io

## How to add new admin?

We have add the task - Admins to be able to add new admins from the interface. So it is not yet available

But here are the steps to do it now. 

1. Register new client. 
2. Go in the database yourdomain.com/adminer and login
3. Get the ID of the user from **users** table
4. Go in **model\_has\_roles** table. There you should find that id  have **role\_id** 4. 
5. Change it to **role\_id** 1

Now he is admin.

## How to add new address?

The option for adding new address from version 1.2 is moved in the order checkout page. When the clients is making new order he can see all his addresses with option to add new one.

This option is using Google Places API and you will need to add it in your configuration otherwise this option will be not functional. More about it [here](https://app.gitbook.com/@mobidonia/s/mresto/~/drafts/-M7w7cOY35j6djVuexqR/define-basics/places-api).

## How to delete the demo data?

To delete the demo data go to your site Adminer. \(Adminer is php script to manage your database\).  
The Adminer is located on **yourdomain.com/adminer**

There, login with your database username and password.   
Click on the SQL command icon \( [Image](https://i.imgur.com/GXetB8K.png) \)

In the text area enter the following sql command. After executing [THIS](https://gist.github.com/dimovdaniel/ebbaa2bb379e92bfc1e223b306ca1531) commands, only your admin user will remain in the database.







