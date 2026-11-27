# Import Strong or Hevy workout history into LiftSelf

Publisher guide by HIHIHIAI Studio · Updated 27 November 2026 · [Product](https://hihihiai.com/liftself) · [Official import help](https://hihihiai.com/liftself/support#import)

LiftSelf can preview and merge supported workout-history CSV exports from Strong and Hevy. This guide describes the current phone workflow. Export menus and file formats can change between source-app versions; use that app’s current official export instructions.

## Before starting

1. Export your workout history as CSV from Strong or Hevy. Save the original file unchanged outside both apps. A screenshot, PDF or routine-sharing link is not a workout-history CSV.
2. Keep the source app and its records until you finish checking the import. If you already use LiftSelf, export a complete LiftSelf JSON backup first.
3. Note the source weight and distance units and the time zone used for your records. Do not assume every weight is in kilograms.

## Import and review

1. Open **Settings → Your data → Backup & restore → Import data** in LiftSelf. Labels may differ by language or beta version.
2. Choose the CSV. Review the detected source, workout dates and counts, exercise matches, recording types, weight/distance units, and any time-zone or ambiguity prompts.
3. Check representative examples: a heavy lift, a bodyweight or assisted exercise, a timed/distance exercise, and a workout near midnight. If a type or unit is wrong, correct the review rather than accepting misleading numbers.
4. Confirm only when the preview is correct. CSV merges the supported history shown in the preview; **LiftSelf JSON restore is a different operation that replaces the current journal after review and confirmation**.
5. Open History and compare several sessions against the original: dates, exercises, sets, loads, reps or durations. Keep the export until satisfied.
6. Optionally select a workout from the imported file, adjust its targets and save it as a template. A workout already imported from that file can still be selected; review any subsequent local corrections. Missing rest settings use LiftSelf’s default and can be edited.

## Scope and limitations

| Content | What to expect |
| --- | --- |
| Completed workout history | Compatible dates, exercises and recorded sets/metrics are imported; review each file’s preview |
| Exercise types and units | Review explicitly, especially bodyweight, assisted, timed and distance movements |
| Existing imported workouts | Recognized, committed records are skipped; altered exports can be ambiguous, so inspect the preview |
| Saved routine library | Not transferred as a whole by workout-history CSV; create a template from an imported workout instead |
| Accounts, subscriptions and purchases | Not imported or converted |
| Photos, attachments and health data | Not a complete migration; do not assume they are in a workout-history CSV |
| Fields absent from the source export | Cannot be reconstructed; no promise of lossless migration of everything in the source app |
| Full LiftSelf JSON backup | Separate format for restoring LiftSelf’s own journal, including saved templates; not a Strong/Hevy account backup |

The implementation has been exercised with actual Strong and Hevy iPhone CSV exports, including a Chinese Strong export. Those checks do not guarantee every app version, locale, unit setting or future file format. No private source exports are published here.

## If a file fails

Cancel rather than repeatedly confirming an unexpected preview. Keep the original unchanged, check that it is a workout-history CSV, and record the error message and app versions. A malformed or unsupported file must be corrected or exported again; do not delete columns merely to bypass an error.

For help, send the header names and a minimal example using invented values, plus the error and selected units/time zone. Never post your entire export or backup in a public issue. Contact [support](https://hihihiai.com/liftself/support) for private troubleshooting.

## Reproducible fictional example — Android 1.0.0 (20)

Checked on **27 November 2026** in an Android 16 / API 36 emulator using the exact signed ARM64 APK distributed on the website. APK SHA-256: `e36fdd47011a1ef06c60a2b14cb0aeb169a7ddf1d84384bf2c03383a9c5941c4`.

[Download the fictional CSV](https://hihihiai.com/examples/liftself/synthetic-hevy-format-v1.csv) · [Localized example and screenshots](https://hihihiai.com/liftself/support#import-example)

This 521-byte file was generated from invented data using Hevy-style column names. **It was not exported by Hevy**, and a source-app version does not apply. It tests LiftSelf’s handling of this particular input, not the complete source-app export workflow or every historical/future format.

1. Save the CSV and open it through **Settings → Your data → Backup & restore → Import data**. For your own journal, export a full JSON backup first.
2. The preview detects **Hevy, 2 workouts, 3 completed sets**, with **kg/km**. The test used **Asia/Shanghai (UTC+08:00)** as the device/source timezone. The CSV dates do not include a timezone.
3. Under **Review recording types**, review both exercises as **Weight & reps**. Confirm only after checking the preview.
4. After import, check these exact values:

| Workout | Date | Exercise | Completed sets |
| --- | --- | --- | --- |
| Sample A | 24 November 2026 | Bench Press (Barbell) | 20 kg × 8; 25 kg × 6 |
| Sample B | 25 November 2026 | Squat (Barbell) | 30 kg × 5 |

[Preview](https://hihihiai.com/examples/liftself/import-preview.webp) · [History](https://hihihiai.com/examples/liftself/import-history.webp) · [Sample A details](https://hihihiai.com/examples/liftself/import-detail.webp). Screenshots use the English interface and only fictional records.

Opening the same unchanged CSV again showed **0 new workouts, 0 new sets, 2 previously imported workouts skipped**. The sample’s workout description appeared in the first exercise’s notes with the `[Hevy description]` marker; its exercise note was also visible. This does not establish preservation of RPE or other untested fields.

A separate invalid CSV, `example,unsupported` followed by `fictional,1`, produced **“Missing column: date. Select a Strong or Hevy workout CSV.”** The import button was disabled. Keep a failing original intact; do not rename columns to bypass an error without understanding the source format.

This example does not test other units, all exercise types, photos, purchases or every Strong/Hevy export variant. See the [backup and offline restart example](https://hihihiai.com/liftself/support#backup-example) for the same fictional records.
