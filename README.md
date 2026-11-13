# My Workouts - APK project

## Easiest: build in the cloud (no Android Studio)
1. Create a free GitHub account and a new repository (branch: main).
2. Upload ALL files from this folder, including the hidden `.github` folder
   (easiest with GitHub Desktop or `git push`; on the website use
   "Add file > Create new file" and type `.github/workflows/build-apk.yml`
   if the folder does not upload).
3. Open the repo > Actions tab > "Build APK" > Run workflow.
4. After ~5 min open the finished run, download the `my-workouts-apk` artifact,
   unzip it, copy app-debug.apk to your phone and install it
   (allow "Install unknown apps" when asked).

## Or build locally (needs Node.js 18+, Android Studio, JDK 17)
    npm install
    npx cap add android
    npx cap sync android
    npx cap open android      # Build > Build APK(s)

The app icon is generated from the files in assets/ during the build.
To change the app, edit www/index.html and rebuild.
