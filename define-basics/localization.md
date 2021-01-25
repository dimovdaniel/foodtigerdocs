# Localization and Time format

## Localization

By default is set in English but you can change it on some of the available languages.

```text
APP_LOCALE=en
```

### **Manually adding new language**

Since some of the languages are still not available you can add manually new language. There are several steps you need to do for achieving that.

In the source code find **resources &gt; lang &gt; en.json** file. Copy the file and paste in the same location.

Rename the copied file into your new language code and save it.

Open the file and translate the English words or sentences into your new language.

When you finish with this change your new language code in the **APP\_LOCALE** environment variable.

## Time Format

From the version 1.2 there is option for customizing the time format in the script for working hours.

There are two options:

* 24 hours time format `24hours`
* AM PM format `AM/PM`

By default is 24 hours time format.

```text
TIME_FORMAT="24hours"
```

## Time zone

To set the correct timezone that your site operates in create .env variable.

It is really important to have done this step, in order restaurant closing and open time to work ok.

```text
TIME_ZONE=UTC
```

List of available [timezones](https://www.php.net/manual/en/timezones.php).

