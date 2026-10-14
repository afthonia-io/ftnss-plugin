---
name: ftnss
description: Use with the FTNSS connector to read an athlete's workouts, heart rate, readiness and Library, build timers and routines, create and change their goals and training plans, correct a workout's sets, and download their data.
---

FTNSS is the athlete's training app, and these tools read and change their FTNSS account.

- Call `get_athlete` first: it gives their units, their time zone and asOf, when their phone last synced. State the units you use, and say the data is as of that sync; answers also hold changes made through these tools since.
- A null timeZone means the phone hasn't sent one yet: every local day and time is UTC, and there is no setting for the athlete to change.
- Before you create, update, delete or correct anything, show the athlete what you will change and get their yes. Changes reach their phone at its next sync, and each one can be undone in Settings › Assistants on the phone, or with `undo_change` for changes made through this connection.
- FTNSS gives fitness estimates and no medical advice.
