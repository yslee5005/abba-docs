---
layout: default
title: Privacy Policy — Abba
---

# Privacy Policy

**Last Updated: April 22, 2026**

## 1. Introduction

Abba ("we," "our," "the app") is a mobile prayer and Quiet Time companion built for Christians who want to pray more deeply. This Privacy Policy describes how Abba collects, uses, stores, and protects your information when you use the iOS app (Bundle ID: `com.ystech.abba`).

Abba is currently operated as an independent developer project. When we refer to "we" in this policy, we mean the Abba team. If Abba becomes a registered company in the future, this policy will be updated accordingly.

This policy applies worldwide. We follow the principles of the EU General Data Protection Regulation (GDPR), the California Consumer Privacy Act (CCPA), and the Korean Personal Information Protection Act (PIPA) where applicable.

## 2. Information We Collect

### 2.1 Account Information
Abba is **anonymous-first**. When you open the app for the first time, we create an anonymous user ID (UUID) so your prayers and settings can sync across sessions. You do not need to provide a name, email, or phone number to use Abba.

You may optionally sign in with **Apple Sign-In** or **Google Sign-In** to back up your data. In that case, we receive your email address and a unique identifier from Apple or Google. You can use "Hide My Email" with Apple Sign-In if you prefer.

### 2.2 Prayer Content (Core Data)
When you use Abba, we collect:
- **Audio recordings** of your spoken prayers
- **Transcripts** generated from those recordings
- **Meditation text and reflections** you write or generate
- **Scripture passages** you bookmark

This is the most sensitive data Abba handles, and we treat it with care. Your audio is stored in your own private folder on our secure storage. Only you can access it. We do not listen to it, share it, or use it for marketing.

### 2.3 Subscription Information
If you subscribe to Abba Pro, a third-party service called **RevenueCat** records your subscription status (active, expired, trial, etc.) along with the anonymous ID. We do **not** receive your credit card number — that stays with Apple.

### 2.4 Technical Information
- Device language (to set your default app language)
- Crash logs with personal data masked (via Sentry)
- Push notification token (FCM, optional — only if you enable notifications)
- App version and iOS version (for debugging)

## 3. How We Use Your Information

We use your information to:
- **Provide AI analysis** of your prayers and Quiet Time reflections (Google Gemini)
- **Sync your data** across sessions and devices
- **Manage your subscription** and entitlements
- **Fix bugs and improve the app** through crash reports
- **Send optional push notifications** (daily Quiet Time reminders) if you opt in

We **do not**:
- Show advertising of any kind
- Sell your data to anyone
- Share your prayer content with third parties (except the AI processing described below)
- Use your content to train AI models

## 4. Third-Party Services

Abba relies on a small number of trusted services to operate.

| Service | Purpose | Data Sent | Region |
|---|---|---|---|
| **Supabase** | Database & authentication | Anonymous ID, prayers, metadata | US / EU |
| **Google Gemini API** | AI analysis of prayers | Prayer text only | Google Cloud |
| **RevenueCat** | Subscription management | Anonymous ID, purchase receipts | US |
| **Sentry** | Crash reporting (PII-masked) | Error traces with emails, long transcripts, JWTs removed | US / EU |
| **Firebase Cloud Messaging** | Push notifications (optional) | FCM token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Optional account link | Email, provider ID | Apple / Google |

**Google Gemini:** Per Google's published policy for paid API usage, prayer content sent to Gemini is **not used to train Google's AI models**. Processing is transient.

**Sentry PII masking:** We apply masking rules before sending crash reports — emails, Korean transcripts longer than 50 characters, JWTs, and other identifiers are stripped.

## 5. Data Storage and Security

- All data in transit is encrypted via HTTPS (TLS 1.2+).
- Data at rest is protected by our database provider's encryption.
- **Row-Level Security (RLS)** in Supabase ensures you can only access your own data.
- Audio files are stored in per-user folders with access controlled by your authentication token.
- Access tokens are stored in iOS Secure Enclave (`flutter_secure_storage`), never in plain preferences.

We retain your data for as long as your account is active. If you delete your account, we remove your data within **30 days**, except where we are legally required to keep records (such as tax records for subscription purchases, which Apple/RevenueCat retain under their own policies).

## 6. Your Rights

You have the following rights over your personal data:

- **Access** — request a copy of the data we hold about you
- **Correction** — ask us to fix inaccurate information
- **Deletion** — ask us to delete your account and data (available in-app: Settings → Account → Delete Account, or by email)
- **Portability** — request an export of your data in a machine-readable format
- **Objection** — object to certain processing
- **Withdraw consent** — you can revoke consent for push notifications, AI processing, or account linking at any time

For GDPR (EU) and CCPA (California) residents, these rights are guaranteed by law. To exercise any right, email **rrallvv@gmail.com**. We respond within 30 days.

## 7. Children's Privacy

Abba is rated 4+ in the App Store. We do not knowingly collect information from children under 13 (COPPA) or under 16 (GDPR, in some EU countries) without verifiable parental consent. If you believe a child has provided personal information, please contact us and we will delete it immediately.

## 8. International Data Transfers

Our infrastructure is hosted in the United States and the European Union. By using Abba, you consent to your data being transferred to and processed in these regions. We rely on Standard Contractual Clauses (SCCs) where required.

## 9. Government and Legal Requests

We disclose user data only when legally required (valid subpoena, court order, or equivalent). We publish no transparency report yet, but we commit to notifying affected users when legally permitted.

## 10. Changes to This Policy

We may update this Privacy Policy as Abba evolves. When we make material changes, we will notify you in the app and update the "Last Updated" date at the top. Continued use of Abba after changes means you accept the updated policy.

## 11. Contact Us

Questions, requests, or complaints?

- **Email:** rrallvv@gmail.com
- **Response time:** within 30 days (usually sooner)

You also have the right to lodge a complaint with your local data protection authority (e.g., your EU member state DPA, the California Attorney General, or Korea's PIPC).
