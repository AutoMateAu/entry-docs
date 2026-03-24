# HubSpot CRM

Entry integrates with HubSpot for bidirectional contact and deal synchronisation. Connect your HubSpot account to keep client records in sync across both platforms.

---

## Connecting HubSpot

1. Go to **Settings → Integrations → HubSpot**
2. Click **Connect**
3. Sign in to your HubSpot account and authorise Entry
4. Entry will detect your HubSpot plan tier and configure sync accordingly

{% hint style="info" %}
Entry supports all HubSpot plans: **Free**, **Starter**, **Professional**, and **Enterprise**. Free and Starter plans use polling-based sync. Professional and Enterprise plans use webhooks for real-time updates.
{% endhint %}

---

## What Syncs

| Data Type    | Direction          | Description                          |
| ------------ | ------------------ | ------------------------------------ |
| **Contacts**  | Bidirectional ↔    | Name, email, phone, company          |
| **Deals**     | Bidirectional ↔    | Deal stage, value, associated contacts |
| **Owners**    | HubSpot → Entry    | Team member assignments              |
| **Notes**     | Entry → HubSpot    | Activity notes and email summaries   |

---

## Sync Behaviour

### Automatic Sync

* **Webhook plans (Pro/Enterprise):** Changes in HubSpot trigger real-time sync to Entry
* **Polling plans (Free/Starter):** Entry checks for changes every 15 minutes via a cron job

### Conflict Resolution

When the same record is modified in both Entry and HubSpot:

1. The most recent change wins (last-write-wins)
2. Phone numbers are normalised to Australian format during sync

---

## Disconnecting

1. Go to **Settings → Integrations → HubSpot**
2. Click **Disconnect**
3. Your synced data in Entry is preserved but no longer updated

{% hint style="warning" %}
Disconnecting stops all sync. Existing records remain in Entry but will not reflect future HubSpot changes until you reconnect.
{% endhint %}

---

## Troubleshooting

| Issue                        | Solution                                          |
| ---------------------------- | ------------------------------------------------- |
| Contacts not syncing          | Check connection status in Settings → Integrations |
| Duplicate contacts            | Merge duplicates in HubSpot, then re-sync         |
| Token expired                 | Disconnect and reconnect — Entry auto-refreshes tokens, but a manual reconnect may be needed after prolonged outages |
