---
description: >-
  This process takes around 5 min. Your site will be down. You should run it
  when you have lowest number of visitors, or put some website redirect.
---

# Updating - Shared hosting

## 1. If you have made any changes on the code

In case, you have made any changes on the code, css or js file. Backup them first so you don't lose your work. Download them or take a note what you have changed. 

### 2. Backup this files and folder is case something goes wrong

* [ ] .env
* [ ] public/uploads  \( you can zip it and move it somewhere \)

### 3. Download the code from CodeCanyon and extract it

### 4. Open your FTP client and connect to your shared hosting ftp 

Almost all FTP client have the option to exclude some folder from transfer.   
You need to exclude the folder **public/uploads** ,  **storage** and **node\_modules**

![](../.gitbook/assets/exclude.png)

Then, select all  files and folders and upload them. Confirm all replacements. If the update is from minor ex 1.1.1 to 1.1.2 then you don't have to select **vendor** folder. If it is 1.1 to 1.2 then you need to select vendor folder also. 

### 5. After files are moved, open yourdomain.com/update

Here, if there are migrations for the database to be done, will be run. If there is nothing to be done you will get 404 site. 

### 6. See the change log and Environment variables to see what new features are added and how to enable them. 

{% page-ref page="../docs/environment-configuration.md" %}





###   





