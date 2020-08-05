# Restaurant subdomain

## Set up wildcard subdomain 

Most commonly used shared hosting framework is cPanel. So we will write our guide for it. But things should be similar in Plesk or any other solution. 

After you have your main domain or subdomain active, and your site is up and running, you can make each restaurant to have their own domain. Like in our demo. 

The main site is [https://foodtiger.site/](https://foodtiger.site/) and there you can find all restaurants. But each restaurant can be also directly open for example: [https://malibudiner.foodtiger.site/](https://malibudiner.foodtiger.site/). This feature is directly enable in your foodtiger site. But you will need to create a wildcard subdomain that uses the same folder as your main site. 

![Click on Subdomain](../.gitbook/assets/subdomain.png)

![Enter \* for Subdomain](../.gitbook/assets/the_subdomain.png)

1. Enter \* for Subdomain
2. Select your domain
3. Select \( enter \) the same document root - in this case /public\_html

Each restaurant has automatically their own subdomain now. Open some restaurant in your site. Example:

[https://foodtiger.site/restaurant/malibudiner](https://foodtiger.site/restaurant/malibudiner) --&gt;  [https://malibudiner.foodtiger.site](https://malibudiner.foodtiger.site/)

In this case the subdomain is **malibudiner**

## **SSL - HTTPS** 

By default the wildcard subdomains are not SSL protected. To do that you can buy or issue wildcard SSL certificate - sometimes they are a bit expensive. You can also use [https://letsencrypt.org/](https://letsencrypt.org/) to create your own free wildcard SSL.  Plesk by default can enable SSL on wildcard subdomain. You can also use this [guide](https://medium.com/@saurabh6790/generate-wildcard-ssl-certificate-using-lets-encrypt-certbot-273e432794d7). Our demo site works on Laravel Forge. They also have the options to automatically create wildcard SSL via Digital Ocean NS. 



