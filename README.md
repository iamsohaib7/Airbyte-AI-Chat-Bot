# AI-Powered E-Commerce Chatbot

A simple AI chatbot that lets users ask natural language questions about e-commerce data. It uses Airbyte to sync data from the Stripe API into a PostgreSQL database with vector embeddings. A Python-based chatbot connects to the database and answers user queries.

---

## Architecture Diagram

![Architecture Diagram](./Images/Chatbot%20Architecture.png)

---

## Project Overview

This project shows how to build an end-to-end AI data stack:

1. **Data Source**: Stripe API provides e-commerce transaction data.  
2. **Data Ingestion**: Airbyte connects to Stripe on a schedule and loads data into PostgreSQL.  
3. **Vector Store**: PostgreSQL with pgvector stores embeddings for quick semantic search.  
4. **Chatbot**: Python code uses the vector store and a language model to answer questions in natural language.  

---

## Features

- Automatic data syncing from Stripe via Airbyte.  
- Vector-based search for fast and relevant results.  
- Simple Python chatbot interface.  
- Notebooks for data generation and chatbot demo (PDF versions included).  

---

## Airbyte Sync Schedule

![Airbyte Schedule](./Images/Airbyte%20Sync.png)

_This shows our Stripe connector running every 24 hours, with successful syncs and error-recovery settings enabled._

---

## What I Learned

- Designing and implementing **custom connectors in Airbyte**, including handling authentication flows, pagination, and incremental sync for high-volume data sources.  
- Configuring **sync schedules and failure recovery** in Airbyte to ensure reliable, automated data ingestion.  
- Setting up a **Supabase PostgreSQL instance** and enabling the `pgvector` extension for efficient storage of vector embeddings.  

---
