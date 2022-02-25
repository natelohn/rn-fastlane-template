# Local Environment Set Up
This is a guide on how to set up our local environment for React Native developement with Fastlane. As always, if we run into any issues following this doc, we should open up an issue or better yet a PR to update the information and better help others in the future. Thanks!

## React Native
Follow [this guide](https://reactnative.dev/docs/environment-setup) with `React Native CLI quickstart` selected along with our development environment (MacOS, Windows, or Linux) and whichever target os we choose to complete first. We will need to complete both.

Note: We will not be able to run all Fastlane commands on a Window or Linux system as we will need XCode to run much of the iOS focused commands.

### Android Trouble Shooting:

#### Error: `Failed to launch emulator. Reason: No emulators found as an output of `emulator -list-avds``
We will need to make sure the `R` system image is downloaded for the emulator we are using in Android studio to ensure the `npx react-native run-android` command will find it.

On MacOS editing the `$HOME/.zshrc` file as is suggested in [this link](https://softmastx.com/no-emulators-found-as-an-output-of-emulator-list-avds/) may help.


#### Error: Unable to make field private final java.lang.String java.io.File.path accessible: module java.base does not "opens java.io" to unnamed module @######
If we're getting this error we may need to change which version of java we are using. [This stackoverflow answer](https://stackoverflow.com/a/24657630/15825406) may help us do that.