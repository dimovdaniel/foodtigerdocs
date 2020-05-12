# Stripe Gateway

## Setup Stripe account information

FoodTiger supports Stripe gateway for payments. To setup the gateway follow these steps.

By default this method is set to **false** and to enable you need to change it to **true**.

```text
ENABLE_STRIPE=false
```

Now visit [Stripe](https://stripe.com) official site. Create new account or login with existing one.

From the left menu choose **Developers** and select **API keys** under that**.**

In the standard keys find your **Publishable key** and **Secret key.**

![](../.gitbook/assets/screenshot%20%289%29.png)

Now copy them and paste in your **.env** file.

```text
STRIPE_KEY="" //Stripe API key
STRIPE_SECRET="" //Stripe API Secret
```

If you want to use Stripe payment you can leave it blank this variables.



### Stripe iDeal payments

For now we don't have integrate option for Stripe iDeal payment so for now this option is set to false.

```text
ENABLE_STRIPE_IDEAL=false //Should we have stripe ideal payment
```













