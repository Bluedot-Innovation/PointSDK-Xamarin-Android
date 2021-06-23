# Bluedot Android PointSDK Xamarin wrapper
This repository contains a project to make a C# wrapper for Bluedot Android PointSDK.

## Building

1. Download the latest Android Point SDK AAR Jar file from https://github.com/Bluedot-Innovation/PointSDK-Xamarin-Android/blob/master/Jars/pointsdk-release.aar, and overwrite the previous version of Android SDK in the `Jars` folder.

2. Open solution, then open project **Options -> NuGet Package -> Metadata** and update version.

3. Build the project with `release` configuration. It will produce `Bluedot.PointSDK.Android.X.Y.Z.nupkg` in `PointSDK-Xamarin-Android/bin/Release/`.

## Validating
There is a Integration sample at https://github.com/Bluedot-Innovation/PointSDK-Xamarin-minimal-app-Android. To validate the Nuget package:

1. Open `BDPointAndroidXamarinDemo.sln`

2. Open **Visual Studio Preferences -> NuGet -> Sources** then add build folder from the **step 3** in **Building** stage

3. Right click on **project -> Add -> Ad NuGet Packages...** then choose NuGet repository from the previous step.

4. Select desired version of **Bluedot.PointSDK.Android ** and press **Add Package**

5. Build and run the project.
