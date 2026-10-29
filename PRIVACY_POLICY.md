# Privacy Policy for Friends Bell

**Effective Date:** YYYY-MM-DD <!-- Set to the publish date. -->

## 1. Introduction

This privacy policy explains what information **Friends Bell** ("the App") uses, what leaves your device, and how it is protected. Friends Bell is built by **Blink22**. It is free to use, with optional paid features (Friends Bell Pro) sold through Google Play.

You can use the App without an account. An account is optional: you create one with your phone number only if you want to send and receive **nudges** (short messages such as a wave or a hug) with friends who also use Friends Bell. Section 4 explains what an account adds.

By using Friends Bell, you agree to the handling of information described in this policy. We do not sell your information, and we do not use it for advertising.

---

## 2. Summary

| | Stays on your device | Sent to our service providers |
|---|---|---|
| Your contacts' names and photos | ✅ Yes, never uploaded | ❌ Never |
| Your contacts' phone numbers | ✅ Yes, unless you choose to find friends | Only with an account, and only if you allow finding friends: sent as hashed values, and never stored (Section 4) |
| Your groups, reminders, notes and swipe history | ✅ Yes, never uploaded | ❌ Never |
| Your phone number, display name and avatar color | | Only with an account: Google Firebase (Section 4) |
| Nudges you send and receive | | Only with an account: Google Firebase, deleted automatically after 30 days (Section 4) |
| Your phone number, when you sign in with WhatsApp | | Meta (WhatsApp), to send you a sign-in link (Section 4) |
| How you use the app (screens and feature events) | | ✅ Yes, Google Firebase, for analytics |
| Crash reports and diagnostics | | ✅ Yes, Google Firebase, for crash reporting |
| App installation identifiers | | ✅ Yes, Google Firebase, for analytics and crash reporting |
| Approximate location (country or city, derived from IP address) | | ✅ Yes, Google Firebase, for analytics |
| Pro purchase events (product, price) | | ✅ Yes, Google Firebase, for analytics |

Our service providers are **Google Firebase** and, for WhatsApp sign-in only, **Meta** (the WhatsApp Business Cloud API). They process this information on our behalf. Without an account, nothing in the "Only with an account" rows leaves your device. The App shows no ads and does not use the Android Advertising ID.

---

## 3. Information That Stays on Your Device

### Contacts

With your permission (**READ_CONTACTS**), the App reads the names, phone numbers and photos saved in your device's contacts. It uses them to build your daily contact cards, your groups and your reminders, and to start a call or message when you tap one. Before Android asks for this permission, the App explains what it reads and what leaves your device.

Your contacts are processed **on your device**. Friends Bell never uploads, sells or shares their names or photos. Their phone numbers leave your device only if you have an account and allow finding friends, as described in Section 4. When you tap Call or Message, the App hands the number to your phone's dialer or messaging app, and only because you asked.

### Your Friends Bell data

Your groups, reminder schedules, quick reminders and their notes, "Next" and "Later" lists, hidden contacts, swipe and action history, earned badges and preferences are stored in the App's private storage on your device. The on-device action history is used only to rank the people suggested to you. None of it is uploaded, with or without an account.

This data is excluded from Android cloud backups and from device-to-device transfers, so it does not leave your device that way either.

---

## 4. Your Account and Nudges (Optional)

### Signing in

You sign in with your phone number. To check that the number is yours, the App sends you either:

