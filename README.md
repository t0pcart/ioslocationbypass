# ioslocationbypass
stops background location updating on iOS devices without tripping the app

there is no support and will be no updates will this as im done with location bypasses

**how this shit works**

locationd/locationpushd is the daemon that sends location updates to apps in the background

findmydeviced, fmflocatord, fmfd are the daemons used by Find My

by unloading the above dameons we can stop location updates systemwide without tripping an app's location service permissions(saying your location is off/offline/or that the app doesnt have location entitlements)

**steps**
- you need a jailbreak 
- install [NewTerm 3](https://chariz.com/get/newterm-beta) inside your package manager of choice
- install launchctl in your package manager of choice
- run su and type in your root password 
- run "load" in NewTerm to re-load the location dameons
- run "unload" in NewTerm to unload- the location dameons

  **If the executable won't run in NewTerm run chmod a+x (un)load**

  Bypassing Life360 requires marking it as non-executable first, a tutorial on how to do this is included

  This tool only unloads the dameon and does not disable it, after a reboot background location services will be restored
