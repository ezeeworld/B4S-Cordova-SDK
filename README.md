Cordova Neerby Plugin
========================

The purpose of this plugin is to offer a simple Neerby SDK integration for Cordova Android and iOS applications.

## Usage

For both iOS and Android platforms, the SDK parameters are set through Cordova CLI variables.

#### 1. iOS prerequities

You must set the Neerby ApplicationID for your application and set the background mode explanation application text.
- ApplicationID is set through the **NEERBY_APP_ID** variable.
- Background mode explanation text is set through the **LOCATION_ALWAYS_USAGE_DESCRIPTION** variable.

#### 2. Android

The Neerby SDK cannot be integrated as a true Cordova plugin. So, the plugin installation script for Android add an Application subclass 'com.ezeeworld.neerby.NeerbyApp' to your project.
This class is instanciated through the AndroidManifest.xml file. The Manifest file is automatically patched by the plugin installation process.
If your project already instanciate an Application subclass, you can follow the classic SDK installation at https://github.com/ezeeworld/B4S-Android-SDK

#### 3. Install the plugin

Before proceeding to the installation, do not forget to set the variables with real values.

(`cordova plugin add https://github.com/ezeeworld/B4S-Cordova-SDK.git --variable NEERBY_APP_ID="SET_YOUR_OWN_APPID" --variable LOCATION_ALWAYS_USAGE_DESCRIPTION="This mode is requested to enable Neerby iBeacon detection."`)