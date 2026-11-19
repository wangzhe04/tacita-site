---
layout: default
title: Tacita Privacy Policy
lang: en
permalink: /privacy/
---

# Tacita Privacy Policy

Effective date: November 20, 2026

## 1. Scope and who is responsible

This policy covers the Tacita app for iPhone and Android ("the app"), including its share extension.

The app is provided by **Zhe Wang**, an individual developer ("the Developer", "we"). For privacy questions or requests, email **tacita.app@gmail.com**.

## 2. In short

- **We don't run servers.** Your conversations, attachments, rules and keys stay on your device. The Developer cannot see or remotely access them.
- **Answers come from the AI provider you configure.** Content goes directly from your device to the provider whose API key you entered, without passing through us.
- **Before anything is sent, the app replaces detected sensitive content with placeholders or masks it**, and shows you what will be sent. Original values stay on your device and are restored there when the answer arrives.
- **No ads, no analytics, no crash reporting, no tracking.**
- Detection cannot be perfect, and we do not promise that nothing will ever leak. Check the preview before you send.

## 3. What stays on your device

**What is stored.** Conversations, your original text, model replies, the map between placeholders and original values, your rules and protected items, provider and search-service API keys and connection details, a receipt for each send, local statistics, a search index, and attachments you add (the original file and its extracted text). The free version's daily message count is also kept on the device.

**How it is protected.**
- This data lives in an encrypted database on your device. On iPhone the database key is kept in the Keychain, available only while the device is unlocked and never moved to another device. On Android it is protected by a non-exportable key in the system keystore.
- This data is **excluded** from iCloud backup, Google backup and device-to-device transfer.
- You can turn on an app lock (Face ID, fingerprint or device passcode) and hide the app in the app switcher.
- Text copied from the app is marked sensitive. On iPhone it stays on the local clipboard and expires after 2 minutes. By default a copy restores placeholders, but credentials stay masked.
- An image shared into the app is stored encrypted until the app picks it up, then deleted.

**Attachments and images.** Text extraction and image text recognition (OCR) happen on your device. Only the text you select is sent to a provider; original files, image pixels, and photo location and capture details are not.

## 4. What is sent to the AI provider you choose

The provider you connect (for example the built-in OpenAI or DeepSeek templates, or a compatible endpoint you enter) receives:

- **The protected version of your current message**: detected sensitive content replaced with placeholders, masked, or the whole message held back. Today's date is added.
- **Recent history from the same conversation**, protected again under the current rules. Other conversations are never included.
- A fixed note explaining the placeholders to the model, plus tool descriptions when you use web access or "suggest protection".
- **Attachments**: only the extracted, fully checked text you selected, and the file name.
- **Conversation titles (on by default; turn off in Settings › Model)**: after the first answer, one extra request with at most the first 600 characters of your first message (protected), without attachments or the answer.
- **Connection checks**: a request for the provider's model list, which includes your API key.

Providers also see connection information such as your IP address, and your API key (used for billing).

**Never sent**: original values of protected content, the placeholder map, original files and images.

How a provider stores and uses what you send, including whether it trains on it, is governed by its own terms. We cannot control that or recall content already sent. Read the provider's privacy policy before connecting. You pay provider fees directly to the provider; they are separate from the app's price.

## 5. Web search and page reading

Web access is off by default. It is used only after you turn it on in a conversation and confirm a one-time notice. There are two routes:

- **Search built into the provider** (currently only certain verified models): the provider decides what to search and which pages to open. The app cannot see the queries it actually sends.
- **Web access run by the app**: the model says what it wants to look up, and the app does it on your device. The possible recipients are listed below; the notice shown before you turn it on names the search source used in that conversation.
  - **General search** sends the query, with placeholders and protected content removed. A search is blocked if it contains anything you marked as secret. The query goes to one of the following, which bills it under its own pricing to your account there:
    - the search API of the provider you are connected to (currently DeepSeek, Kimi and Zhipu), using the same key;
    - a search service you added a key for in Settings › Web search (Brave Search, Tavily, Exa);
    - DeepSeek's search API, if you saved a DeepSeek key. **This can happen even when the conversation uses another provider's model**; the notice says so.
    - If none of these is available, no general search is made.
  - **Page reading**: your device connects to the website directly, as a browser would, so the site can see your IP address. Only URLs you wrote in your current message, or URLs that appeared in this turn's results, are read. Only HTTPS is used; no cookies or account details are sent, and local-network or on-device addresses are never contacted. For URLs taken from results, the site's robots.txt is checked first and the page is not read if the site disallows it.
  - **Encyclopedia**: Wikipedia (Wikimedia Foundation). The query is handled the same way as search terms.
  - **Exchange rates**: Frankfurter (reference rates published by the European Central Bank and other central banks). Only currency codes and an optional date are sent.

