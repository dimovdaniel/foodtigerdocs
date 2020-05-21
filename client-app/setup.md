# Setup

## Getting started

This is React Native. Read the getting started guide in expo, and run a local example to confirm your environment is ok. 

Download the Client app source code from CodeCanyon and extract it. 

Open the source code in you favorite text/code editor. We suggest Visual Studio Code. 

## Setup config.js file

```text
exports.domain = "https://foodtiger.mobidonia.com/api";

//Currency
exports.currency="USD";
exports.currencySign="$";

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



