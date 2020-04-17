---
description: How to enable Google login
---

# Facebook

Visit [Facebook for developers](https://developers.facebook.com/).

Create new project.

![](../.gitbook/assets/sss%20%2812%29.png)

Click **Create App** and fill the information for your project.

![](../.gitbook/assets/sss%20%2813%29.png)

From the left menu click **Settings** and select **Basic**.

![](../.gitbook/assets/sss%20%286%29.png)

Enter the information for your project.

![](../.gitbook/assets/sss%20%2821%29.png)

Next after you finish with this scroll to the bottom, click **Add platform** and select **Website.**

![](../.gitbook/assets/sss%20%284%29.png)

![](../.gitbook/assets/sss%20%2814%29.png)

Now enter your website URL.

![](../.gitbook/assets/sss%20%2822%29.png)

Next from the left menu in Product section find **Facebook Login** and under select **Settings**.

![](../.gitbook/assets/screenshot%20%281%29.png)

Find **Valid QAuaht Redirect URIs** and enter your redirect URL.

{% hint style="info" %}
Note: The redirect must be defined like in the picture below. 
{% endhint %}

![](../.gitbook/assets/screenshot.png)

The last step you need to do is to switch the mode of your app from development to live.

![](../.gitbook/assets/screenshot%20%282%29.png)

Copy **App ID** and **App Secret** and add this values in the .env file.

