# Masrofaty — Google Play Data Safety (Summary)
**Last updated:** 2026-02-16

---

## A) What data is collected? (What the app/SDKs may process)

### 1) On-device (default)
- Financial data entered by the user: transactions, categories, budgets, goals (stored locally).
- Receipt images and OCR text (stored locally by default).

### 2) Ads (Free tier)
- If ads are enabled, ad SDKs may process data required for ad delivery/measurement.  
  You must declare SDK collection/sharing correctly in Play Console Data Safety. [1](https://www.4each.com.br/threads/flutter-flutter-isar-database-v3-1-0-1-namespace-not-defined.53836/)[2](https://github.com/isar/isar/issues/277)

### 3) Cloud OCR (Pro, optional)
- If the user enables Cloud OCR, receipt images may be uploaded to the OCR endpoint for extraction.

### 4) Backups/Sync (optional)
- If enabled, backups may be exported/imported by the user, or uploaded to the user’s cloud account.

---

## B) Is any data shared with third parties?
- Ads SDK providers (if ads enabled).
- Cloud OCR provider (if enabled).
- Cloud backup provider (if enabled).

Google requires declaring third-party SDK data handling in Data Safety. [1](https://www.4each.com.br/threads/flutter-flutter-isar-database-v3-1-0-1-namespace-not-defined.53836/)[2](https://github.com/isar/isar/issues/277)

---

## C) Security practices
- Data stored locally by default.
- Optional app lock (PIN/biometrics).
- HTTPS for network transfers where applicable.

---

## D) Data deletion
- In-app “Delete all data” option (recommended).
- Uninstall removes local data.
- Cloud backups can be deleted by the user from their cloud account.

---

## E) GDPR consent (EEA/UK) if Ads enabled
- If serving ads to EEA/UK users, consent and privacy options should be handled using UMP. [3](https://play.google.com/store/apps/details?id=com.castor.expensestrack&hl=ar)[4](http://moneylover.me/)
