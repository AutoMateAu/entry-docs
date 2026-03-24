# User Roles & Permissions

Entry uses role-based access control (RBAC) to manage what team members can do within your organisation.

---

## Roles

| Role       | Description                                                    |
| ---------- | -------------------------------------------------------------- |
| **Admin**   | Full access — manage settings, integrations, team members      |
| **Member**  | Standard access — inbox, clients, knowledge brain              |

---

## Permission Matrix

| Action                          | Admin | Member |
| ------------------------------- | ----- | ------ |
| View inbox                       | Yes   | Yes    |
| Send / reply to emails           | Yes   | Yes    |
| Generate AI drafts               | Yes   | Yes    |
| Manage clients                   | Yes   | Yes    |
| Upload knowledge documents       | Yes   | Yes    |
| Search knowledge brain           | Yes   | Yes    |
| Connect / disconnect integrations | Yes   | No     |
| Manage team members              | Yes   | No     |
| Organisation settings            | Yes   | No     |

---

## Changing Roles

Admins can change a team member's role:

1. Go to **Settings → Team**
2. Find the team member
3. Change their role using the role dropdown
4. Changes take effect immediately

{% hint style="warning" %}
There must always be at least one Admin in the organisation. You cannot demote the last remaining Admin.
{% endhint %}

---

## Removing Team Members

1. Go to **Settings → Team**
2. Click **Remove** next to the team member
3. Confirm the removal

Removed members lose access immediately. Their historical activity (sent emails, created clients) is preserved.
