# :warning: NOT COMPLETED YET / DO NOT USE :warning:
\###############################################################
# :black_square_button: LaunchpadSaver (v0.2)
* :recycle: Saves your macOS Launchpad user configuration to a folder.
* :shipit: Can be backed up/hashed to external devices/remote servers.

## :computer: Terminal (Command-line)
> :desktop_computer: Enter this commmand to save it to a folder in your user folder (~); 

> :heavy_exclamation_mark: make sure you don't already have a backup in the folder created or you can modify the rsync path)



### Folder (with 3 files):
```
mkdir ~/.swap_
cd $(getconf DARWIN_USER_DIR)/com.apple.dock.launchpad
rsync -a db ~/.swap_/
```

### Files:
```
ls ~/.swap_/db/

aap@mbook com.apple.dock.launchpad % ls -lh db
total 3688
-rw-r--r--  1 aap  staff   1.6M  6 Jan 19:20 db
-rw-r--r--  1 aap  staff    32K  7 Jan 07:56 db-shm
-rw-r--r--  1 aap  staff   157K  7 Jan 07:56 db-wal
```

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

If you need to restore your layout, simply put back the files where they belong (may need to use "sudo" before...);
```
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout.plist > ~/Desktop/LaunchPadLayout.plist.bk
cat /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout2.plist > ~/Desktop/LaunchPadLayout2.plist.bk
rsync -a ~/.swap_/db $(getconf DARWIN_USER_DIR)/com.apple.dock.launchpad/

cat ~/Desktop/LaunchPadLayout.plist.bk > /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout.plist
cat ~/Desktop/LaunchPadLayout2.plist.bk > /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout2.plist
cat ~/Desktop/LaunchPadLayout3.plist.bk > /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout3.plist
cat ~/Desktop/LaunchPadLayout4.plist.bk > /System/Library/CoreServices/Dock.app/Contents/Resources/LaunchPadLayout4.plist
```

![Have your icons ever started acting weird? Simple fix](https://user-images.githubusercontent.com/91343617/210118185-151c57cb-daae-4b41-b2e6-b667073bc9dc.png)

Credit/source: https://fgimian.github.io/blog/2016/12/23/how-macos-stores-launchpad-configuration/
