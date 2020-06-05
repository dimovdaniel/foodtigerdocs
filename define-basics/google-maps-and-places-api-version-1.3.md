---
description: How to get Google Maps and Places API keys
---

# Google Maps and Places API

## Make a Google Project and enable APIs

To use the Maps JavaScript and Places API you must have an API key. The API key is a unique identifier that is used to authenticate requests associated with your project for usage and billing purposes.

To get an API key:

1. Go to the [Google API Console](https://console.developers.google.com/).

   2. Click the project drop-down and select or create the project for which you want to add an API key..

![](../.gitbook/assets/screenshot%20%2813%29.png)

 3. Click the menu button and select **Library**.

![](../.gitbook/assets/screenshot%20%2814%29.png)

4. Find **Maps JavaScript API** and enable it.

![](../.gitbook/assets/screenshot%20%2816%29.png)

5. Go back to the Library menu, find **Places API** and enable it. 

![](../.gitbook/assets/screenshot%20%284%29.png)

6. Click the menu button and select **Credentials** and click **Create credentials &gt; API key**.

![](../.gitbook/assets/screenshot%20%2819%29.png)

The **API key created** dialog displays your newly created API key.

![](../.gitbook/assets/screenshot%20%2818%29.png)

The new API key is listed on the **Credentials** page under **API keys**.  
\(Remember to [restrict the API key](https://developers.google.com/maps/documentation/javascript/get-api-key#restrict_key) before using it in production.\) 

7. Click on **RESTRICT KEY**.

An application restriction controls which websites, IP addresses, or applications can use your API key. You can set one application restriction per key.

* Select **HTTP referrers \(web sites\)**
* Click on **ADD AN ITEM** and add your domain. Your domain should look like this: `https://yourdomain.com/*` or `only yourdomain.com/*`

![](../.gitbook/assets/screenshot%20%2815%29.png)

* Select **Restrict key**.
* Click on **Select APIs drop down menu** and select **Maps JavaScript API** and **Places API**.

![](../.gitbook/assets/screenshot%20%2817%29.png)

Now your API Key is ready for use.

8. Copy the API Key and paste in your `.env` file

```text
GOOGLE_MAPS_API_KEY="" //Uses Google Maps and Places API
```

{% hint style="info" %}
**IMPORTANT:** Please make sure that everything is working okay \(showing maps and adding new client address in order checkout page\).

Sometimes after adding the key these features maybe won't work again. Then depending on the google account associated with the project created and maybe you will need to enable Billing.

Learn more here about it: [Billing](https://console.cloud.google.com/project/_/billing/enable) or here [Getting started with Google Maps Platform](https://developers.google.com/maps/gmp-get-started)
{% endhint %}

