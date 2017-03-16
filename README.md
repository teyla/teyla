# 入门

欢迎来到React Native！ 此页面将帮助您在系统上安装React Native，以便您可以立即构建应用程序。 如果已经安装了React Native，可以跳过教程。

根据您的开发操作系统，以及是否要开始为iOS或Android开发，这些说明有所不同。 如果你想开发iOS和Android，那很好 - 你只需要选择一个开始，因为设置有点不同。

## 安装依赖关系

您将需要Node.js，React Native命令行界面和Android Studio。

### Node

我们建议通过Chocolatey安装Node.js和Python2，Windows是一个流行的软件包管理器。 以管理员身份打开命令提示符，然后运行：

```
choco install nodejs.install
choco install python2
```

> 您可以在Node.js下载页面中找到其他安装选项。

### The React Native CLI

Node.js comes with npm, which lets you install the React Native command line interface.

Run the following command in a Terminal:

npm install

-

g react

-

native

-

cli

> If you get an error like`Cannot find module 'npmlog'`, try installing npm directly:`curl -0 -L https://npmjs.org/install.sh | sudo sh`.

### Android Development Environment

Setting up your development environment can be somewhat tedious if you're new to Android development. If you're already familiar with Android development, there are a few things you may need to configure. In either case, please make sure to carefully follow the next few steps.

#### 1. Download and install Android Studio

[Android Studio](https://developer.android.com/studio/install.html)provides the Android SDK and AVD \(emulator\) required to run and test your React Native apps.

#### 2. Install the AVD and HAXM

Android Virtual Devices allow you to run Android apps on your computer without the need for an actual Android phone or tablet. Choose`Custom`installation when running Android Studio for the first time. Make sure the boxes next to all of the following are checked:

* `Android SDK`
* `Android SDK Platform`
* `Performance (Intel ® HAXM)`
* `Android Virtual Device`

Then, click "Next" to install all of these components.

> If you've already installed Android Studio before, you can still[install HAXM](https://software.intel.com/en-us/android/articles/installation-instructions-for-intel-hardware-accelerated-execution-manager-windows)without performing a custom installation.

#### 3. Install the Android 6.0 \(Marshmallow\) SDK

Android Studio installs the most recent Android SDK by default. React Native, however, requires the`Android 6.0 (Marshmallow)`SDK. To install it, launch the SDK Manager, click on "Configure" in the "Welcome to Android Studio" screen.

> The SDK Manager can also be found within the Android Studio "Preferences" menu, under**Appearance & Behavior**→**System Settings**→**Android SDK**.

Select "SDK Platforms" from within the SDK Manager, then check the box next to "Show Package Details". Look for and expand the`Android 6.0 (Marshmallow)`entry, then make sure the following items are all checked:

* `Google APIs`
* `Android SDK Platform 23`
* `Intel x86 Atom_64 System Image`
* `Google APIs Intel x86 Atom_64 System Image`

![](https://facebook.github.io/react-native/img/AndroidSDKManager.png "Android SDK Manager")

Next, select the "SDK Tools" tab and check the box next to "Show Package Details" here as well. Look for and expand the "Android SDK Build Tools" entry, then make sure that`Android SDK Build-Tools 23.0.1`is selected.

Finally, click "Apply" to download and install the Android SDK and related build tools.

#### 4. Set up the ANDROID\_HOME environment variable

The React Native command line interface requires the`ANDROID_HOME`environment variable to be set up.

Go to**Control Panel**→**System and Security**→**System**→**Change settings**→**Advanced System Settings**→**Environment variables**→**New**, then enter the path to your Android SDK.

![](https://facebook.github.io/react-native/img/react-native-android-sdk-environment-variable-windows.png "env variable")

Restart the Command Prompt to apply the new environment variable.

> Please make sure you export the correct path for`ANDROID_HOME`if you did not install the Android SDK using Android Studio.

## Starting the Android Virtual Device

![](https://facebook.github.io/react-native/img/react-native-tools-avd.png "Android Studio AVD Manager")

You can see the list of available AVDs by opening the "AVD Manager" from within Android Studio. You can also run the following command in a terminal:

android avd

Once in the "AVD Manager", select your AVD and click "Edit...". Choose "Android 6.0 - API Level 23" under Device, and "Intel Atom \(x86\_64\)" under CPU/ABI. Click OK, then select your new AVD and click "Start...", and finally, "Launch".

![](https://facebook.github.io/react-native/img/AndroidAVDConfiguration.png "Android AVD Configuration")

> It is very common to run into an issue where Android Studio fails to create a default AVD. You may follow the[Android Studio User Guide](https://developer.android.com/studio/run/managing-avds.html)to create a new AVD manually if needed.

### Using a real device

If you have a physical Android device, you can use it for development in place of an AVD. Plug it in to your computer using a USB cable and[enable USB debugging](https://developer.android.com/training/basics/firstapp/running-app.html)before proceeding to the next step.

## Testing your React Native Installation

Use the React Native command line interface to generate a new React Native project called "AwesomeProject", then run`react-native start`inside the newly created folder to start the packager.

react

-

native init AwesomeProject cd AwesomeProject react

-

native start

Open a new command prompt and run`react-native run-android`inside the same folder to launch the app on your Android emulator.

react

-

native run

-

android

If everything is set up correctly, you should see your new app running in your Android emulator shortly.

![](https://facebook.github.io/react-native/img/AndroidSuccess.png "AwesomeProject on Android")

### Modifying your app

Now that you have successfully run the app, let's modify it.

* Open
  `index.android.js`
  in your text editor of choice and edit some lines.
* Press the
  `R`
  key twice or select
  `Reload`
  from the Developer Menu to see your change!

### That's it!

Congratulations! You've successfully run and modified a React Native app.

![](https://facebook.github.io/react-native/img/react-native-congratulations.png)

## Now What?

* If you want to add this new React Native code to an existing application, check out the[Integration guide](https://facebook.github.io/react-native/docs/integration-with-existing-apps.html).

* If you can't get this to work, see the[Troubleshooting](https://facebook.github.io/react-native/docs/troubleshooting.html#content)page.

* If you're curious to learn more about React Native, continue on to the[Tutorial](https://facebook.github.io/react-native/docs/tutorial.html).



