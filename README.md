# :black_square_button: LaunchpadSaver (v0.1)
* :recycle: Saves your macOS Launchpad user configuration to a file.
* :shipit: Can be backed up/hashed to external devices/remote servers.

## :computer: Terminal (Command)
> :desktop_computer: Enter this commmand to save it to a file on your desktop; 
> :heavy_exclamation_mark: make sure you don't already have a backup on your Desktop or you can modify the export path, after >>)
```
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout.plist >> ~/Desktop/LaunchPadLayout.plist
```
If you need to restore your layout, simply put back the file where it belong (may need to use "sudo" before...);
```
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout.plist > ~/Desktop/LaunchPadLayout.plist.bk
cat ~/Desktop/LaunchPadLayout.plist > /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout.plist
```

![Have your icons ever started acting weird? Simple fix](https://user-images.githubusercontent.com/91343617/210118185-151c57cb-daae-4b41-b2e6-b667073bc9dc.png)
