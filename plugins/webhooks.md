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

 

