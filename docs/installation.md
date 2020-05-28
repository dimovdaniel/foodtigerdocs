---
description: Learn how to install FoodTiger
---

# Installation on Shared Hosting

## Requirements

Foodtiger is a self-hosted web application written in PHP on top of the Laravel 5.8 framework. The followings are required to install Foodtiger:

* PHP Version: 7.1 or higher
* MySQL Version: &gt;= 5.x
* Application server: Apache, Nginx

## Prepare to install

Installing FoodTiger is very easy and you'll be able to install it without any coding knowledge. Installation process included three major steps:

1. **Creating domain or subdomain**
2. **Creating database**
3. **Uploading script files to the host**
4. **Creating environment configuration**

**Now bellow you can watch the video installation tutorial or you can continue with step by step.**

{% hint style="info" %}
**Warning:** Video installation tutorial doesn't include environment explanation. You can check that in the steps below.
{% endhint %}

## Video installation tutorial

{% embed url="https://www.youtube.com/watch?v=XaFa8OyNiDc&feature=youtu.be" %}



### Installation on Shared Hosting

Plesk / cPanel and other hosting managers are recommended. In this guide we will use Plesk but similar should be for other. 

#### 1. Create your domain or subdomain in your shared hosting

After you have created that, you will be able to access the file manager for that domain/subdomain

Delete any default files that are maybe added.

#### 2. Create a database

Create an empty database in your shared hosting and remember this credentials

* db name
* db username
* db user pass

The process of making database is something like this.

![](../.gitbook/assets/dbadd.png)



#### 3.  Upload the source code you have downloaded from CodeCanyon and unzip it

![](../.gitbook/assets/extract.png)

#### 4. Now navigate to the web url where your project is located

ex. mydomain.com or subdomain.mydomain.com

You should be redirected to a screen like this one

![](../.gitbook/assets/foodtiger-installer.png)

Click on the "Check Requirements" If some requirements is missing it will be noted out.

![](../.gitbook/assets/system.png)

Now let's check folder permissions. If some folder is noted as not writable, please check his permission. It should be 775 or 777

![](../.gitbook/assets/permissions.png)

Now we need to setup the environment. This tells larval how to work

![](../.gitbook/assets/classic.png)

Select the classic text editor

![](../.gitbook/assets/save_env%20%281%29.png)

**5. Environment Configuration**

{% hint style="info" %}
**Note:** This configuration requires many steps so we will explain this more detailed.
{% endhint %}

Next click on the article below to continue with the configuration.

{% page-ref page="environment-configuration.md" %}

When you finish with the configuration don't forget to save the env file.

![](../.gitbook/assets/save_env.png)

Click on **Save and install**

Now the install process will begin

It will install all the demo data in your database. If some error occurs, the next screen will tell you that. Take screenshot from it. Send to our support chat.

If all goes okay, you can click on "Finish" 

Now you have your own instance 

Learn how to use it. 

{% page-ref page="../usage/getting-started.md" %}



