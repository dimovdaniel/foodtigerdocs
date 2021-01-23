---
description: Frequently Asked Questions (FAQs)
---

# FAQ

## Registration is not working.

This is one of the most common problem. It happens because SMTP is not correctly set up, or not setup at all. To learn how to set it up, follow this guide

{% page-ref page="../define-basics/obtain-smtp.md" %}

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

In the text area enter the following sql command. 

```text
DELETE from order_has_status where order_id<601;
DELETE from orders where id<601;
DELETE FROM address where id<6;
DELETE FROM items where id<256;
DELETE FROM categories where id<52;
DELETE FROM hours where restorant_id<13;
DELETE FROM model_has_roles where model_id<6 and model_id>1;
DELETE FROM restorants where id<13;
DELETE FROM users where id<6 and id>1;
```

{% hint style="danger" %}
After executing the commands, only your admin user will remain in the database.
{% endhint %}

## Best image sizes

* Project logo \( 487x144 \)
* Logo restaurant \( 600x600 \)
* Item image \( 600x600 \) 

## Update problems

### Error on update 500

**Problem**: When you click on the update button, you get blank screen with error 500. 

**Cause**: This mostly happens because there is not enough memory available. You can check "Error" pages in cPanel to confirm

**Solution**: 
Go to you cPanel
There find the tool "MultiPHP INI Editor"
Select the project
memory_limit put to 512M
This should bee enough
Then try to update again


### Error on update 503

**Problem**: After an update, some users experience error 503 \| Service not found.

**Cause**: This mostly happens because your PHP setup doesn't have the ZIP extension enabled. 

**Solution**: 

You will need to enable the ZIP extension 

This is the best and simplest guide we could find on how to enable the ZIP extension in cPanel

{% embed url="https://bobcares.com/blog/enable-php-zip-extension-cpanel/" %}

Also, please talk with your hosting provider on how to enable the zip extension for you.

## Error 500

**Problem**  
You get a white screen with Error 500 on it 

**Reason**  
This is a general error, meaning something wrong happened in the system. And it can be from different causes. it can be a bug or misconfiguration. 

**Solution**  
First, we need to see why this error happens,   
Enable debug mode, so you can see what is behind the 500 error. To do that

1. Login as admin
2. Go In **Setting**
3. Select **Setup** tab
4. Select **APP\_DEBUG**

Then try to reproduce the problem. Now, you will see a lot more information about the problem. If you do understand the message, you get, you may fix the problem on your own. Some common ones are SMTP are Stripe Misconfiguration. For these ones you may try to fix on your own, by going in settings to check if what you have entered is correct. 

For some other reported errors, don't hesitate to contact us with a screenshot of the problem \( including the address bar link \) here [https://help.mobidonia.com/](https://help.mobidonia.com)

## Error 500 on migrating languages

**Problem**  
Before, 2.0.8 if you try to migrate language you can get error 500. 
And some of the item like the categories, can be translated multiple times like ```text{en:\\\en:\\\......}```

**Reason**  
This happens because we didn't look into object active status.
And script crashed when it tried to translate un-active record.

**Solution**  
Update to 2.0.8+
For the ```text{en:\\\en:\\\......}```, if you don't have lot of data, you can manually edit them from the admin.
If you have lot of data, 
- Export the categories and items table
- Find replace, so it looks normal
- Delete categories and items by ignoring foreign keys and import again
Or ask for help from us. 

Then make the translation migration again. Now should go fine. 



## SQL Error - Table not found

**Error**   
After installation, when you open your site, you see an error screen with a report similar to this.

```text
local.ERROR: SQLSTATE[42S22]: Column not found: 1054 Unknown column 'plan.plan_id' 
```

**Reason**  
The most common problem for this is because you have entered the wrong credentials/user/pass for the Database and the setup of the database was incomplete. 

**Solution**

1. Open the file **.env** and make sure you have entered the correct  DB data
2. Remove file storage/installed
3. Try to install again by visiting yourdomain.com/install

If that doesn't help, please create a ticket, and if you can share cPanel / Admin details with us so we can look into the problem. 



## Error on uploading an image 

**Error**

"PHP Fileinfo extension must be installed

**Reason**  
 "PHP Fileinfo extension must be installed/enabled to use Intervention Image."

The project needs the [fileinfo](https://i.stack.imgur.com/vhN3E.png) extension. 

**Solution**

As you can see on the [image](https://i.stack.imgur.com/vhN3E.png), it can be enabled from PHP Selector. But if there is no  PHP Selector you should have access to **WHM**.

**IN WHM**

Initially, we login to WHM and navigate as follows,

Software &gt;&gt; EasyApache 4 &gt;&gt; Customize &gt;&gt; PHP extensions.

Here we search for **fileinfo** and enable phpx.x-php-fileinfo for all versions. Finally, we click on Review and Provision.

This enables the file extension for all the PHP websites in the server.

Let me know about this.









