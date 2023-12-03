# AI Persona Chatbot Project
## Project Overview
This AI Persona Chatbot combines OpenAI's GPT, Streamlit, and Pinecone to create a conversational AI that interacts with users via a chat interface. It leverages podcast transcripts stored in Pinecone's vector data store, enabling the chatbot to provide contextually rich responses based on the content.
## Workflow
1. **Embedding Podcasts**: Transcripts are processed using OpenAI API for vector embeddings and stored in Pinecone.
2. **User Interaction**: User queries are converted into vector embeddings by OpenAI API.
3. **Similarity Search**: Query vectors undergo similarity search in Pinecone's database to find relevant podcast segments.
4. **Engaging ChatGPT**: ChatGPT receives the query and matched context, generating coherent answers.
5. **Delivering the Answer**: The chatbot presents the full answer to the user.
## Project Structure
* `app.py`: Streamlit web application integrating GPT model and Pinecone for response generation.
* `utils.py`: Functions for text embeddings and semantic search using OpenAI API and Pinecone.
* `render.py`: HTML templates and functions for formatting chat messages.
* `prompts.py`: Templates for system and user messages to guide response generation.
## Requirements
* OpenAI API key
* Pinecone API key, environment, and index name
* Python dependencies (install via `pip install -r requirements.txt`)
## Setting Up
1. Create z.streamlit/secrets.tomlz in the app folder.
2. Add API keys and Pinecone details:
```
OPENAI_API_KEY = "XXXXXXX"
PINECONE_API_KEY = "XXXXXXX"
PINECONE_ENVIRONMENT = "XXXXXXX"
PINECONE_INDEX_NAME = "XXXXXXX"
```
3. Install dependencies: `pip install -r requirements.txt`
## Running the Chatbot
Execute `streamlit run app.py` in the command line within the project folder. This will launch the chatbot in a web browser.
## Conclusion
This AI Persona Chatbot serves as a multi-functional assistant, offering insights from a specific persona's data, ideal for personalized advice or coaching.



