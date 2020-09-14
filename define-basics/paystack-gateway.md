# Paystack Gateway

## Paystack account information

FoodTiger supports Paystack gateway for payments. To setup the gateway follow these steps.

By default this method is set to **false** and to enable you need to change it to **true**.

```text
ENABLE_PAYSTACK=false
```

Now visit [Paystack](https://paystack.com/) official site. Create new account or login with existing one.

From the left side menu select **Settings** and open **API Keys and Webhooks**.

The **Secret Key** and the **Public key** will be auto generated.

In the **Callback URL** enter 

{% hint style="info" %}
**https://yourdomain.com/payment/callback**
{% endhint %}

In the **Webhook URL** enter

{% hint style="info" %}
**https://yourdomain.com/pay**
{% endhint %}

After you are done with this click on **Save changes**.

Now lets add these credentials in your env file.

```text
PAYSTACK_PUBLIC_KEY=your public key
PAYSTACK_SECRET_KEY=your secret key
PAYSTACK_PAYMENT_URL=https://api.paystack.co
MERCHANT_EMAIL=your paystack email
```



