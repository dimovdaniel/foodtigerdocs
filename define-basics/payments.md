# Payments

At this moment FoodTiger comes with two methods to make payments: Pay cash on delivery, Pay via Stripe. To enable or disable this methods there are several variables that you will need to configure.

  
By default the two methods are set to false and to enable you need to change them to true.  
  
**- Cash on Delivery**  
`HIDE_CODE` change from **false** to **true** if you want to enable it. ****

```text
HIDE_COD=false //Hide or Show Cash on Delivery payment
```

 **- Stripe Gateway** 

{% page-ref page="stripe-gateway.md" %}



### Default payment method

You can choose which payment method to be set by default. Choose one of the aliases.

`cod` - Cash on delivery

`stripe` - Stripe gateway

```text
DEFAULT_PAYMENT="cod" //Default payment method - Cash On Delivery default cod|stripe
```



### **Payment currency**

FoodTiger supports many currencies. By default is set to **usd** currency but you can change into one of the [available currencies](https://stripe.com/docs/currencies#presentment-currencies). 

```text
CASHIER_CURRENCY="usd" //usd,eur etc.
```

