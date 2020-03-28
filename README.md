# Appium-installation-by-npm
appium installation for test automation against iOS devices running from iOS simulator

# Appium Installation for iOS Simulator test automation on macOS

Appium is an open source test automation framework for use with native, hybrid and mobile web apps.
It drives iOS, Android, and Windows apps using the WebDriver protocol. More details are available at http://appium.io/.

Two Appium installation methods are available for macOS:
* Appium Download - https://github.com/appium/appium-desktop/releases/tag/v1.15.1 (as of March 27, 2020)
* Easy setup process, run a test now. - http://appium.io/ (v1.17.0 as of March 27, 2020)

This document demonstrates the installation of **Easy setup process, run a test now** via homebrew, node.js, and npm.

## Required softwares and libraries on macOS Catalina version 10.15.4
* Xcode
* JDK (1.8)
* homebrew
* carthage
* node & npm
* ios-deploy
* ideviceinstaller
* ios_webkit_debug_proxy
* appium (built with authorize-ios)
* appium-doctor

### Prerequisites

* macOS Cataline 
* user access to macOS Cataline as admin
```
System Preference -> Users & Groups
The **Admin** should be displayed under the user name.
```

### Installing required softwares / libraries

* Install **Xcode:** install from App Store - Xcode Version 11.4 (11E146)
* Install **JDK:** download from https://www.oracle.com/java/technologies/javase-downloads.html#JDK8 (Java SE 8u241 as of March 27, 2020), then **click** on the downloaded **jdk-8u241-macosx-x64.dmg** file to install
* Open a **terminal** 
* Install **homebrew:** ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
* Install **carthage:** brew install carthage
* Install **node.js:** brew install node
* Install **authorize-ios:** npm install -g authorize-ios
* Install **ios-deploy:** brew install ios-deploy
* Install **ideviceinstaller:** brew install ideviceinstaller
* Install **ios-webkit-debug-proxy:** brew install ios-webkit-debug-proxy
* Remove **authorize-ios:** npm remove -g authorize-ios before installing appium
* Install **appium:** npm install -g appium
* Install **appium-doctor:** npm install -g appium-doctor

## Check appium installation
* type: **appium-doctor** in the same terminal
#### Expected output from appium-doctor: ####
```
info AppiumDoctor Appium Doctor v.1.13.1
info AppiumDoctor ### Diagnostic for necessary dependencies starting ###
info AppiumDoctor  ✔ The Node.js binary was found at: /usr/local/bin/node
info AppiumDoctor  ✔ Node version is 13.10.1
info AppiumDoctor  ✔ Xcode is installed at: /Applications/Xcode.app/Contents/Developer
info AppiumDoctor  ✔ Xcode Command Line Tools are installed in: /Applications/Xcode.app/Contents/Developer
info AppiumDoctor  ✔ DevToolsSecurity is enabled.
info AppiumDoctor  ✔ The Authorization DB is set up properly.
info AppiumDoctor  ✔ Carthage was found at: /usr/local/bin/carthage. Installed version is: 0.34.0
info AppiumDoctor  ✔ HOME is set to: /Users/<username>
WARN AppiumDoctor  ✖ ANDROID_HOME is NOT set!
info AppiumDoctor  ✔ JAVA_HOME is set to: /Library/Java/JavaVirtualMachines/jdk1.8.0_241.jdk/Contents/Home
WARN AppiumDoctor  ✖ adb could not be found because ANDROID_HOME is NOT set!
WARN AppiumDoctor  ✖ android could not be found because ANDROID_HOME is NOT set!
WARN AppiumDoctor  ✖ emulator could not be found because ANDROID_HOME is NOT set!
info AppiumDoctor  ✔ Bin directory of $JAVA_HOME is set
info AppiumDoctor ### Diagnostic for necessary dependencies completed, 4 fixes needed. ###
info AppiumDoctor 
info AppiumDoctor ### Diagnostic for optional dependencies starting ###
WARN AppiumDoctor  ✖ opencv4nodejs cannot be found.
WARN AppiumDoctor  ✖ ffmpeg cannot be found
WARN AppiumDoctor  ✖ mjpeg-consumer cannot be found.
WARN AppiumDoctor  ✖ set-simulator-location is not installed
WARN AppiumDoctor  ✖ idb and idb_companion are not installed
WARN AppiumDoctor  ✖ applesimutils cannot be found
info AppiumDoctor  ✔ ios-deploy is installed at: /usr/local/bin/ios-deploy. Installed version is: 1.10.0
WARN AppiumDoctor  ✖ bundletool.jar cannot be found
info AppiumDoctor ### Diagnostic for optional dependencies completed, 7 fixes possible. ###
info AppiumDoctor 
info AppiumDoctor ### Manual Fixes Needed ###
info AppiumDoctor The configuration cannot be automatically fixed, please do the following first:
WARN AppiumDoctor  ➜ Manually configure ANDROID_HOME.
WARN AppiumDoctor  ➜ Manually configure ANDROID_HOME and run appium-doctor again.
info AppiumDoctor 
info AppiumDoctor ### Optional Manual Fixes ###
info AppiumDoctor The configuration can install optionally. Please do the following manually:
WARN AppiumDoctor  ➜ Why opencv4nodejs is needed and how to install it: https://github.com/appium/appium/blob/master/docs/en/writing-running-appium/image-comparison.md
WARN AppiumDoctor  ➜ ffmpeg is needed to record screen features. Please read https://www.ffmpeg.org/ to install it
WARN AppiumDoctor  ➜ mjpeg-consumer module is required to use MJPEG-over-HTTP features. Please install it with 'npm i -g mjpeg-consumer'.
WARN AppiumDoctor  ➜ set-simulator-location is needed to set location for Simulator. Please real https://github.com/lyft/set-simulator-location to install it
WARN AppiumDoctor  ➜ Why idb is needed and how to install it: https://github.com/appium/appium-idb
WARN AppiumDoctor  ➜ Why applesimutils is needed and how to install it: http://appium.io/docs/en/drivers/ios-xcuitest/
WARN AppiumDoctor  ➜ bundletool.jar is used to handle Android App Bundle. Please read http://appium.io/docs/en/writing-running-appium/android/android-appbundle/ to install it
info AppiumDoctor 
info AppiumDoctor ###
info AppiumDoctor
info AppiumDoctor Bye! Run appium-doctor again when all manual fixes have been applied!
info AppiumDoctor
```

## Conclusions
* #### All required softwares / libraries are installed correctly ####
* #### Warnings for android can be ignored since the test automation is targeted for iOS Simulator ####
* #### Warnings for Diagnostic for optional dependencies can be fixed by following the instructions or ignored ####


