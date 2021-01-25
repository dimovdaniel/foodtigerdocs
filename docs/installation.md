---
description: Learn how to install Food Tiger
---

# Installation on Shared Hosting

## Requirements

Food Tiger is a self-hosted web application written in PHP on top of the Laravel 8.0 framework. The followings are required to install Food Tiger:

* PHP Version: 7.4 or 8.0
* MySQL Version: &gt;= 5.x
* Application server: Apache, Nginx
* IMPORTANT: The script can't be installed in a subfolder. Only directly in domain or subdomain.

## Prepare to install

Installing Food Tiger is very easy and you'll be able to install it without any coding knowledge. The installation process included three major steps:

1. **Creating domain or subdomain**
2. **Creating a database**
3. **Uploading script files to the host**

**Now below you can watch the video installation tutorial or you can continue with step by step.**

{% embed url="https://youtu.be/DgJ3dpeYNVY" %}


### Installation on Shared Hosting

Plesk / cPanel and other hosting managers are recommended. In this guide, we will use Plesk but similar should be for others.

#### 1. Create your domain or subdomain in your shared hosting

After you have created that, you will be able to access the file manager for that domain/subdomain

Delete any default files that are maybe added.

#### 2. Create a database

Create an empty database in your shared hosting and remember this credentials

* db name
* db username
* db user pass


#### 3.  Upload the source code you have downloaded from CodeCanyon and unzip it

#### 4. Now navigate to the web url where your project is located

ex. mydomain.com or subdomain.mydomain.com

The installation screen should appear and guide you in the process.

When you login as admin, in Site Settings you have the option to change all the settings. 

{% hint style="danger" %}
Don't forget to do the SMTP setup. Without it, you will get error 500 on register.
{% endhint %}

Here is how to do it

{% page-ref page="../define-basics/obtain-smtp.md" %}

When you finish with the configuration we can go on the next step application usage.

Learn how to use it.

{% page-ref page="../usage/getting-started.md" %}

