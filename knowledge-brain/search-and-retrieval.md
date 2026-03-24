# Search & Retrieval

How Entry finds the right information from your Knowledge Brain when generating AI responses.

---

## How Search Works

```
Query → Embed → Vector Search (top 10) → Re-rank (top 3) → Return results
```

1. **Embed the query** — Your search query (or the AI's extracted questions from an email) is converted to a vector embedding
2. **Vector search** — pgvector performs a cosine similarity search across all active document chunks, returning the top 10 matches
3. **Re-rank** — GPT-4o-mini scores each result for relevance to the specific query, selecting the top 3
4. **Return** — The most relevant chunks are returned with source attribution

---

## Manual Search

You can search your Knowledge Brain directly:

1. Go to **Knowledge Brain**
2. Use the **Search** bar
3. Enter your query in natural language (e.g., "What are the office hours?" or "Pet policy for rentals")
4. View matching document chunks ranked by relevance

---

## Search in Email Drafts

When generating an email draft, the AI automatically:

1. Extracts 1–5 queries from the incoming email
2. Runs each query against your Knowledge Brain in parallel
3. Uses the combined results as context for the draft

You don't need to search manually — the draft generation pipeline handles retrieval automatically.

---

## Improving Search Results

| Action                           | Effect                                          |
| -------------------------------- | ----------------------------------------------- |
| Upload more documents            | Broader coverage = better matches               |
| Use natural language in docs     | Matches how questions are asked in emails        |
| Keep documents focused           | One topic per document improves chunk relevance  |
| Deactivate outdated documents    | Prevents stale info from surfacing               |

{% hint style="success" %}
Entry uses **semantic search**, not keyword matching. It understands meaning, so "What time do you open?" will match a document that says "Business hours: 9am–5pm Monday to Friday" even though the exact words don't overlap.
{% endhint %}
