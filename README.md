# Semantic Search on Hospitality KPI Data Using OpenAI Embeddings

This project demonstrates how I built a natural language semantic search system using real-world hospitality KPI data. By transforming structured daily hotel performance data into descriptive text and generating vector embeddings with OpenAI’s `text-embedding-ada-002` model, I created a system that understands and responds to human-language queries about hotel performance.

---

## What I Did

- Loaded 3 years of daily hotel KPI data (Occupancy, ADR, RevPAR, Demand, Supply)
- Converted each row into a descriptive sentence capturing the business context
- Generated vector embeddings using OpenAI's `text-embedding-ada-002` model
- Implemented cosine similarity to perform semantic similarity search
- Enabled natural language queries such as:
  - *"Find days with low occupancy and high ADR"*
  - *"Show dates with high RevPAR"*

---

## Why This Project Matters

In traditional dashboards or BI tools, querying KPI data often requires filters, dropdowns, or knowledge of exact fields. This project brings **human-level understanding** to hotel performance data, enabling users to ask free-form questions and get accurate, relevant results based on meaning — not just keywords.

This has practical implications for:
- Hotel revenue managers and analysts
- Business intelligence automation
- RAG (Retrieval-Augmented Generation) applications
- Making data search intuitive and insight-driven

---

## Tech Stack

- **Python**, **Pandas**
- **OpenAI API** (`text-embedding-ada-002`)
- **Scikit-learn** for cosine similarity
- **Jupyter Notebook** for development

---

## How It Works

1. Descriptive sentences are created from raw KPI data (e.g., occupancy, ADR)
2. Sentences are embedded using OpenAI's model to generate high-dimensional vectors
3. A user query is also embedded into vector form
4. Cosine similarity is calculated between the query vector and all KPI vectors
5. The top 5 most semantically relevant rows are returned

---

## Example Queries

```text
"Find dates with low occupancy and high ADR"
"Show periods with high RevPAR"
"Which dates had weak performance?"
"Find days when demand exceeded supply"
