# Uploading Documents

Add documents to your Knowledge Brain to power AI email drafts and chatbot responses.

---

## How to Upload

1. Navigate to **Knowledge Brain** in the sidebar
2. Click **Upload Document**
3. Select your file (PDF, DOCX, XLSX, CSV, TXT, or Markdown) or paste text directly
4. Click **Upload**
5. Entry will process the document — this typically takes 10–30 seconds

---

## Processing Status

After uploading, your document moves through these stages:

| Status         | Meaning                                                |
| -------------- | ------------------------------------------------------ |
| **Processing**  | Text extraction and chunking in progress               |
| **Embedding**   | Vector embeddings being generated                      |
| **Active**      | Ready — included in search and draft generation        |
| **Error**       | Processing failed — check the document format          |
| **Inactive**    | Manually disabled — excluded from search               |

{% hint style="info" %}
Processing usually completes within 30 seconds for standard documents. Large PDFs or spreadsheets may take up to a minute.
{% endhint %}

---

## Text Entries

You can also add knowledge directly as text without uploading a file:

1. Click **Add Text Entry**
2. Enter a title and paste your content
3. Click **Save**

This is useful for quick FAQs, policy snippets, or information that doesn't exist in a document.

---

## Managing Documents

| Action          | How                                                     |
| --------------- | ------------------------------------------------------- |
| **View details** | Click a document to see its status, chunks, and metadata |
| **Toggle active** | Use the active/inactive toggle to include or exclude from search |
| **Delete**       | Click delete to permanently remove the document and all its chunks |

{% hint style="warning" %}
Deleting a document is permanent. All associated chunks and embeddings are removed. If you just want to temporarily exclude a document from search, use the **inactive** toggle instead.
{% endhint %}

---

## Best Practices

* **Keep documents current** — Outdated listings or pricing will produce inaccurate AI drafts
* **Use descriptive titles** — Helps you manage your library and improves retrieval
* **Upload one topic per document** — The chunking system works best with focused content
* **Review the Knowledge Summary** — Check what the AI extracted to ensure accuracy
