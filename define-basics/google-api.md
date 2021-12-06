---
description: How to get Google Maps, Places and Geo location API keys
---

# Google API

## Make a Google Project and enable APIs

To use the Maps JavaScript, Places API and Geolocation API you must have an API key. The API key is a unique identifier that is used to authenticate requests associated with your project for usage and billing purposes.

To get an API key:

1. Go to the [Google API Console](https://console.developers.google.com).

&#x20;  2\. Click the project drop-down and select or create the project for which you want to add an API key.

![](<../.gitbook/assets/screenshot (13).png>)

&#x20;3\. Click the menu button and select **Library**.

![](<../.gitbook/assets/screenshot (14).png>)

4\. Find **Maps JavaScript API** and enable it.

![](<../.gitbook/assets/screenshot (16).png>)

5\. Go back to the Library menu, find **Places API** and enable it.&#x20;

![](<../.gitbook/assets/screenshot (4).png>)

6\. Go back to the Library menu, find **Geocoding API** and enable it.

![](<../.gitbook/assets/screenshot (43).png>)

7\. Click the menu button and select **Credentials** and click **Create credentials > API key**.

![](<../.gitbook/assets/screenshot (19).png>)

The **API key created** dialog displays your newly created API key.

![](<../.gitbook/assets/screenshot (18).png>)

The new API key is listed on the **Credentials** page under **API keys**.\
(Remember to [restrict the API key](https://developers.google.com/maps/documentation/javascript/get-api-key#restrict\_key) before using it in production.)&#x20;

7\. Click on **RESTRICT KEY**.

An application restriction controls which websites, IP addresses, or applications can use your API key. You can set one application restriction per key.

* Select **HTTP referrers (web sites)**
* Click on **ADD AN ITEM** and add your domain.\
  Your domain should look like this: `https://yourdomain.com/*` and `yourdomain.com/*`

![](<../.gitbook/assets/screenshot (30).png>)

* Select **Restrict key**.
* Click on **Select APIs drop down menu** and select **Maps JavaScript API** and **Places API** and **GeoCoding API**

![](<../.gitbook/assets/screenshot (17).png>)

Now your API Key is ready for use.

8\. Copy the API Key and paste in your `.env` file

```
GOOGLE_MAPS_API_KEY="" //API KEY
```



### Possible problems

{% hint style="info" %}
**IMPORTANT:** Please make sure that everything is working okay (showing maps and adding new client address in order checkout page).

You must enable Billing on the Google Cloud Project at [https://console.cloud.google.com/project/\_/billing/enable](https://console.cloud.google.com/project/\_/billing/enable%20Learn%20more%20at%20https://developers.google.com/maps/gmp-get-started)

[Learn more at ](https://console.cloud.google.com/project/\_/billing/enable%20Learn%20more%20at%20https://developers.google.com/maps/gmp-get-started)\
\
[https://developers.google.com/maps/gmp-get-started](https://console.cloud.google.com/project/\_/billing/enable%20Learn%20more%20at%20https://developers.google.com/maps/gmp-get-started)
{% endhint %}

\
1\. **Change application restrictions** \
****\
****Depending on your server/domain configuration the script maybe won't accept the **HTTP referrers** restrictions so try with changing the application restrictions back to **None**&#x20;

![](<../.gitbook/assets/screenshot (32).png>)

2\. **Enable Billing on your project.**

Sometimes after adding the key these features maybe won't work again. Then depending on the google account associated with the project created and maybe you will need to enable Billing.\


Learn more here about it: [Billing](https://console.cloud.google.com/project/\_/billing/enable) or here [Getting started with Google Maps Platform](https://developers.google.com/maps/gmp-get-started)



If you have still problems with this configuration write us on our [support chat](https://help.mobidonia.com/#foodtiger) for help/assistance.



## Allow us to configure Google project for you

Go to the [Google Cloud Platform](https://console.cloud.google.com).

Click the project drop-down and select your project.

From the left menu select **IAM & Admin**.

![](<../.gitbook/assets/screenshot (42).png>)

Now click on the **Add** button.

![](<../.gitbook/assets/screenshot (40).png>)

Add our email **mobidonia@gmail.com** and give us **Editor** role.

![](<../.gitbook/assets/screenshot (41).png>)

In the end click **Save**.

Write us on our [support chat ](https://help.mobidonia.com/#foodtiger)for your project details.
