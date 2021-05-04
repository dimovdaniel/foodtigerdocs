---
description: Learn how to setup the thermal WebHooks Module
---

# WebHooks

### Install

After you have downloaded the code from CodeCanyon, log in to your admin panel as admin and go to the "Apps" section. there is an "Add" button where you can upload the zip file you got from CodeCanyon.

{% page-ref page="how-to-install-plugin.md" %}

### Setup as project admin

After the module is installed, if you go to "Settings-&gt;Apps" you will see the "WebHooks" section. 

![](https://i.imgur.com/HEbpUw3.png)

WebHooks is a link or an API endpoint that accepts POST call with data for the order being made. 

You can set WebHook when the order is approved by the admin \( system \) or by the vendor. 

You can connect with tools like [integromat](https://www.integromat.com/) or [zappier](https://zapier.com/) and connect the project with some of their connections.  

You or your developer can make a custom API that will receive this data and extend the system without modifying any of the code of the project.

### Setup as vendor

When vendors log in, they can go to "Restaurant-&gt;Apps-&gt;WebHooks"

![](https://i.imgur.com/LlNLeQ8.png)

WebHooks is a link or an API endpoint that accepts POST call with data for the order being made. 

Vendors can set WebHook when the order is approved by the admin \( system \) or by themself. 

They can connect with tools like [integromat](https://www.integromat.com/) or [zappier](https://zapier.com/) and connect the project with some of their connections.  

A developer can make a custom API that will receive this data and extend the system without modifying any of the code of the project.

### Video

{% embed url="https://www.youtube.com/watch?v=5bl9TZP2GBY" %}





### Demo

In order to experience the demo, and test 

1. Go inside the demo of [FoodTiger](https://foodtiger.site/),[ QR Menu](https://zebra-qr.com/), or [WhatsApp food](https://whatsappmenus.com/) and login as admin@example.com \| secret
2. Then go to restaurants, and choose some of the demo restaurants
3. Go in Apps tab
4. Enter a link for the WebHook \( you can use any POST API link \)
5. Do a demo order for that restaurant
6. You should get the order data to send to that url
7. Remove the url link from that restaurant



 

