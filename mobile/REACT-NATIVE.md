# Working with React Native

- Only aimed at producing APK in Windows when working with React Native. Therefore:
- This workspace does not work in WSL. Git Bash would have to be used.
- Even then, to make an APK, if cannot be done in CLI inside Git Bash. We must use Android Studio.

## Setup

1. Set up your Windows dev environment by installing Git Bash

   - https://gitforwindows.org
   - For better UI with Git Bash, remember to tick option to add Git Bash to Windows Terminal so you can customize the UI.

2. Run Windows Terminal as administrator and run the following: `choco install -y nodejs-lts microsoft-openjdk11` to install Node in Git Bash.

3. Install **Android Studio**, https://developer.android.com/studio, and make sure `AndROID SDK`, `Android SDK Platform`, and `Android Virtual Device` are ticked.

   - You should go for SDKs for Android 12+.

4. Open Android Studio, click **More Actions** and select **SDK Manager**. Go for `Android 12 (S)` and/or up. Make sure you've check `Android SDK Platform 31` or up, and `Intel x86 Atom_64 System Image`. Now, in the official documentation it recommends making sure `Google APIs Intel x86 Atom System Image` is ticked, _but_ you should also tick `Google Play Intel x86 Atom System Image`.

5. Next, select `SDK Tools` tab and check `Show Package Details` so we can look for the `Android SDK Build-Tools` entry. Make sure it's `31.0.0` is selected and/or up.

6. Now we gotta set up our Windows environment variables for Android Studio. Open Window's **Control Panel**, then **User Accounts** twice and click **Change my environmental variables**. Press **New** to create a new variable:

   - Variable name: `ANDROID_HOME`
   - Variable value: `%LOCALAPPDATA%\Android\Sdk` or `C:\Users\your_user\AppData\Local\Android\Sdk`
   - To verify the env var is there, run `Get-ChildItem -Path Env:\` in PowerShell.

7. Add **platform-tools** to Path environment variable. Double-click **Path**, then **Edit**, click **New** and enter `%LOCALAPPDATA%\Android\Sdk\platform-tools`.

- To make APK in Android Studio, make sure to follow React Native docs and open the `android` directory in Android Studio

<hr>

## References:

- https://reactnative.dev/docs/environment-setup

- [Programming with Mash's React Native Tutorial #35 (2021) - Generating APK & Android App Bundle for Google Play Store](https://www.youtube.com/watch?v=5tgcogEoIiQ)

  - https://www.youtube.com/watch?v=5tgcogEoIiQ
