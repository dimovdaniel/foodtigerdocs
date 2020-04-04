---
description: Learn how to install FoodTiger
---

# Installation

Foodtiger is a self-hosted web application written in PHP, on top of the Laravel 5.8 framework. The followings are required to install Foodtiger:

* PHP Version: 5.6, 7.0, 7.1 or higher
* MySQL Version: &gt;= 5.x
* Application server: Apache, Nginx

### Installation with cPanel

Upload Foodtiger source files to the domain webroot folder. The file structure should look like this:

here image

### Installation with Apache

Before installing, make sure that Apache `mod_rewrite` is **enabled** and `mod_security` is **disabled**.

Then, unzip the source file

```text
cd /home/user/
unzip foodtiger.zip
```

Put Foodtiger source folder into your domain document root. For example, if your Foodtiger source is located at `/home/user/foodtiger`, you can configure Apache virtual host as follows, notice how `DocumentRoot` is setup

```text
<VirtualHost *:80>
  ServerName yourhost.net
  DocumentRoot "/home/user/foodtiger/public"
  Options Indexes FollowSymLinks
  <Directory "/home/user/foodtiger/public">
    AllowOverride All
    Require all granted
  </Directory>
</VirtualHost>
```

Change the director/file's owner to Apache's running user, to make sure it has proper permission on your source files. If you are on Ubuntu, the default user that Apache runs under is `www-data` \(and it is `apache` for CentOS/RedHat\).

```text
sudo chown www-data:www-data -R /home/user/foodtiger
sudo chmod 775 -R /home/user/foodtiger
```

Then restart Apache and go to the webapp's installation URL. For example `http://yourhost.net`

Follow the web installation wizard to get Foodtiger installed on your own host.

