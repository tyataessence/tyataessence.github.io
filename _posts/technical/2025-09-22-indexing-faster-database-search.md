---
layout: default
title: "Indexing for Faster Database Search."
date: 2025-09-22
categories: [Technical]
author: Rakesh Tyata
---

_Learn how SQL, Graph, Vector, and NoSQL databases use indexes to speed up queries — with simple visuals and examples._

Searching through a database without an index is like trying to find a word in a book by reading every page — slow and frustrating. Indexing acts like a **shortcut or map**, letting the database jump directly to the data you need.

This post will explain **how different types of databases use indexing** to speed up searches, with simple visuals and practical analogies.

---

## 1️⃣ SQL Databases

**Relational Database:** MySQL, PostgreSQL, SQLite, SQL Server, Oracle

- Columns are indexed (B-Tree or Hash) to quickly locate rows. 
- Idea behind Binary Tree is that data is splitted into 2 parts i.e. left child and right child in tree.
- Perfect for structured tables with clearly defined columns.

![DB Index]({{ '/assets/images/db_index.jpg' | relative_url }})

💡 Analogy: Book index → instantly jump to the page you want.

---

## 2️⃣ Graph Databases

**Relationship Database:** Neo4j, Amazon Neptune, TigerGraph, Orient DB, ArangoDB

- Index node properties (like `name`) to quickly locate starting points.
- For spatial data, use **Geohashing** or **Quadtrees** for fast location queries.
- In Geohashing, you divide into 2 parts (East/West or North/South), next split that half again and so on. 

![Graph Index]({{ '/assets/images/graph_index.jpg' | relative_url }})

💡 Analogy: Address book or map grid → find a starting point, then explore relationships.

---

## 3️⃣ Vector Databases

**Embedding Database:** Pinecone, Weaviate, Milvus, FAISS, Vespa
**Concept:**

- Store numerical embeddings (vectors).
- Use **Approximate Nearest Neighbor (ANN)** indexes to find similar items quickly.

![VectorDB Index]({{ '/assets/images/vectordb_index.jpg' | relative_url }})

💡 Analogy: Map of dots → jump to the closest neighborhood instead of scanning all points.

---

## 4️⃣ NoSQL Databases

**Non-Relational Database:** DynamoDB, CosmosDB, CassandraDB, MongoDB

### DynamoDB

- **Index Type:** Partition Key + optional Sort Key, Secondary Indexes
- 💡 Analogy: Locker system → main key = your locker, secondary index = other access points

### Cosmos DB

- **Index Type:** Partition Key determines logical partition, Auto-index for all fields
- 💡 Analogy: Super-smart library catalog indexing every word

### Cassandra DB

- **Index Type:** Partition Key + Clustering Key, Secondary Indexes exist but are limited in scale.
- 💡 Analogy: Filing cabinet → drawers = partition, sorted folders inside = clustering key

### Mongo DB

- **Index Type:** Field Indexes (single-field, compound, text); optional Shard Key
- 💡 Analogy: Library → shelves = shard (optional), books on each shelf sorted by indexed fields

---

## 📚 Quick Comparison Table

```
| DB Type      | Index Type                         | Analogy                      |
|--------------|------------------------------------|------------------------------|
| SQL DB       | B-Tree / Hash on columns           | Book index                   |
| Graph DB     | Node properties + Geohash/Quadtree | Address book / Map grid      |
| Vector DB    | ANN (Approx. Nearest Neighbor)     | Map of dots                  |
| DynamoDB     | Primary + Secondary Indexes        | Locker system                |
| Cosmos DB    | Auto-index all fields              | Smart library catalog        |
| Cassandra DB | Partition + Clustering Key         | Drawer with sorted folders   |
```

---

🧠 **Key Takeaway:** Indexes act as **shortcuts**. Whether in SQL, graphs, vectors, or NoSQL systems, they drastically reduce search time and make queries efficient.
