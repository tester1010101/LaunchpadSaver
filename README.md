# :warning: NOT COMPLETED YET / DO NOT USE :warning:
\###############################################################
# :black_square_button: LaunchpadSaver (v0.1)
* :recycle: Saves your macOS Launchpad user configuration to a file.
* :shipit: Can be backed up/hashed to external devices/remote servers.

## :computer: Terminal (Command)
> :desktop_computer: Enter this commmand to save it to a file on your desktop; 

> :heavy_exclamation_mark: make sure you don't already have a backup on your Desktop or you can modify the export path, after >>)

### File 1:
```
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout.plist > ~/Desktop/LaunchPadLayout.plist
```
### File 2:
```
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout2.plist > ~/Desktop/LaunchPadLayout2.plist
```
### File 3:
```
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout3.plist > ~/Desktop/LaunchPadLayout3.plist
```
### File 4:
```
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout4.plist > ~/Desktop/LaunchPadLayout4.plist
```

If you need to restore your layout, simply put back the files where they belong (may need to use "sudo" before...);
```
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout.plist > ~/Desktop/LaunchPadLayout.plist.bk
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout2.plist > ~/Desktop/LaunchPadLayout2.plist.bk
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout3.plist > ~/Desktop/LaunchPadLayout3.plist.bk
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout4.plist > ~/Desktop/LaunchPadLayout4.plist.bk

cat ~/Desktop/LaunchPadLayout.plist.bk > /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout.plist
cat ~/Desktop/LaunchPadLayout2.plist.bk > /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout2.plist
cat ~/Desktop/LaunchPadLayout3.plist.bk > /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout3.plist
cat ~/Desktop/LaunchPadLayout4.plist.bk > /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout4.plist
```

![Have your icons ever started acting weird? Simple fix](https://user-images.githubusercontent.com/91343617/210118185-151c57cb-daae-4b41-b2e6-b667073bc9dc.png)
