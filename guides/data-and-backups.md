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

For current details and deletion behavior, use the [official support](https://hihihiai.com/liftself/support) and [privacy](https://hihihiai.com/liftself/privacy) pages. These instructions do not guarantee that every beta build has passed every multi-device or store test.
