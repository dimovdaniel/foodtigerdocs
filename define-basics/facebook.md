---
description: How to enable Google login
---

# Facebook authentication

Visit [Facebook for developers](https://developers.facebook.com).

Create new project.

![](<../.gitbook/assets/sss (12).png>)

Click **Create App** and fill the information for your project.

![](<../.gitbook/assets/sss (13).png>)

From the left menu click **Settings** and select **Basic**.

![](<../.gitbook/assets/sss (6).png>)

Enter the information for your project.

![](<../.gitbook/assets/sss (21).png>)

Next after you finish with this scroll to the bottom, click **Add platform** and select **Website.**

![](<../.gitbook/assets/sss (4).png>)

![](<../.gitbook/assets/sss (14).png>)

Now enter your website URL.

![](<../.gitbook/assets/sss (22).png>)

Next from the left menu in Product section find **Facebook Login** and under select **Settings**.

![](<../.gitbook/assets/screenshot (6).png>)

Find **Valid QAuaht Redirect URIs** and enter your redirect URL.

{% hint style="info" %}
Note: The redirect must be defined like in the picture below.&#x20;
{% endhint %}

![](<../.gitbook/assets/screenshot (2).png>)

The last step you need to do is to switch the mode of your app from development to live.

![](<../.gitbook/assets/screenshot (12).png>)

Copy **App ID** and **App Secret** and add this values in the .env file.\


```
FACEBOOK_CLIENT_ID="" //Used for facebook login
FACEBOOK_CLIENT_SECRET="" //Used for facebook login
FACEBOOK_REDIRECT="" //Used for facebook login
```
