# Security & Data

Entry is built with multi-tenant security as a core principle. Your agency's data is strictly isolated from other organisations on the platform.

---

## Data Isolation

Every piece of data in Entry is scoped to your organisation. There is no cross-organisation data access.

| Layer                  | Protection                                                    |
| ---------------------- | ------------------------------------------------------------- |
| **Application**         | Every API request validates organisation membership           |
| **Database**            | Row-Level Security (RLS) enforces tenant isolation at the PostgreSQL level |
| **Session**             | Authenticated sessions with httpOnly cookies                  |

{% hint style="success" %}
Even if an application bug occurred, the database-level RLS policies prevent any query from returning data belonging to another organisation.
{% endhint %}

---

## Authentication

Entry supports multiple sign-in methods:

| Method              | Provider              |
| ------------------- | --------------------- |
| **Google OAuth**     | Sign in with Google   |
| **Microsoft OAuth**  | Sign in with Microsoft |
| **Email & password** | Standard credentials  |

All sessions are managed by NextAuth.js with secure, httpOnly session cookies.

---

## Encryption

| Data                     | Encryption                     |
| ------------------------ | ------------------------------ |
| **OAuth tokens**          | AES-256-GCM at rest            |
| **Data in transit**       | TLS/HTTPS everywhere           |
| **Database**              | Azure PostgreSQL encryption at rest |

---

## External Services

Entry connects to these external services — all over HTTPS with OAuth2:

| Service           | Purpose                                |
| ----------------- | -------------------------------------- |
| **OpenAI**         | AI classification and draft generation |
| **Microsoft Graph** | Outlook email sync and sending        |
| **HubSpot**        | CRM synchronisation                   |

{% hint style="info" %}
Your email content is sent to OpenAI for AI processing (classification, draft generation). OpenAI's API data usage policies apply. No email data is used for model training.
{% endhint %}

---

## Data Retention

* **Emails** — Synced emails are retained as long as your account is active
* **Documents** — Knowledge Brain documents are retained until you delete them
* **Client records** — Retained until manually deleted or account closure

---

## Reporting a Security Issue

If you discover a security concern, contact your Entry account administrator or reach out to the Entry support team directly.
