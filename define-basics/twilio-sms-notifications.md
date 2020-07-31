# Twilio SMS notifications

From version 1.4 in the script we enable SMS notifications.

By default this feature is disabled and you will need to enable by changing the ENV variable from **false** to **true**.

```text
ENABLE_SMS_VERIFICATION=true
```

Visit the [Twilio official website](https://www.twilio.com/) and create a new account.

After creating you will have access to the Twilio console.

From the left menu select **Settings** &gt; **General.**

Find **API Credentials** sections and copy **ACCOUNT SID** and **AUTH TOKEN**.

![](../.gitbook/assets/screenshot%20%2846%29.png)

Add these variables in your ENV file.

```text
TWILIO_ACCOUNT_SID=""
TWILIO_AUTH_TOKEN=""
```

Now you will need to add your phone number that you will use for your project.

Click on the menu under the home icon and select **Phone Numbers**.

![](../.gitbook/assets/screenshot%20%2844%29.png)

Add new phone number and add in your ENV file again.

```text
TWILIO_FROM=""
```



