



I use ruby 2.7.4 to install cocoapods.

```sh
npx react-native init Tippin --directory tippin-mobile-app --template react-native-template-typescript
```

but it tell me

```sh
✔ Processing template
ℹ Installing dependencies
✔ CocoaPods (https://cocoapods.org/) is not installed. CocoaPods is necessary for the iOS project to run correctly. Do you want to install it? › Yes, with gem (may require sudo)
✔ Installing CocoaPods
✖ Installing CocoaPods dependencies (this may take a few minutes)
✖ Installing CocoaPods dependencies (this may take a few minutes)
error Error: Failed to install CocoaPods dependencies for iOS project, which is required by this template.
Please try again manually: "cd ./tippin-mobile-app/ios && pod install".
CocoaPods documentation: https://cocoapods.org/
```

so I should mannuly install the rest

```sh
cd ./tippin-mobile-app/ios && pod install
```
it tells me

```sh
Warning: the running version of Bundler (2.1.4) is older than the version that created the lockfile (2.2.27). We suggest you to upgrade to the version that created the lockfile by running `gem install bundler:2.2.27`.
Could not find proper version of cocoapods (1.11.2) in any of the sources
Run `bundle install` to install missing gems.
```

then i do the following

```
gem install bundler:2.2.27 && pod install
```

```sh
Could not find proper version of cocoapods (1.11.2) in any of the sources
Run `bundle install` to install missing gems.
```

then i do

```sh
bundle install && pod install
```

finally success


when yarn android,it tells

```sh
error Failed to install the app. Make sure you have the Android development environment set up: https://reactnative.dev/docs/environment-setup.
Error: Command failed: ./gradlew app:installDebug -PreactNativeDevServerPort=8081

FAILURE: Build failed with an exception.

* What went wrong:
Could not determine the dependencies of task ':app:compileDebugJavaWithJavac'.
> SDK location not found. Define location with an ANDROID_SDK_ROOT environment variable or by setting the sdk.dir path in your project's local properties file at '/Users/wyknmjj/Documents/GitHub/tippin-mobile-app/android/local.properties'.

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 33s
```
so i create local.properties ad android folder with
```
## This file must *NOT* be checked into Version Control Systems,
# as it contains information specific to your local configuration.
#
# Location of the SDK. This is only used by Gradle.
# For customization when using a Version Control System, please read the
# header note.
#Mon Jan 24 10:10:03 CST 2022
sdk.dir=......../Android/sdk
```