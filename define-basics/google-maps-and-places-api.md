---
description: How to get Google Maps and Places API keys
---

# Google Maps and Places API

**From version 1.3**  
  
To use the Google JavaScript API you must have an API key. The API key is a unique identifier that is used to authenticate requests associated with your project for usage and billing purposes.

Go to the [Google API Console](https://console.developers.google.com/).

Click the project drop-down and select or create the project for which you want to add an API key.

![](../.gitbook/assets/sss-1%20%281%29.png)

Next open **Library** from the left menu.

![](../.gitbook/assets/screenshot%20%2822%29.png)

Find Maps JavaScript API.

![](../.gitbook/assets/screenshot%20%2829%29.png)

Now enable Maps JavaScript API.

![](../.gitbook/assets/screenshot%20%2821%29.png)

Now next open **Library** from the left menu.

Find **Places API**.

![](../.gitbook/assets/screenshot%20%288%29.png)

Now enable **Places API**.

![](../.gitbook/assets/screenshot%20%284%29.png)

After you enable it from the left menu button select **Credentials** and in the **Credentials** page, click on the link **Credentials in APIs & Services**.

![](../.gitbook/assets/screenshot%20%2820%29.png)

Now after it redirects you to the new page click **Create credentials &gt; API Key**.

![](../.gitbook/assets/screenshot%20%2823%29.png)

The **API key created** dialog displays your newly created API key.

The new API key is listed on the **Credentials** page under **API keys**.  
\(Remember to [restrict the API key](https://developers.google.com/maps/documentation/javascript/get-api-key#restrict_key) before using it in production.\)

![](../.gitbook/assets/screenshot%20%2828%29.png)

Now after you click on **RESTRICT KEY** you will need to do several steps.

* Click on HTTP referrers \(web sites\)
* Add your domain with clicking **ADD AN ITEM** Your domain should look like this: **`https://*.yourdomain.com/*`**

![](../.gitbook/assets/screenshot%20%2827%29.png)

* Click **Restrict key** and then open **Select APIs** drop down menu and choose **Maps JavaScript API** and **Places API**.

![](../.gitbook/assets/screenshot%20%2824%29.png)

Click **SAVE** and your API is ready for using.

Copy the API Key and paste in your `.env` file

```text
GOOGLE_MAPS_PLACES_API_KEY="" //Display google maps
```

{% hint style="warning" %}
NOTE: After enabling the APIs please check if everything works okay.   
If everything works okay than your work is done here.  
  
Otherwise if see that maps and adding client new address are not working, depending on the google account associated with that project maybe you will need to enable Billing on your Google project.   
  
Check these links for more info: [Link1](https://console.cloud.google.com/project/_/billing/enable), [`Link2`](https://developers.google.com/maps/gmp-get-started)\`\`
{% endhint %}





















