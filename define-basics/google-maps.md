---
description: How to get Google maps API Key
---

# Google Maps \(version 1.2\)

You must have at least one API key associated with your project.  
To get an API key:

Head over to[ Google Developers Web Maps JavaScript API ](https://developers.google.com/maps/documentation/javascript/get-api-key)to obtain API Key.

Click on the "**Get Started**" button.

![](../.gitbook/assets/sss%20%2815%29.png)

**Select Maps**

![](../.gitbook/assets/sss%20%2819%29.png)

Then Select or create a project.

![](../.gitbook/assets/sss%20%285%29.png)

**Then set up billing.** 

In the end, you will get the **API KEY.** 

**Important:** When you get your Google API Key, by default is not protected, it means, it can be used anywhere. 

Make sure you set up the URL where your key will be used. 

Go in [Google Cloud Platform](https://console.cloud.google.com/apis/credentials)

![](../.gitbook/assets/sss%20%2820%29.png)

Locate the key you have created and enter the url.

![](../.gitbook/assets/sss%20%2811%29.png)

Copy the API Key and paste in your `.env` file

```text
GOOGLE_MAPS_API_KEY="" //Display google maps
```



