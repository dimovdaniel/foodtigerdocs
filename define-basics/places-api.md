---
description: How to get Google Places API Key
---

# Google Places API \(version 1.2\)

Visit [Google API Console](https://console.developers.google.com/).

Create new project or select one if you already create one.

![](../.gitbook/assets/sss-1.png)

Next open **Library** from the left menu.

![](../.gitbook/assets/sss%20%287%29.png)

Find Places API.

![](../.gitbook/assets/screenshot%20%288%29.png)

Enable Places API.

![](../.gitbook/assets/screenshot%20%284%29.png)

After you enable the Places API go back to [Google API Console](https://console.developers.google.com/).

In the menu from the left side select **Credentials**.

![](../.gitbook/assets/screenshot%20%287%29.png)

On the **Credentials** page, click **Create credentials &gt; API key**.  
The **API key created** dialog displays your newly created API key.

![](../.gitbook/assets/screenshot%20%281%29.png)

Now copy the given key in the **.env** file.

```text
GOOGLE_MAPS_GEOCODING_API_KEY=YOUR_API_KEY
```



