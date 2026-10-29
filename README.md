# Master Financial Planner (hosted)

This folder is the whole app. Everything you enter stays in your browser and, if you turn on sync, in a hidden app
folder in your own Google Drive. Nothing personal is in these files.

## Put it online (GitHub Pages, free)
1. Sign in at github.com (or create a free account).
2. New repository: name it `planner`, Public, then Create repository.
3. Click "uploading an existing file", drag in every file from this folder, then Commit changes.
4. Settings > Pages: Source "Deploy from a branch", Branch `main`, folder `/ (root)`, Save.
   About a minute later the app is at https://YOUR-NAME.github.io/planner/

## Google sign-in ID (for sync, once)
1. console.cloud.google.com, signed in with the Google account you'll sync with: create a project (any name).
2. APIs & Services > Library: Google Drive API > Enable.
3. Google Auth Platform (OAuth consent screen) > Get started: app name, your email, Audience External, Create.
4. Audience > Test users > Add users: your Google address.
5. Clients > Create client: Web application; Authorized JavaScript origins: https://YOUR-NAME.github.io
   (no path, no slash at the end). Create, then copy the Client ID (ends in .apps.googleusercontent.com).
   Optional: paste it into config.js here so no device asks for it.

## Move your data in and turn on sync
1. In your current copy (the file on your computer): Income & spending > Accounts & data > Download backup.
2. Open https://YOUR-NAME.github.io/planner/ and choose "restore a backup" on the first screen.
3. Sidebar: "Sync is off · Set up". Paste the Client ID, name the device, optionally set a passphrase, Turn on sync.
4. In the sync screen, "Copy a setup link" and open it on your phone (Chrome: Share > Send to your devices).
   Turn on sync there with the same Google account (and passphrase). Chrome menu > Add to home screen.

## Update
Upload a newer build over these files (keep your config.js).
