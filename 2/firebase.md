---
title: 'Firebase Setup'
prev_page:
  url: /1/1/google-cloud-platform.html
  title: 'Google Cloud Platform'
next_page:
  url: /1/3/auto-ml-vision-edge.html
  title: 'Auto ML Vision Edge'
title: 'Firebase Setup'

prev_page:

  url: /1/1/google-cloud-platform.html

  title: 'Google Cloud Platform'

next_page:

  url: /1/3/auto-ml-vision-edge.html

  title: 'Auto ML Vision Edge'

comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"

comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---
Firebase
==============
Firebase is a google service/platform that enables developers to build high quality apps, 
using a number of features and capabiities. It is build on Google infrastructure and 
allows for functionalities such as analystics, messaging, and databases. Using Firebase 
allows developers to create better apps, fast, without having to manage infrastructure.

Firebase for Android...

The first step is to launch the Firebase Console, in which a Firebase project can be created. 
Once a project is created (or firebase is added to an existing GCP project), the Android app 
must be registered to Firebase. The Android apps application ID, found in the 
app/build.gradle file, must be added as the Android Package Name field in the Firebase 
project setup. 

Once the App is registered to Firebase, the next step is to configure it. The configuration 
file for Firebase Android should be added to the Android app. This configuration file 
(google-services.json) should be added to the app-level directory of the andriod app 
project via Android Studio.   

Nest, Firebase SDKs must be added to the Android App. SDKs added should be specific to 
the functionalities desired for Firebase and the machine learning task/cloud computing
project at hand. Some of the important SDKs added for this project are:

--Google Firebase Analytics
--Cloud Storage for Firebase
--ML Kit AutoML Vision Edge


<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
##The Google services plugin for Gradle loads the google-services.json file 
#Modify your build.gradle files to use the plugin.
##Project-level build.gradle (<project>/build.gradle):

buildscript {
  dependencies {
    // Add this line
    classpath 'com.google.gms:google-services:4.2.0'
  }
}

##App-level build.gradle (<project>/<app-module>/build.gradle):

dependencies {
  // add SDKs for desired Firebase products
  // https://firebase.google.com/docs/android/setup#available-libraries
}

```
</div>

</div>


Cloud Firestore and Storage

Using Cloud Firestore provids access to a database that maintains and syncs data 
across all apps. It is easily integrated with other GCP products and functions. 
A newstorage bucket should be created from the Firebase console, and the dependency 
should be added to the module Gradle file (similar to the apps sdks added in the
prior steps).


<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
##firebase storage bucket cloud setup

service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      allow read, write: if request.auth != null;
    }
  }
}
##add dependancy for the Cloud Storage Android library to your module 
##(app-level) Gradle file (usually app/build.gradle)

implementation 'com.google.firebase:firebase-storage:19.0.0'
```
</div>


