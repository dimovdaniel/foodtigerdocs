---
description: 'IMPORTANT: Follow this step after you have done all of the previous steps'
---

# Android App

## Make the signing certificate 

First, let's make a key - certificate that we will use for debug and release signing. So we don't make two key files.   
  
The official documented why by React Native is to make the keystore via [command line](https://reactnative.dev/docs/signed-apk-android#generating-an-upload-key). But since this is a bit complex, we will suggest the following steps.

1. Open android studio
2. Make new app, doesn't matter what you enter. 
3. Go to Build-&gt;Generate Signed Bundle / APK, click next
4. Select  Android App Bundle or APK \( it is the same \) , click next
5. Click on "Create new" to create new keystore
6. For keystore path, select your project folder, and then go in android/app/production.keystore
7. For passwords, and aliases use your values. Remember them. 
8. After you have made the keystore, open `android/app/build.gradle` and around line 155, change the values of the **release** element with the values you have. 

```text
release {
            storeFile file('production.keystore')
            storePassword 'android'
            keyAlias 'android'
            keyPassword 'android'
        }
```

For reference, look into this video

{% embed url="https://www.loom.com/share/23b69ab308be4d358fa358c00dbcbe95" %}

## Run the app on emulator or Android device \( device recommended \)

To run the app on Android Emulator, you will first need to manually start the android Emulator via Android Studio. You should already have download the Android Studio in step 1 - the Environment setup. In that guide there are also really good informations on how to prepare real device or starting the Android Emulator. Search for "Preparing the Android device" in the [React native docs.](https://reactnative.dev/docs/environment-setup#docsNav)

Once you have the emulator started or  device connected via USB \( and developer mode enabled and US debugging allowed \), you should be able to start the app on the. To do that, run the following command in the root of the project.

```text
npm run android
```

After this, you should see the app running on your emulator on connected device. 

## Make .aab  file \( compile the app \)

Full guide we followed [here](https://reactnative.dev/docs/signed-apk-android#generating-the-release-apk). 

Next, if you are happy how the app looks, it is time to compile the app and sign it with distribution keystore you did before.

First, you need to have the react native package manager up and running. In the rood of your project execute the following command.

```text
react-native start
```

This will start the package manager.   
  
Open new terminal window, and navigate to your project **android** folder, and then execute the command   
`./gradlew bundleRelease`

```text
cd android
./gradlew bundleRelease
```

If all goes well you should have the app as .aab file in android/app/build/outputs/bundle/release/app-release.aab

.aab files are preferred for Google Play, because Google will optimize the app size. But you can also create .apk file if you like with the following command. 

```text
./gradlew assembleRelease
```

This .aab file, should be uploaded on Google Play

## Distribute on Google Play

After you have the .aab file it is time to upload this file on google play. As mentioned before, you will need Google Developer account. 

Login into your [Google Play developer console](https://play.google.com/apps/publish).

The process of uploading the app to Google Play is perfectly explained here  
[https://instabug.com/blog/how-to-submit-your-app-to-the-google-play-store/](https://instabug.com/blog/how-to-submit-your-app-to-the-google-play-store/)

## Help and problems

If you face any problem, don't hesitate to let us know on our support chat. 

{% embed url="https://help.mobidonia.com/\#foodtiger" %}



