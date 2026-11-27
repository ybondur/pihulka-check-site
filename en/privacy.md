---
title: Privacy Policy
lang: en
permalink: /en/privacy/
alt_url: ../../uk/privacy/
alt_lang: uk
alt_label: Українська
---

# Pihulka Check Privacy Policy

Version of {{ site.privacy_version_date.en }} (`{{ site.privacy_version }}`)

---

## In short

- **Without an account, everything stays on your phone.** We don't receive your medications, schedules or dose history.
- **With an account, we keep a copy on our server**, so your schedule isn't lost when you reinstall the app or move to a new phone.
- **Your phone schedules the reminders itself.** They work without the internet and without our server.
- **No ads, no analytics, no trackers.** We don't sell your data or share it with advertisers.
- **You can delete your account in the app.** Your data is removed from the server immediately and from backups within 7 days.

---

## 1. Who we are and who is responsible for your data

Pihulka Check is built and run by a small team of developers.

The controller of your personal data, meaning the person responsible for it: **Yaroslav Bondur**, a private individual.

For any question about your data, write to **{{ site.support_email }}**. We reply within 30 days.

## 2. How the app works

Pihulka Check reminds you to take your medications and repeats the reminder until you respond.

- Reminders are local iOS notifications. Your phone schedules them itself, so they don't pass through our server or Apple's servers.
- The server does only two things: backup and sync between your phones. Without an account, the app doesn't contact it.

## 3. What data we process

### 3.1. Without an account

Your medications, schedules, dose history and settings are stored only on your phone. We don't see or receive them.

If you delete the app, this data is deleted with it.

### 3.2. If you create an account

| Data | Why | Legal basis |
| --- | --- | --- |
| **Email** | Signing in; the email with your password reset code | Performance of a contract (the terms of use) |
| **Password** | Signing in. We store only a one-way hash (bcrypt) and never see the password itself | Performance of a contract |
| **Language and time zone** | Emails in your language; dose times and history in the right time zone | Performance of a contract |
| **Medications:** name, form, dose, note (e.g. "after food"), colour, icon | Backup and sync | **Your explicit consent** (see 3.3) |
| **Schedules:** days, times, course start and end dates, repeat settings | Same | **Your explicit consent** |
| **Dose history:** whether a dose was taken, skipped, snoozed or left unanswered; when, and in which time zone | History and adherence rate on all your phones | **Your explicit consent** |
| **Reminder settings:** repeat interval and window, snooze length, sound | The same behaviour on all your phones | Performance of a contract |
| **Consents:** which document you accepted, which version, when, and in which language | To prove that consent was given | Legal obligation |
| **Sign-in security data:** hashes of session tokens, hash of the one-time password reset code | Account security | Legitimate interest (protecting your account) |

### 3.3. Health data

Medication names, schedules and dose history can reveal your health condition. The law gives this data special protection:

- Article 9 of the GDPR;
- Article 7 of the Law of Ukraine "On Personal Data Protection".

That's why we ask for separate **explicit consent** to process it when you register. You can't create an account without this consent. The app still works fully without an account.

You can withdraw your consent at any time by deleting your account (section 8). Your data will then stay only on your phone.

### 3.4. IP address

The server doesn't keep a request log. It holds your IP address only in memory, to limit the number of requests from one address and to protect against password guessing.

Your IP address may appear in the server's technical error log. That log is limited in size and is overwritten automatically.

### 3.5. What we don't collect

- your name, phone number or date of birth;
- your location, contacts or photos;
- data from Apple Health;
- advertising identifiers.

The app contains no third-party SDKs for analytics, advertising or crash reporting.

## 4. Data on your phone

- Your medications, schedules, settings and the last 90 days of dose history are stored in the app's storage on your phone. Older history is loaded from the server when you open the History screen.
- The key that keeps you signed in is stored in the iOS Keychain.
- When you **sign out**, this data stays on your phone and your reminders keep working. To remove it from the phone, delete the app.

**Notifications on the lock screen.** The reminder text includes the medication name. If you don't want others to see it, go to Settings → Notifications → Show Previews in iOS and choose "When Unlocked".

## 5. Who we share data with

We don't sell or rent your data, or share it with advertisers or data brokers.

Only services that do one specific job for us receive data:

| Service | What it does | What it receives |
| --- | --- | --- |
| **Hetzner Online GmbH** (Germany) | Runs the server in the EU that hosts our API and database | Stores all account data listed in section 3.2 |
| **Brevo** (France) | Sends the email with your password reset code | Your email address and the one-time code. **The email contains no medication data** |
| **Google** (Gmail) | The {{ site.support_email }} inbox you write to us at | Your message and the address you sent it from |
| **Apple** | The App Store; crash reports, only if you've turned on "Share With App Developers" in iOS | What Apple collects under its own privacy policy. Apple receives none of your data from us |

We disclose data to public authorities only when the law requires it, and only to the extent required.

**Where your data is stored.** Our server and the service that sends our emails (Brevo) are located in the European Union. EU countries are parties to Council of Europe Convention No. 108 on the protection of personal data, so Ukrainian law recognises that they provide an adequate level of protection. We don't transfer your account data outside the EU.

The exception is emails you send us at {{ site.support_email }}: Google stores them, including on servers outside the EU.

## 6. How long we keep data

| Data | Retention |
| --- | --- |
| Account data (section 3.2) | Until you delete your account |
| Database backups | Taken daily; the 7 most recent are kept. Deleted data disappears from backups within 7 days |
| Session tokens | 30 days from last use; expired tokens are deleted daily |
| Password reset code | Valid for 15 minutes; expired codes are deleted daily |
| Server technical error log | Overwritten automatically when it reaches its size limit |

## 7. How we protect data

- All connections to the server use HTTPS (TLS).
- Passwords, session tokens and reset codes are stored only as hashes.
- The database can't be reached from the internet: only our API connects to it.
- Only members of our team who maintain the server have access to it and to the database.
- The sign-in key on your phone is kept in the iOS Keychain.

No system is completely secure. If a breach threatens your rights, we'll notify you and the supervisory authority within the time limits set by law.

## 8. Your rights

| Right | How to use it |
| --- | --- |
| **Access** — to know what data we hold | Everything we store is visible in the app. We'll send a full copy on request |
| **Rectification** | Edit your medications, schedules or settings in the app |
| **Erasure** | In the app: "Account" → "Delete account". Your data is removed from the server immediately and from backups within 7 days |
| **Portability** — to get your data in a machine-readable format | Write to us and we'll send you a JSON file |
| **Withdrawing consent** to the processing of health data | Delete your account. The app keeps working on your phone without an account |
| **Restriction and objection** | Write to us |
| **Complaint** | In Ukraine, the Ukrainian Parliament Commissioner for Human Rights (ombudsman.gov.ua). In the EU, the data protection authority of your country |

We reply to email requests within 30 days. We may ask you to confirm that the account is yours, for example by writing from the address it's registered to.

## 9. Children

Pihulka Check isn't intended for children under 16. We don't knowingly collect their data. If a child has created an account, write to us and we'll delete it.

## 10. Changes to this policy

Each version is identified by a date (currently `{{ site.privacy_version }}`). We'll tell you about significant changes in the app. If a change concerns health data, we'll ask for your consent again.
