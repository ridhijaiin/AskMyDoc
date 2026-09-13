# AskMyDoc
PROBLEM STATEMENT:-
Users need quick, accurate answers from a specific set of documents, but searching through them manually is slow, and a general chatbot can't answer from your documents with confidence. This project builds a system that answers questions using only the given documents, and points back to the exact source for every answer.

Retrieve relevant document chunks using hybrid search (BM25 keyword search + vector semantic search).
Rerank the retrieved chunks with a cross-encoder so the most relevant ones surface first.
Generate answers from an LLM that uses only the retrieved chunks, with citations pointing to the source.
Evaluate the system with Ragas metrics (faithfulness, answer relevance, context precision) and gate it in CI so quality can't silently regress.

DELIVERABLE:-
A working "Ask My Docs" app where you can ask a question about your chosen documents and get a cited answer, plus a metrics report showing how well it performs (e.g., "faithfulness 0.85, answer relevance 0.78") and a CI check that fails if those numbers drop.