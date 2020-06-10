# One Signal push notifications

From version 1.3 in the script we enable push notification for web and mobile apps.

For the setup guide you can follow one signal official [video tutorial](https://www.youtube.com/watch?v=lNv_3qq1sKs) or our step by step explanation.

Visit the [OneSignal official website](https://onesignal.com/).

Click on the **NEW APP/WEBSITE** button.

![](../.gitbook/assets/screenshot%20%2837%29.png)

Now enter your app name and select **Web Push**.

![](../.gitbook/assets/screenshot%20%2834%29.png)

Next enter your **Site name**, **Site URL** and **upload or enter the default icon UR**L.

![](../.gitbook/assets/screenshot%20%2835%29.png)

Now after you finish with the Site Setup next step is Permission Prompt Setup.

Slide Prompt is added by default and you need to click on it for changing the configuration.

More information you will find on the video documentation about this part.

Next click on **ADD A PROMPT**.

![](../.gitbook/assets/screenshot%20%2833%29.png)

 ****Click on the **SUBSCRIPTION BELL** and customize the look in the options under that.

Also you can find more details about it in the video documentation.

![](../.gitbook/assets/screenshot%20%2838%29.png)

Next step is configuration on Welcome Notification.

Here you can change the **TITLE**, **MESSAGE** and **LINK**.

![](../.gitbook/assets/screenshot%20%2836%29.png)

After you finish with this click on the **Save** button and then **Finish**.

Now after you app is active you will need to get the credentials created in this app.

You will find this credentials in the **Keys & IDs** page.

![](../.gitbook/assets/screenshot%20%2839%29.png)

After you finish with the setup copy the credentials and add into .env file.

```text
ONESIGNAL_APP_ID=
ONESIGNAL_REST_API_KEY=
```