Page reading, encyclopedia and exchange rates are free and use no key.

Search terms and URLs are kept on the device for at most 7 days (cleared the next time you open the app).

## 6. Other connections

- **Purchases**: the one-time purchase goes through the Apple App Store (Google Play for Android, when available). The store handles payment; we never receive your card details. The app reads the store's purchase record on the device. There is no developer licence server and no device identifier is collected.
- **Links**: opened in the system browser only when you tap them, after showing the real domain. The app never loads remote images or link previews on its own.
- **Saving and sharing files**: only when you choose to through the system save or share screens.
- **The app connects to nothing else.** There is no analytics, advertising, crash-reporting or third-party tracking code, and no developer server. "Diagnostics" are generated on the device and only leave it if you copy them yourself; they contain no conversations, keys or placeholders.

If you email us, we receive your email address and message and use them only to reply. Please do not send API keys or private conversations by email.

## 7. In-app reporting

The current version **does not offer** in-app reporting and sends no reports. If we add it, we will update this policy first, and a report will be sent only after you review the full preview and confirm.

## 8. Encrypted backups and exports

- **Recovery backup**: encrypted with a passphrase you set. It contains conversations, the placeholder map (including original values), rules, **API keys**, receipts and attachments, but not purchase status or the daily count. It is saved only where you choose in the system save screen and is never uploaded automatically. Keep the backup and its passphrase safe.
- **Protected export and sharing**: sensitive content appears only as a category and number, without original values.

## 9. Permissions

- **iPhone**: Face ID (app lock only); App Group (only for the share extension's encrypted handoff). Files are picked with the system file picker, so no photo-library permission is needed.
- **Android**: network access; the app lock uses the system biometric or device credential prompt. Files are picked and saved with the system picker, so no storage permission is needed.
- The app does not request microphone, location, contacts, calendar or notification permissions.

## 10. Retention and deletion

- Conversations, the placeholder map, rules and saved keys: kept until you delete them.
- Receipts and web-request metadata: 90 days. Local statistics: 13 months. Search terms and URLs: at most 7 days.
- You can delete a conversation, all conversations, rules, statistics or a provider connection at any time. Uninstalling the app deletes all data on the device.
- To delete content already sent to a provider, follow that provider's process.

## 11. International processing

The provider you choose may process data outside your country or region (for example, OpenAI in the United States and DeepSeek in mainland China). Data goes directly from your device to the provider you choose, and, when web access is on, to the search services and websites listed in section 5; you decide whether and where it is sent. Using your own key does not by itself prevent international transfers.

## 12. Your rights

We do not collect or keep your personal information, so you can view, change, export and delete your data directly in the app. For information you send us by email, you can ask to access, correct or delete it. You may also complain to your local regulator.

**By region:**
- **Mainland China**: personal information of minors under 14 is sensitive personal information and requires a guardian's consent.
- **United States**: we do not sell personal information or "share" it for cross-context behavioral advertising.
- **Japan, Korea, Taiwan, Hong Kong and Macao**: your rights under local law to access, correct or delete are unaffected; contact us at the email above.

## 13. Children

The app is not designed for children. If you believe a child's personal information has been sent to us by email, contact us and we will delete it.

## 14. Security

We use on-device encryption, system key protection and encrypted transport (HTTPS), but no measure is perfectly secure. Detection and protection can miss things, so check the preview before sending.

## 15. Changes

When this policy changes, we update the effective date at the top. Material changes are announced in the app, and we ask for your consent again where the law requires it.

[中文版](../privacy-zh/)
