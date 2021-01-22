---
description: To define it as your own project
---

# Setup the project

Download the Client app source code from CodeCanyon and extract it.   
Open the source code in your favorite text/code editor. We suggest [Visual Studio Code](https://code.visualstudio.com/). 

There you will find the file **config.js** 

Replace the values with your real values, like the ULR link, desired currency. You should have the same values as in your .env file in FoodTiger web. 

{% hint style="info" %}
The most important is to change

**exports.domain** - with your real domain

**exports.APP\_SECRET** - with the app secret from the .env file from your site 
{% endhint %}

The same **GOOGLE\_API\_KEY** should be put in android/app/src/main/AndroidManifest.xml  
  
You can use the same **GOOGLE\_API\_KEY** as in your web project.

{% page-ref page="../define-basics/google-api.md" %}



