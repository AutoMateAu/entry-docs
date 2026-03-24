# Outlook Email

Entry uses Microsoft Graph API to connect to your Outlook mailbox for email sync, sending, and real-time push notifications.

---

## Connecting Outlook

1. Go to **Settings → Integrations → Outlook Email**
2. Click **Connect**
3. Sign in with your Microsoft 365 account and grant permissions
4. Entry will begin syncing your mailbox immediately

{% hint style="info" %}
Entry requires a **Microsoft 365 Business** or **Enterprise** account with Exchange Online. Personal Outlook.com or Hotmail accounts are not supported.
{% endhint %}

---

## What Entry Accesses

| Permission              | Purpose                                    |
| ----------------------- | ------------------------------------------ |
| **Read mail**            | Sync incoming emails to the unified inbox  |
| **Send mail**            | Send replies from within Entry             |
| **Manage subscriptions** | Set up push notifications for new emails   |

---

## How Sync Works

| Method           | Description                                                |
| ---------------- | ---------------------------------------------------------- |
| **Webhooks**      | Microsoft sends push notifications when new emails arrive  |
| **Polling**       | Backup sync every 15 minutes catches any missed messages   |
| **Full sync**     | Initial connection syncs recent email history               |

---

## Sending Email

When you reply to an email in the unified inbox (or approve an AI draft), Entry sends the reply through your Outlook account via Microsoft Graph `sendMail`. The email appears in your Outlook Sent Items as if you sent it directly.

{% hint style="success" %}
Replies sent through Entry are indistinguishable from replies sent through Outlook. Recipients see your normal email address, signature, and thread history.
{% endhint %}

---

## Disconnecting

1. Go to **Settings → Integrations → Outlook Email**
2. Click **Disconnect**
3. Email sync stops immediately
4. Existing synced emails remain visible in Entry but are no longer updated

---

## Troubleshooting

| Issue                         | Solution                                        |
| ----------------------------- | ----------------------------------------------- |
| Emails not appearing           | Check connection in Settings → Integrations     |
| "Token expired" error          | Disconnect and reconnect your Outlook account   |
| Webhook notifications stopped  | Entry auto-renews webhooks — if persistent, reconnect |
| Can't send replies             | Verify your Microsoft 365 license includes Exchange Online |
