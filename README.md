# EICR Pro Updates

Public update endpoint for the EICR Pro Android app.

## Update manifest

The app should read:

https://raw.githubusercontent.com/mikelizat007/eicr-pro-updates/main/update.json

The manifest contains:
- `version` - human-readable version
- `versionCode` - Android build/version code used for comparison
- `apkUrl` - direct APK download URL
- `releaseNotes` - list of changes shown in the app
- `mandatory` - whether the update must be installed

## APK release naming

Publish each Android release as a GitHub Release and attach the APK with this exact file name:

`EICR_Pro.apk`

The manifest uses this permanent latest-release URL:

https://github.com/mikelizat007/eicr-pro-updates/releases/latest/download/EICR_Pro.apk

## Release process

1. Increase the EICR Pro version/build number.
2. Build the signed release APK.
3. Create a new GitHub Release in this repository.
4. Attach the APK as `EICR_Pro.apk`.
5. Update `update.json` with the new `version`, `versionCode`, and release notes.
6. Keep `mandatory` as `false` unless an update genuinely must be forced.

The Flutter source code remains in the private `eicr_pro` repository and is not published here.
