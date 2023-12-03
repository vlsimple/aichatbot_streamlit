# AI Persona Chatbot Project

## Project Overview

This AI Persona Chatbot combines OpenAI's GPT, Streamlit, and Pinecone to create a conversational AI that interacts with users via a chat interface. It leverages podcast transcripts stored in Pinecone's vector data store, enabling the chatbot to provide contextually rich responses based on the content.

## Workflow

1. **Embedding Podcasts**: Transcripts are processed using OpenAI API for vector embeddings and stored in Pinecone.
User Interaction: User queries are converted into vector embeddings by OpenAI API.
Similarity Search: Query vectors undergo similarity search in Pinecone's database to find relevant podcast segments.
Engaging ChatGPT: ChatGPT receives the query and matched context, generating coherent answers.
Delivering the Answer: The chatbot presents the full answer to the user.
