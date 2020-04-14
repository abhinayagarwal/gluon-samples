# User Authentication

This example shows how to perform user authentication in a [Gluon Mobile](http://gluonhq.com/products/mobile/)
application using [Gluon Cloudlink](http://gluonhq.com/products/cloudlink/).
 
## Prerequisites

You need a valid subscription to Gluon CloudLink. You can get it [here](http://gluonhq.com/products/cloudlink/buy/), and 
there is a 30-day free trial. Sign up and get a valid account on Gluon CloudLink and a link to download the Gluon CloudLink 
Dashboard. 

Install and open the Dashboard, and sign in using the Gluon account credentials provided above. You can then
create a login method using the ["User Management"](http://docs.gluonhq.com/cloudlink/#_user_management) section. 

To configure Cloudlink in mobile application, go to the App Management view in the Dashboard, and you will 
find a pair of key/secret tokens. Save the file `gluoncloudlink_config.json` under your mobile project 
`src/main/resources/` folder. The content of the file is a JSON object with the key and secret that will grant access
to Gluon CloudLink:

```json
{
  "gluonCredentials": {
    "applicationKey": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
    "applicationSecret": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
  }
}
``` 

## Instructions

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

## Documentation

Read how to create this sample step by step here