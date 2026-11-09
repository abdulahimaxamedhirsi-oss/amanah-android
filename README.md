# AMANAH – Android test app

This folder turns the AMANAH design preview into an Android app (APK) that you can install on your Samsung S25.
GitHub builds the APK for you, for free. You do not need Android Studio.

## Steps (about 10 minutes)

1. Make a free account at github.com if you do not have one.
2. Click the + at the top right, then "New repository". Name it `amanah-android`. Choose "Private". Click "Create repository".
3. On the next page click "uploading an existing file". Unzip this folder on your computer first, then drag in EVERYTHING inside it,
   including the hidden `.github` folder. Click "Commit changes".
   (If you cannot see `.github`, turn on "show hidden files" on your computer, or create the file by hand:
   Add file > Create new file > name it `.github/workflows/build-apk.yml` and paste the contents of that file.)
4. Open the "Actions" tab. The "Build Android APK" job starts by itself. It takes about 5 to 8 minutes. Wait for the green tick.
   (If nothing starts, click "Build Android APK" on the left, then "Run workflow".)
5. Click the finished job, scroll to "Artifacts", and download `amanah-apk`. Unzip it to get `app-debug.apk`.
6. Send `app-debug.apk` to your phone (Google Drive, email to yourself, or USB).
7. On the S25, tap the file. Android asks to allow installs from that app: allow it once. Tap Install.

## Good to know

- This is a TEST build with sample data. The demo PIN is 123456. It is not connected to the real backend yet.
- The first time you open it the phone needs internet (it loads the Manrope font).
- If the build job shows a red cross, open it, copy the error text, and send it to Claude.
- To update the app later: replace `www/index.html` in your repository with the new version. GitHub builds a new APK.
