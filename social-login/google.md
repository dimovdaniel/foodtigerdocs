---
description: How to enable Google login
---

# Google

Visit [Google API Console](https://console.developers.google.com/).

Create new project or select one if you already create one.

![](../.gitbook/assets/sss%20%2810%29.png)

Next open **Library** from the left menu.

![](../.gitbook/assets/sss%20%287%29.png)

Find Google+ API and click on that.

![](../.gitbook/assets/sss%20%288%29.png)

Enable Google+ API.

![](../.gitbook/assets/sss%20%289%29.png)

Now after you enable the API from the left menu click **QAuth consent screen** and select **External.**

![](../.gitbook/assets/sss.png)

Next fill the following information connected with your domain project and click **Save**.

![](../.gitbook/assets/sss%20%283%29.png)

Now open **Credentials** from left menu, click **Create Credentials** and select **QAuth client ID.**

![](../.gitbook/assets/sss%20%281%29.png)

Select **Web application** and fill the information for your project domain.

![](../.gitbook/assets/sss%20%282%29.png)

{% hint style="danger" %}
NOTE: Your domain need to be the same as the previous in the **QAuth consent screen.**

Also the redirect route need to be the same as it is define in the picture.

_**https://yourdomain.com/login/google/redirect**_
{% endhint %}

{% hint style="info" %}
If you have some problems with authorizing your domain please open **authorized domains list** and add your domain. 
{% endhint %}

Click **Create** and copy the given credentials in the .env file..

![](../.gitbook/assets/sss%20%2817%29.png)













