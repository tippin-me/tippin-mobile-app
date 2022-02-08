




### how to run

1. git clone this project
2. cd and yarn
3. cd ios and pod install,it may tell us
```sh
Could not find proper version of cocoapods (1.11.2) in any of the sources
Run `bundle install` to install missing gems.
```
4. bundle install && pod install
5. cd .. and yarn ios/yarn android.if you yarn android,you may add local.properties at android folder with
```properties
## This file must *NOT* be checked into Version Control Systems,
# as it contains information specific to your local configuration.
#
# Location of the SDK. This is only used by Gradle.
# For customization when using a Version Control System, please read the
# header note.
#Mon Jan 24 10:10:03 CST 2022
sdk.dir=......../Android/sdk
```


