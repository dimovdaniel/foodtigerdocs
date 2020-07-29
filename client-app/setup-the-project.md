---
description: To define it as your own project
---

# Setup the project

Download the Client app source code from CodeCanyon and extract it.   
Open the source code in you favorite text/code editor. We suggest [Visual Studio Code](https://code.visualstudio.com/). 

There you will find the file **config.js** 

Replace the values with your real values, like the url link, desired currency. You should have the same values as in you .env file in FoodTiger web. 

**Most important is to change**   
**export.domain** - with your real domain  
**exports.APP\_SECRET** - with the app secret from the .env file from your site   
\( we did this to protect your site \)

```
exports.domain = "https://foodtiger.mobidonia.com/api";

//Currency
exports.currency="USD";
exports.currencySign="$";

//APP API secert
exports.APP_SECRET=""; //Your app secret - same as in the .env file in your web project 

//COD setup
exports.enableCOD=true;  //Cash on deliver

//Stripe settup
exports.enableStripe=false; 
exports.stripePublishKey="YOUR_STRIPE_KEY";

//OneSignal APP KEY
exports.ONESIGNAL_APP_ID="YOUR_ONESIGNAL_APP_ID";

//Google setup
exports.GOOGLE_API_KEY="YOUR_GOOGLE_API_KEY";
exports.queryTypes="address"
exports.queryCountries=['us']; //{['pl', 'fr']}


/*
    searchRadius={500}
    searchLatitude={51.905070}
    searchLongitude={19.458834}
*/
exports.searchLatitude=null;
exports.searchLongitude=null;
exports.searchRadius=null;
```

The same **GOOGLE\_API\_KEY** should be put in android/app/src/main/AndroidManifest.xml  
  
You can use the same **GOOGLE\_API\_KEY** as in your web project.

{% page-ref page="../define-basics/google-api.md" %}



