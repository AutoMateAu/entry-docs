# Unified Inbox — Overview

The Unified Inbox is Entry's central hub for all email communications. It pulls emails from connected Outlook accounts and presents them in a single, organised view with AI-powered classification and priority scoring.

---

## How It Works

```
Outlook Mailbox → Entry Sync → Classification → Priority Scoring → Unified Inbox
```

1. **Sync** — Entry connects to your Outlook mailbox via Microsoft Graph API and syncs emails in real-time using push notifications
2. **Classify** — Each email is automatically classified using a 4-layer hybrid classifier (sender reputation, content analysis, thread context, and AI)
3. **Score** — Emails receive a priority score so the most important messages surface first
4. **Display** — Threaded conversations appear in the inbox, grouped and searchable

---

## Key Features

| Feature               | Description                                                    |
| --------------------- | -------------------------------------------------------------- |
| **Threaded view**      | Emails grouped by conversation thread                          |
| **AI classification**  | Automatic categorisation (enquiry, offer, maintenance, etc.)   |
| **Priority scoring**   | Important emails surface to the top                            |
| **AI draft replies**   | One-click draft generation using your knowledge base           |
| **Search**             | Full-text search across all synced emails                      |
| **Filters**            | Filter by status, category, priority, or date                  |

---

## Email Categories

Entry automatically classifies incoming emails into categories:

| Category            | Description                                    |
| ------------------- | ---------------------------------------------- |
| Property Enquiry    | Questions about listings or properties         |
| Offer / Negotiation | Purchase offers or price negotiations          |
| Maintenance         | Repair or maintenance requests                 |
| Lease / Rental      | Tenancy applications or lease queries          |
| General             | Everything else                                |

{% hint style="success" %}
Classification happens automatically on sync. No manual tagging required — though you can override categories manually if needed.
{% endhint %}

---

## Navigation

* **Inbox tab** — All incoming email threads
* **Sent tab** — Outgoing emails and replies
* **Drafts tab** — AI-generated drafts awaiting review
* **Archive** — Completed or dismissed conversations