* **A sign-in link on WhatsApp.** If WhatsApp is installed, your phone number is sent to **Meta's WhatsApp Business Cloud API**, which delivers a "Verify account" message from the Friends Bell WhatsApp number. Tapping its button signs you in. The link works for 10 minutes, and only on the phone that asked for it. Meta processes your number and this message on our behalf. Its handling of WhatsApp messages is described in [WhatsApp's Privacy Policy](https://www.whatsapp.com/legal/privacy-policy).
* **A code by SMS,** sent by Google Firebase, if WhatsApp isn't installed or can't deliver the link, or if you choose a text message instead.

While you sign in, Google Firebase also processes your IP address and an app-integrity check (Google Play Integrity or, if that isn't available, reCAPTCHA), to keep out automated and fraudulent sign-ins.

### What we store, and for how long

Your account is stored with **Google Firebase** (Firebase Authentication and Cloud Firestore).

| Data | Why | Kept until |
|---|---|---|
| Your phone number and sign-in record | Sign you in | You delete your account |
| A protected copy of your number (a keyed hash) | Let friends who have your number saved find you | You delete your account |
| Your display name and avatar color | Show friends who a nudge is from | You delete your account |
| Your settings: who can nudge you, and the App's language | Apply your choices | You delete your account |
| Counts of your recent requests (for example, friend searches) | Prevent abuse | You delete your account |
| The people you block | Stop their nudges | You unblock them or delete your account |
| A notification token for each signed-in device, stored under the App's installation ID (with the app version) | Deliver nudges | You log out on that device, delete your account, or don't open the App for 60 days |
| Nudges you send and receive: who it's from and to, the type (for example a wave or a hug), and when it was sent, answered or returned | Deliver and show nudges | Deleted automatically after 30 days |

Nudges contain no text that you write, and they don't carry your phone number. Other Friends Bell users can see only your display name and avatar color, and only if they already have your number saved or you nudge them. In **Profile → Who can nudge me** you can choose **Nobody**, so friends can no longer find you or send you new nudges. Replies to nudges you sent still arrive.

### Finding friends

If you have an account and allow it (for example, by tapping **Find my friends**), the App finds which of your contacts already use Friends Bell. Before you allow it, the App explains what is sent. It turns each contact's phone number into a SHA-256 hash on your device and sends the hashes to our server, which compares them with the protected copies of our users' numbers and returns the matches. The hashes are used only for that check and are **never stored**. They are still your contacts' phone numbers in another form, so we treat them with the same care and send them only over an encrypted connection. Names and photos are never sent. Once you've allowed it, the App checks again from time to time, so friends who join later appear too, and when someone nudges you, it checks whether they are one of your contacts so it can show their name from your contacts. While you're logged out, nothing is checked. To stop it permanently, turn off Contacts access for Friends Bell in your device settings, or delete your account.

### WhatsApp sign-in records

When the App asks for a WhatsApp sign-in link, our server keeps, for each number:

* **A sign-in link record.** It is keyed by a protected copy of the number, not the number itself. It holds a hash of the link, a check that ties the link to your phone, the language of the message, WhatsApp's message ID and delivery status (sent, delivered, read or failed), and the times links were requested and used.
* **Fraud-prevention counters.** To stop people requesting links for numbers that aren't theirs, the server counts requests per device (by a hash of the App's installation ID) and per network (by a hash of the IP address), with short tags of the numbers requested from each.

These records are deleted automatically, usually within 3 days of the last link request. They aren't part of your account, and they expire on the same schedule whether or not you delete it.

### Server logs

Our servers keep technical logs to run and protect the service. They never contain a full phone number; where a log needs to tell numbers apart, it keeps only the last 4 digits. Logs may include account and nudge IDs, and are deleted automatically within 30 days.

---

## 5. Information Collected Automatically

To understand how the App is used and to fix crashes, the App uses **Google Firebase** (Google Analytics for Firebase, Firebase Crashlytics, Firebase Sessions and Firebase Installations). Google acts as our service provider. This information never includes your contacts' names, phone numbers or photos, or the text of your notes. We don't attach your phone number, display name or account ID to it either.

* **App interactions.** Screens viewed and feature events, such as a reminder being set, a card being swiped, or a nudge being sent, answered or received. These events carry only generic values, such as a card type, a nudge type, where in the App an action started, a count, or a rough time range. They never say who a nudge was to or from.
* **Crash logs and diagnostics.** When the App crashes: the stack trace, app version, device model, OS version and the App's state at the time. Also basic session and performance metadata.
* **Identifiers.** A Firebase installation ID and a Google Analytics app-instance ID. These identify an installation of the App. With an account, the installation ID is also stored with your notification token (Section 4). The App does **not** collect the Android Advertising ID.
* **Approximate location.** Google Analytics derives a coarse location, such as country or city, from your device's masked IP address. The App never requests location permission.
* **Purchase events.** When you buy Friends Bell Pro, Google Analytics records the purchase event (product ID, product name and price).

All of this information is encrypted in transit (HTTPS/TLS) and is deleted automatically: Google Analytics event data after 2 months, and Crashlytics crash data after 90 days.

Google's own privacy information is available at [https://firebase.google.com/support/privacy](https://firebase.google.com/support/privacy).

---

## 6. Purchases

Payments are handled entirely by **Google Play**. We never see or store your payment details. The App checks the purchase receipt that Google Play returns on your device and stores your Pro status locally, encrypted.

---

## 7. Permissions

| Permission | Why |
|---|---|
| Contacts | Show your contacts as cards, groups and reminders (on your device, see Section 3). With an account, and only if you allow it, find friends who use Friends Bell (Section 4). |
| Notifications | Deliver your reminders and, with an account, your nudges. |
| Alarms & reminders (exact alarms) | Make quick reminders ring at the exact time you set. |
| Full-screen notifications (optional) | Show a ringing quick reminder over the lock screen. Without it, the reminder appears as a normal notification. |
| Run in the foreground / vibrate / keep awake | Ring a quick reminder until you dismiss it. |
| Run at startup | Reschedule your reminders after the device restarts. |

The App does not request access to your call log, SMS, location, camera or microphone.

---

## 8. Your Choices and Data Deletion

* **Permissions.** You can revoke any permission at any time in your device settings. Without Contacts access, the App cannot suggest people or find friends.
* **Who can nudge you.** In **Profile → Who can nudge me**, choose **Nobody** to stop new nudges and stop friends from finding you. Replies to nudges you sent still arrive.
* **Delete your account.** In the App, go to **Profile → Delete account**. This deletes your account and the data linked to it right away. If you can't use the App, you can ask us by email. See [Delete Your Friends Bell Account](ACCOUNT_DELETION.md) for the steps and exactly what is deleted.
* **Delete your on-device data.** Uninstall the App, or clear its storage (Android Settings → Apps → Friends Bell → Storage → Clear storage). This permanently deletes all of your Friends Bell data from the device. It doesn't delete your account; delete that first.
* **WhatsApp messages.** A sign-in message we send you stays in your WhatsApp chat until you delete it there.
* **Analytics and crash data.** We don't attach your account ID, phone number or name to this data. It is deleted automatically within 90 days (see Section 5).

---

## 9. Children's Privacy

Friends Bell is **not directed to children under 13**. We do not knowingly collect personal information from children. If we learn that a child under 13 has provided us with personal information, we will delete it.

---

## 10. Security

Information sent to our service providers is encrypted in transit. Your Friends Bell data stays in the App's private storage, which other apps cannot read, and your Pro status is stored encrypted. Account data is protected by access rules: only you can read your private settings and your nudges, and other users can see only your display name and avatar color. The copy of your number that lets friends find you is a keyed hash, made with a secret key that is kept separately. No method of electronic storage or transmission is completely secure, but we use commercially reasonable measures to protect your information.

---

## 11. Changes to This Policy

We may update this policy from time to time. We will post the new version on this page and update the effective date above. Changes take effect when they are posted.

---

## 12. Contact Us

If you have questions or suggestions about this policy, contact us at:

📧 **developer@blink22.com**
