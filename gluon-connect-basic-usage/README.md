# Gluon Connect - Basic Usage

A JavaFX application that uses [Gluon Connect](https://gluonhq.com/open-source/connect), an application framework to
bind your data to your JavaFX UI controls. This application demonstrates how to retrieve data from a resource that is
located on the classpath.

## Documentation

Read how to create this sample step by step here

## Quick Instructions

Please follow the pre-requisites as stated [here](https://github.com/gluonhq/client-samples/#build-and-run-the-samples).

### Desktop

Run the application using:

    mvn javafx:run

Build a native image using:

    mvn client:build

Run the native image app:

    mvn client:run

### Android

Build a native image for Android using:

    mvn client:build -Pandroid

Package the native image as an 'apk' file:

    mvn client:package -Pandroid

Install it on a connected android device:

    mvn client:install -Pandroid

Run the installed app on a connected android device:

    mvn client:run -Pandroid

### iOS

Build a native image for iOS using:

    mvn client:build -Pios

Install and run the native image on a connected iOS device:

    mvn client:run -Pios

Create an IPA file (for submission to Test Flight or App Store):

    mvn client:package -Pios