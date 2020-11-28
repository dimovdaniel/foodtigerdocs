---
description: >-
  This process takes around 5 min. Your site will be down. You should run it
  when you have lowest number of visitors, or put some website redirect.
---

# Updating - Shared hosting

## 1. If you have made any changes on the code

In case, you have made any changes on the code, css or js file. Backup them first so you don't lose your work. Download them or take a note what you have changed. 

### 2. Backup this files and folders

* [ ] .env \( you can also do it via the env editor in your admin panel \) 
* [ ] public/uploads  \( you can zip it and move it somewhere \)

{% hint style="info" %}
It is recommended to zip/backup your entire project
{% endhint %}

### 3. Download the code from CodeCanyon and upload the zip

Download the code from CodeCanyon and directly upload it on your hosting, in the same place where your existing site is.

### 4. Extract the zip file 

Extract the zip files. Overwriting old files.

### 5. Put back your old .env file

You old .env file contains previous settings to connect to db, mail and so on. So it is required to but it back. 

### 6. Create "installed" file

In the storage folder, create a new file "installed" like the one on the [image](https://prntscr.com/vriof4).

### 7. After the file is extracted, open yourdomain.com/update

Here, if there are migrations for the database to be done, will be run. If there is nothing to be done you can get 404 site. 

{% hint style="danger" %}
This step is mandatory
{% endhint %}

### 8. See the changelog and Environment variables to see what new features are added and how to enable them. 

{% page-ref page="../docs/environment-configuration.md" %}





###   





