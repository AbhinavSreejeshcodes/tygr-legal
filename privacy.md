# Privacy Policy

**Last updated: 30 August 2026**

This policy explains what tygr collects, why, who else sees it, and how to get
rid of it. It describes the tygr iOS app and nothing else.

tygr is operated by Abhinav Sreejesh ("we", "us"). For anything in this policy,
including a request to access or delete your data, write to
**support@tygr.app**.

---

## The short version

- We collect what the app needs to work: your account, your onboarding answers,
  and the workouts you log.
- We do not track you, run ads, or use an analytics SDK. There is no advertising
  identifier in the app and nothing is sold or shared with data brokers.
- You can delete your account and everything in it from inside the app, at any
  time: **Progress → Settings → Delete Account**.

---

## What we collect

### Account details

When you create an account we receive, through our authentication provider
Clerk:

- your email address
- your first and last name, if your sign-in method provides one
- your profile image URL, if your sign-in method provides one
- an account identifier that Clerk generates

If you sign in with Apple and choose to hide your email, we receive Apple's
private relay address and never see your real one.

### Onboarding answers

The questions asked when you first open the app: your date of birth, your
experience level, your preferred weight unit, how many days a week you train,
your training goal, and whether you want workout reminders.

Your date of birth is used to check you are old enough to use the app and to
inform training recommendations. We store the date; we do not use it for
anything else.

### Training data

Everything you log: exercises, sets, reps, weights, session duration and when
each session happened; the routines you save; and the programs the AI coach
generates for you.

### Coach conversations

The messages you send the AI coach, and its replies. These are stored **on your
device only** — they are not saved to our servers. Each message is sent to our
server to be answered, and is not retained there after the reply comes back.

### Subscription status

If you subscribe to tygr Pro, Apple gives the app a signed receipt. We send that
receipt to our server, which verifies Apple's signature and stores a single
date: when your subscription runs out. **We never receive your payment details.**
Those stay with Apple.

### Device integrity

To stop the AI features being abused by anything other than the real app, each
install registers a key with Apple's App Attest service. We store the resulting
key identifier and public key. This identifies the *app install*, not you, and
cannot be used to track you across other apps.

### Usage counts

A count of how many AI generations and coach messages you have used in the
current period, so daily and weekly limits can be enforced.

### What we do **not** collect

- No location data.
- No contacts, photos or calendar.
- No Apple Health or HealthKit data. tygr does not integrate with Health.
- No advertising identifier (IDFA), and no cross-app or cross-site tracking.
- No third-party analytics or crash-reporting SDK.

---

## Microphone and speech

If you use the microphone to talk to the coach, audio is captured only while the
recording view is open, and only after you grant microphone and speech
recognition permission.

Transcription uses Apple's Speech framework. Where your device supports on-device
recognition, the audio never leaves your phone. Where it does not, iOS sends the
audio to Apple for transcription under
[Apple's privacy policy](https://www.apple.com/legal/privacy/). We never receive
or store the audio itself — only the text you choose to send, after you have had
the chance to edit it.

---

## Who else processes your data

We use three service providers. Each processes data on our behalf, under
contract, and none of them is permitted to use it for their own purposes.

| Provider | What it handles |
|---|---|
| **Clerk** | Authentication. Holds your email, name and profile image. |
| **Supabase** | Database and server functions. Holds your profile, workouts, routines, programs, usage counts and subscription expiry. |
| **Google** | The Gemini model that answers coach messages and generates programs. |

**What is sent to Google:** your training goal, experience level, preferred unit,
days per week, session length, equipment, the names and set-and-rep counts of
your saved routines, a summary of your recent training, and the text of your
message.

**What is never sent to Google:** your name, your email address, your date of
birth, or your account identifier. Google does not receive anything that
identifies you personally.

Apple processes your subscription purchase and, where on-device recognition is
unavailable, your dictated audio.

We do not sell your personal information, and we do not share it for cross-context
behavioural advertising.

---

## Why we are allowed to hold it

If you are in the UK or EEA, our lawful bases under the UK GDPR and GDPR are:

- **Performance of a contract** — for your account, your training data and your
  subscription status. Without these the app cannot function.
- **Legitimate interests** — for App Attest and usage counts, to protect the
  service from abuse and control costs. We consider this proportionate because
  neither identifies you personally.
- **Consent** — for microphone access and for notifications. You can withdraw
  either at any time in iOS Settings, and the rest of the app carries on working.

---

## How long we keep it

Your account data and training history are kept for as long as your account
exists.

When you delete your account, everything listed above is erased from our database
immediately and your authentication record is deleted from Clerk. Backups made
before the deletion are overwritten on our providers' normal rotation, within 30
days.

Coach conversations live on your device, so they go when you delete your account
or remove the app.

---

## Your rights

You can access, correct, export or delete your data. Most of it you can do
yourself:

- **Delete everything** — Progress → Settings → Delete Account. This is
  immediate and cannot be undone.
- **Correct your details** — through the app's onboarding answers and Settings.

For anything else, including a copy of your data in a portable format, email
**support@tygr.app** and we will respond within 30 days.

If you are in the UK or EEA you also have the right to object to processing, to
restrict it, and to complain to your data protection authority — in the UK, the
Information Commissioner's Office at [ico.org.uk](https://ico.org.uk).

If you are a California resident, you have the right to know what we collect, to
delete it, to correct it, and not to be discriminated against for exercising
those rights. We do not sell or share personal information as those terms are
defined by the CCPA.

---

## Children

tygr is not intended for anyone under 13, and we do not knowingly collect data
from children under 13. If you believe a child has created an account, email
**support@tygr.app** and we will delete it.

---

## Security

Traffic between the app and our servers uses TLS. Database rows are protected by
row-level security policies, so an authenticated user can read and write only
their own rows. Model API keys are held as server-side secrets and are never
present in the app.

No system is perfectly secure, and we cannot guarantee absolute security.

---

## International transfers

Our providers operate in the United States and elsewhere. Where data leaves the
UK or EEA it is transferred under the UK International Data Transfer Addendum or
the EU Standard Contractual Clauses, as applicable.

---

## Changes

If we change this policy we will update the date at the top. If the change is
significant we will tell you in the app before it takes effect.

---

## Contact

**support@tygr.app**
