# Email Management

How to read, reply, and manage email threads in the Unified Inbox.

---

## Reading Emails

Click any thread in the inbox to open the conversation detail view. You'll see:

* **Full email thread** — All messages in the conversation, rendered with original formatting
* **Sender info** — Contact details and any linked client record
* **Classification badge** — The AI-assigned category
* **Priority indicator** — Visual priority level

---

## Replying to Emails

### Manual Reply

1. Open an email thread
2. Click **Reply** at the bottom of the conversation
3. Compose your message in the editor
4. Click **Send**

### AI-Assisted Reply

1. Open an email thread
2. Click **Generate Draft** (or the AI draft icon)
3. Entry will analyse the email, search your knowledge base, and generate a draft reply
4. Review the draft, edit if needed, then click **Send**

{% hint style="warning" %}
**AI drafts are never sent automatically.** Every draft is queued with `status: draft` and requires human review before sending. This is a safety feature that cannot be disabled.
{% endhint %}

---

## Thread Actions

| Action       | Description                                         |
| ------------ | --------------------------------------------------- |
| **Reply**    | Send a reply to the thread                          |
| **Archive**  | Move to archive (removes from active inbox)         |
| **Star**     | Mark as important for quick access                  |
| **Classify** | Override the AI classification manually             |

---

## Email Sync

Emails sync automatically via Outlook push notifications (webhooks). Entry also runs a periodic background sync to catch any missed messages.

{% hint style="info" %}
**Sync frequency:** Real-time via webhooks, with a backup polling sync every 15 minutes.
{% endhint %}

If emails aren't appearing, check:

1. Your Outlook connection is active in **Settings → Integrations**
2. Your Microsoft 365 account has Exchange Online enabled
3. The webhook subscription hasn't expired (auto-renewed by Entry)
