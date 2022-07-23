# Bankey app

## How to create a new iOS project without storyboard

1. Remove the uncessary files
  - `SceneDelegate.swift`
  - `Main.storyboard`

2. Update `info.plist`
  - Select the app on left panel, click "Shift + command + F"
  - Search for "main"
  - Select `Bankey.xcodeproj` file
  - Search for "main" again inside the file, select `UIKit Main Storyboard File Base Name` record and hit delete
  - Select `Info.plist`, select the record `Application Scene Manifest` and hit delete

3. Update `AppDelegate.swift`
