# Knowledge Brain — Overview

The Knowledge Brain is Entry's document intelligence system. Upload your agency's documents — listings, FAQs, policies, procedures — and Entry indexes them for AI-powered search and email draft generation.

---

## How It Works

```
Upload → Extract Text → Chunk (~400 tokens) → Embed (vector) + AI Extract → Store & Index
```

| Step               | What happens                                                        |
| ------------------ | ------------------------------------------------------------------- |
| **Upload**          | You upload a document (PDF, DOCX, XLSX, CSV, TXT, Markdown)        |
| **Extract**         | Entry extracts raw text from the file                               |
| **Chunk**           | Text is split into ~400-token chunks at sentence boundaries         |
| **Embed**           | Each chunk is converted to a 1536-dimension vector embedding        |
| **AI Extract**      | GPT-4o extracts structured content (FAQs, services, policies)      |
| **Index**           | Chunks and embeddings are stored in PostgreSQL with pgvector        |

---

## What Gets Extracted

When you upload a document, the AI extracts structured information in addition to the raw text:

* **FAQs** — Common questions and answers found in the document
* **Services** — Products or services your agency offers
* **Policies** — Rules, procedures, or terms mentioned in the document

This structured data is aggregated into a **Knowledge Summary** for your organisation, which the AI uses alongside vector search results when drafting emails.

---

## Key Concepts

| Concept              | Description                                                    |
| -------------------- | -------------------------------------------------------------- |
| **Document**          | An uploaded file or text entry in your knowledge base          |
| **Chunk**             | A ~400-token segment of a document, stored with its embedding  |
| **Embedding**         | A numerical vector representation used for similarity search   |
| **Knowledge Summary** | Aggregated FAQs, services, and policies across all documents   |

{% hint style="info" %}
Documents can be toggled **active/inactive**. Inactive documents are excluded from search results but not deleted — you can reactivate them at any time.
{% endhint %}

---

## Supported Formats

| Format     | Extensions          |
| ---------- | ------------------- |
| PDF        | `.pdf`              |
| Word       | `.docx`             |
| Excel      | `.xlsx`             |
| CSV        | `.csv`              |
| Plain text | `.txt`              |
| Markdown   | `.md`               |
