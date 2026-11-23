# Import Strong or Hevy workout history into Solift

Publisher guide by HIHIHIAI Studio · Updated 23 November 2026 · [Product](https://hihihiai.com/solift) · [Official import help](https://hihihiai.com/solift/support#import)

Solift can preview and merge supported workout-history CSV exports from Strong and Hevy. This guide describes the current phone workflow. Export menus and file formats can change between source-app versions; use that app’s current official export instructions.

## Before starting

1. Export your workout history as CSV from Strong or Hevy. Save the original file unchanged outside both apps. A screenshot, PDF or routine-sharing link is not a workout-history CSV.
2. Keep the source app and its records until you finish checking the import. If you already use Solift, export a complete Solift JSON backup first.
3. Note the source weight and distance units and the time zone used for your records. Do not assume every weight is in kilograms.

## Import and review

1. Open **Settings → Your data → Backup & restore → Import data** in Solift. Labels may differ by language or beta version.
2. Choose the CSV. Review the detected source, workout dates and counts, exercise matches, recording types, weight/distance units, and any time-zone or ambiguity prompts.
3. Check representative examples: a heavy lift, a bodyweight or assisted exercise, a timed/distance exercise, and a workout near midnight. If a type or unit is wrong, correct the review rather than accepting misleading numbers.
4. Confirm only when the preview is correct. CSV merges the supported history shown in the preview; **Solift JSON restore is a different operation that replaces the current journal after review and confirmation**.
5. Open History and compare several sessions against the original: dates, exercises, sets, loads, reps or durations. Keep the export until satisfied.
6. Optionally select a workout from the imported file, adjust its targets and save it as a template. A workout already imported from that file can still be selected; review any subsequent local corrections. Missing rest settings use Solift’s default and can be edited.

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
| Full Solift JSON backup | Separate format for restoring Solift’s own journal, including saved templates; not a Strong/Hevy account backup |

The implementation has been exercised with actual Strong and Hevy iPhone CSV exports, including a Chinese Strong export. Those checks do not guarantee every app version, locale, unit setting or future file format. No private source exports are published here.

## If a file fails

Cancel rather than repeatedly confirming an unexpected preview. Keep the original unchanged, check that it is a workout-history CSV, and record the error message and app versions. A malformed or unsupported file must be corrected or exported again; do not delete columns merely to bypass an error.

For help, send the header names and a minimal example using invented values, plus the error and selected units/time zone. Never post your entire export or backup in a public issue. Contact [support](https://hihihiai.com/solift/support) for private troubleshooting.
