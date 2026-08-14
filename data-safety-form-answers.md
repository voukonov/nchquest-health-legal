# Play Console Data Safety form — answers for NchQuest Health

Reference for filling out **Play Console → Policy → App content → Data safety**.
Reflects the app as of Phase 2 (2026-08-14): on-device storage only, Health Connect
read-only for Steps/Heart Rate/Resting Heart Rate, no network transmission of user data.

**Re-check this document every time app functionality changes** (e.g. if cloud sync,
crash reporting, or an analytics SDK is ever added) — an inaccurate Data Safety form is
itself a Play Store policy violation, separate from whatever the new feature is.

## Does your app collect or share any of the required user data types?

**Answer: Yes** (the app *collects* health data — it just doesn't *share* or *transmit* it).

Google's definitions: "Collect" = the data leaves the user's device or is stored beyond
the current session, whether or not it's transmitted off-device — on-device-only storage
still counts as "collected" for this form. "Share" = transmitted to a third party. NchQuest
Health collects but does not share.

## Data types to declare

| Data type | Collected? | Shared? | Purpose | Optional? |
|---|---|---|---|---|
| Health info → Fitness info (steps) | Yes | No | App functionality | No — core to Activity tab |
| Health info → Fitness info (heart rate) | Yes | No | App functionality | No — core to Activity tab |
| Health info → Health info (blood pressure, symptoms, medication) | Yes | No | App functionality | No — core to Vitals tab |

Leave every other category (Location, Personal info, Financial info, Messages, Photos/
Videos, Audio, Files/docs, Calendar, Contacts, App activity, App info & performance, Device
or other IDs) set to **not collected**. This app has no account system, no analytics SDK,
no ad SDK, and no crash reporter — there is nothing else to declare truthfully.

## Security practices section

| Question | Answer |
|---|---|
| Is all user data encrypted in transit? | Not applicable — no user data is transmitted off the device. If the form forces a choice, select "Data isn't transmitted" for each data type rather than claiming in-transit encryption that doesn't apply. |
| Can users request that data be deleted? | Yes — describe as: "Users can delete individual entries in-app, or delete all data by uninstalling the app or clearing its storage in Android Settings, since no data is stored on a server." |
| Do you commit to following the Play Families Policy? | Not applicable — app is not targeted at children (see privacy policy §7). |
| Has an independent security review been conducted? | No |

## App access

Since there's no login/account system, when Play Console asks "does your app require
account creation," answer **No** — all features are available without any sign-in.

## Health Connect declaration

Play Console separately asks about Health Connect integration in the store listing setup
(distinct from the Data Safety form). Declare:
- Data types read: Steps, Heart Rate, Resting Heart Rate
- Data types written: none
- Link to the same hosted privacy policy URL used everywhere else

## Before submitting

1. Confirm the privacy policy is live at its public URL (see `legal/privacy-policy.html`)
   and that the URL is the same one entered in Play Console's "Privacy policy" field, the
   Health Connect permission-rationale field, and the in-app disclaimer link.
2. Re-read this file against whatever the app *actually does* at submission time — not
   what it did when this file was written. If Phase 2's scope changed (e.g. Sleep/Weight/
   Hydration/Blood Pressure Health Connect write access gets implemented later), add rows
   for those data types before submitting.
