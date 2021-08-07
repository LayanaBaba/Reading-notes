# Android Fundamentals

- Android apps can be written using Kotlin, Java, and C++ languages.
- An Android package : is an archive file with an `.apk` suffix, contains the contents of an Android app. 
- An Android App Bundle : is an archive file with an `.aab` suffix, contains the contents of an Android app project.
-  An AAB is a publishing format and is not installable on Android devices.

Each Android app protected by the following Android security features:

1. The Android operating system.
2. The system sets permissions for all the files in an app so that only the user ID assigned to that app can access them.
3. Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.
4. The Android system starts the process when any of the app's components need to be executed, and then shuts down the process.

There are ways for an app to share data with other apps and for an app to access system services:
1. It's possible to arrange for two apps to share the same Linux user ID, in which case they are able to access each other's files. 
2. An app can request permission to access device data such as the device's location, camera, and Bluetooth connection. 

## App components

Types of app components:
1. Activities.
2. Services.
3. Broadcast receivers.
4. Content providers.

### Activities:
An activity is the entry point for interacting with the user. An activity facilitates the following key interactions between system and app:
- Keeping track of what the user currently cares about.
- Knowing that previously used processes contain things the user may return to.
- Helping the app handle having its process killed so the user can return to activities with their previous state restored.
- Providing a way for apps to implement user flows between each other, and for the system to coordinate these flows.

### Services:
It is a component that runs in the background to perform long-running operations or to perform work for remote processes.

### Broadcast receivers:
A broadcast receiver is a component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements.

### Content providers:
A content provider manages a shared set of app data that you can store in the file system, on any persistent storage location that your app can access. 

## Activating components
- Activities, services, and broadcast receivers are activated by an asynchronous message called an intent.
- An intent is created with an Intent object.

## The manifest file
Before the Android system can start an app component, the system must know that the component exists by reading the app's manifest file, `AndroidManifest.xml`. The manifest does a number of things in addition to declaring the app's components, such as the following:
1. Identifies any user permissions the app requires.
2. Declares the minimum API Level required by the app, based on which APIs the app uses.
3. Declares hardware and software features used or required by the app.
4. Declares API libraries the app needs to be linked against.

* You must declare all app components using the following elements:
1. `<activity>` elements for activities.
2. `<service>` elements for services.
3. `<receiver>` elements for broadcast receivers.
4. `<provider>` elements for content providers.
<br>
<br>
* When you declare an activity in your app's manifest, you can optionally include intent filters that declare the capabilities of the activity so it can respond to intents from other apps.
* To prevent your app from being installed on devices that lack features needed by your app, it's important that you clearly define a profile for the types of devices your app supports by declaring device and software requirements in your manifest file.
*  Using app resources makes it easy to update various characteristics of your app without modifying code.