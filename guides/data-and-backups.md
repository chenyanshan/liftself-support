# Local data, optional iCloud and backups

LiftSelf stores its journal on the device and does not require a LiftSelf account. Offline recording is distinct from iCloud, purchasing and restoring purchases, which need access to their online services.

## Apple devices

Supported Apple builds can synchronize selected records through your private iCloud storage. Sync is on by default and can be turned off in **Settings → Your data → Backup & restore**. An exchange already in progress completes before new sync operations stop. Turning it off does not remove existing local or cloud copies.

The synchronized scope includes saved routines, their names and notes, exercise/set plans, folders/order, and completed workout names, dates and set records. Workout notes, photos, body measurements, health/energy data, unfinished workouts and purchase entitlements are excluded. Sync is not a complete backup, and deletions of synchronized records can propagate when sync is enabled.

## Android

Use deliberate file export and import. Android has no iCloud or Google Drive sync. The QR scanner uses Google ML Kit; its SDK can send performance/usage information to Google. “Local-first” does not mean that every optional platform service performs no networking. See the [platform-specific privacy policy](https://hihihiai.com/liftself/privacy).

## Full backup and restore

Export a LiftSelf JSON backup outside the app before reinstalling, changing phones or making a major import. The file contains the journal’s routines and folders, exercise definitions/images, history, body measurements, preferences and phone-accepted active progress within the supported backup scope. It does not transfer Pro, cloud identity, watch authority or independently managed energy data. Records still only on an offline watch need to return to the phone first.

JSON restoration replaces the current journal after preview and confirmation, with recovery protection. CSV imports merge supported history and are not a full backup. Do not assume an automatic operating-system backup will recover the app’s private files. Protect exported files as personal information.

## Moving from a previous test build

Keep the previous app installed, then export a complete JSON backup to Files or another location outside that app. Open the file in LiftSelf, preview and restore it, and compare your workouts and templates before removing the earlier installation. Store entitlements stay with the app and store account used for the purchase.

For current details and deletion behavior, use the [official support](https://hihihiai.com/liftself/support) and [privacy](https://hihihiai.com/liftself/privacy) pages. These instructions do not guarantee that every beta build has passed every multi-device or store test.

## Verified example — Android 1.0.0 (20)

On **27 November 2026**, the website’s released Android 1.0.0 (20) APK was checked in an **Android 16 / API 36 emulator**, using only the [fictional import sample](strong-hevy-import.md#reproducible-fictional-example--android-100-20).

- After importing the sample, Wi-Fi and mobile data were disabled. Following force-stop and cold restart, History still showed Sample A and Sample B with their dates, exercises and loads.
- The sample was exported to a full LiftSelf JSON file outside the app. Only this disposable test installation’s data was cleared; no personal device or user records were used.
- After starting with empty workout history, **Import data** opened the JSON. The replacement preview showed workouts **0 → 2**. **Replace and restore** completed successfully.
- A second JSON export was compared with the first: the entire `history` collection was deeply equal, including both workouts and their three sets. This comparison does not claim that every backup field was independently exercised.

[Localized example](https://hihihiai.com/liftself/support#backup-example) · [History after restore](https://hihihiai.com/examples/liftself/restore-history.webp)

This is a reproducible check on one emulator and one released APK, not evidence for iCloud, store purchases, watch-only records or every device. For your own data, keep a verified export outside the app before reinstalling or replacing a journal; do not clear your app data merely to try the example.
