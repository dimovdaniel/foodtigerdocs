# Single restaurant

From the version 1.4.0 the project supports single restaurant version.  
To enable this option you will need to make these steps:

Chande the environment variable **SINGLE\_MODE** from **false** to **true**.

```text
SINGLE_MODE=true
```

Open your database using phpMyAdmin on your shared hosting or just simply open Adminer. \(Adminer is php script to manage your database\). The Adminer is located on **yourdomain.com/adminer**

There, login with your database username and password. 

Open **restorants** table and find the restaurant that you want to use in your project.

Find the column **id** and see which number ID is used for that restaurant.

![](../.gitbook/assets/screenshot%20%2847%29.png)

Now add the restaurant id in the following environment variable.

```text
SINGLE_MODE_ID=1 //Restaurant id
```

