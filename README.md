# Bluedot Android PointSDK Xamarin wrapper
This repository contains a project to make a C# wrapper for Bluedot Android PointSDK.

## Building

1. Download the latest Android Point SDK AAR file from artifacts released from Gitlab PointSDK repository https://gitlab.com/bluedotio/android/point_sdk_android, and overwrite the previous version of Android SDK in the `Jars` folder.

2. Open solution, then open project **Options -> NuGet Package -> Metadata** and update version. Or if on a Mac, right click the Project (not Solution) -> Edit Profile file -> Update `<PackageVersion>` value.

3. Build the project with `release` configuration. It will produce `Bluedot.PointSDK.Android.X.Y.Z.nupkg` in `PointSDK-Xamarin-Android/bin/Release/`.

## Validating
There is a Integration sample at https://github.com/Bluedot-Innovation/PointSDK-Xamarin-minimal-app-Android. To validate the Nuget package:

1. Open `BDPointAndroidXamarinDemo.sln`

2. Open **Visual Studio Preferences -> NuGet -> Sources** then add build folder from the **step 3** in **Building** stage

3. Right click on **project -> Add -> Ad NuGet Packages...** then choose NuGet repository from the previous step.

4. Select desired version of **Bluedot.PointSDK.Android ** and press **Add Package**

5. Build and run the project.

Note: If SDK is not refreshed in Minimal App, Test after renaming the Package name `Bluedot.PointSDK.Android.X.Y.Z.nupkg` to `Bluedot.PointSDK12.Android.X.Y.Z.nupkg` and include this in Min App

## Releasing

1. Open solution in Visual Studio

2. Build the project with `release` configuration. It will produce `Bluedot.PointSDK.Android.X.Y.Z.nupkg` in `PointSDK-Xamarin-Android/bin/Release/`.

3. Go to `https://www.nuget.org/packages/Bluedot.PointSDK.Android` and login to Bluedot account.

4. Upload `Bluedot.PointSDK.Android.X.Y.Z.nupkg` from `PointSDK-Xamarin-Android/bin/Release/`