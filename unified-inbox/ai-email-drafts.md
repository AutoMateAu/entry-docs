# AI Email Drafts

Entry uses your Knowledge Brain to generate context-aware email draft replies. The AI reads the incoming email, searches your uploaded documents for relevant information, and writes a professional response.

---

## How Draft Generation Works

```
Incoming Email → Analyse (extract queries) → Search Knowledge Base → Generate Draft → Human Review
```

1. **Analyse** — GPT-4o-mini reads the email and extracts 1–5 distinct queries or questions
2. **Search** — Each query runs a parallel vector search against your Knowledge Brain documents
3. **Re-rank** — Results are re-ranked for relevance using a cross-encoder model
4. **Draft** — GPT-4o generates a reply using the retrieved context
5. **Review** — The draft appears in your inbox for review, editing, and sending

---

## Confidence Score

Every draft includes a **confidence score** (0–1) indicating how well your knowledge base covers the email's questions.

| Score Range | Meaning                                                    |
| ----------- | ---------------------------------------------------------- |
| 0.8 – 1.0   | High confidence — knowledge base covers the topic well     |
| 0.5 – 0.79  | Medium — partial coverage, review carefully                |
| 0.0 – 0.49  | Low — knowledge base has limited relevant information      |

{% hint style="warning" %}
A low confidence score means the AI had limited context to work with. Review these drafts carefully and consider uploading more relevant documents to your Knowledge Brain.
{% endhint %}

---

## Source Attribution

Each draft lists the **source documents** and specific chunks that contributed to the response. This lets you verify the information and trace it back to your uploaded materials.

---

## Tips for Better Drafts

| Tip                                     | Why it helps                                        |
| --------------------------------------- | --------------------------------------------------- |
| Upload comprehensive FAQs               | Covers common enquiry patterns                      |
| Keep documents up to date               | Prevents outdated pricing or policy information     |
| Upload listing descriptions             | Enables accurate property-specific responses        |
| Add company policies                    | Ensures consistent responses about procedures      |
| Use specific, clear document titles     | Helps retrieval match the right content             |

{% hint style="success" %}
The more relevant documents you upload, the better your AI drafts will be. Entry's retrieval system finds the most relevant chunks automatically — you just need to provide the source material.
{% endhint %}
