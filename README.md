# Hide-Specific-App-Icon-from-mac-os-Dock-Menu
Hides app icon in mac os dock when they are active or opened 


Source :- https://apple.stackexchange.com/a/349641


### Steps :- 

Use native PlistBuddy command to do it:

```
/usr/libexec/PlistBuddy -c 'Add :LSUIElement bool true' /Applications/[AppName].app/Contents/Info.plist
```

Don't forget to change the [App Name] and path.

If you wish gonna back (Revert), run command:

```
/usr/libexec/PlistBuddy -c 'Delete :LSUIElement' /Applications/[AppName].app/Contents/Info.plist
```
