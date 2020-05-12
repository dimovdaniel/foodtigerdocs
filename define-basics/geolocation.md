---
description: How to get Google Geo location API Key
---

# Geolocation

Visit [Google API Console](https://console.developers.google.com/).

Create new project or select one if you already create one.

![](../.gitbook/assets/sss-1.png)

Next open **Library** from the left menu.

![](../.gitbook/assets/sss%20%287%29.png)

Find Geolocation API.

![](../.gitbook/assets/sss-1-.png.png)

Enable Geolocation API.

![](../.gitbook/assets/sss-1-.png%20%281%29.png)

Click the menu button and select **APIs & Services &gt; Credentials**.

![](../.gitbook/assets/screenshot%20%288%29.png)

On the **Credentials** page, click **Create credentials &gt; API key**.  
The **API key created** dialog displays your newly created API key.

![](../.gitbook/assets/screenshot%20%281%29.png)

Now copy the given key in the .env file.

```text
GOOGLE_MAPS_GEOCODING_API_KEY=YOUR_API_KEY
```



