# Local Environment Set Up
This is a guide on how to set up our local environment for React Native developement with Fastlane. As always, if we run into any issues following this doc, we should open up an issue or better yet a PR to update the information and better help others in the future. Thanks!

## React Native
Follow [this guide](https://reactnative.dev/docs/environment-setup) with `React Native CLI quickstart` selected along with our development environment (MacOS, Windows, or Linux) and whichever target os we choose to complete first. We will need to complete both. 

### Troubleshooting
Below we have a list of errors that we have ran into while running this project, but we can always check the [React Native Troubleshooting Docs](https://reactnative.dev/docs/troubleshooting) for more info.

#### error Unrecognized command "run-ios".
Make sure to run all `npx react-native ______` commands within the project (`FastlaneRN`) directory

### Android Specific Troubleshooting:

#### Error: `Failed to launch emulator. Reason: No emulators found as an output of `emulator -list-avds``
We will need to make sure the `R` system image is downloaded for the emulator we are using in Android studio to ensure the `npx react-native run-android` command will find it.

On MacOS editing the `$HOME/.zshrc` file as is suggested in [this link](https://softmastx.com/no-emulators-found-as-an-output-of-emulator-list-avds/) may help.


#### Error: Unable to make field private final java.lang.String java.io.File.path accessible: module java.base does not "opens java.io" to unnamed module @######
If we're getting this error we may need to change which version of java we are using. [This stackoverflow answer](https://stackoverflow.com/a/24657630/15825406) may help us do that.

### iOS Specific Troubleshooting:

#### Command PhaseScriptExecution failed with a nonzero exit code
This error may be due to us not having the correct (or any) node version (using `nvm`) configured on our local machine. T[his StackOverflow answer](https://stackoverflow.com/a/53118851/14846515) has helped some of us configure our local machine. React Native docs suggest using the latest stable LTS version so we should stick with that unless we're getting fancy.

## Fastlane
Note: We will not be able to run all Fastlane commands on a Window or Linux system as we will need XCode to run much of the iOS focused commands and it is only available on MacOS.