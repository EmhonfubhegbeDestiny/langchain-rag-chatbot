# LangChain RAG Chatbot

A retrieval-augmented generation (RAG) chatbot that scrapes a webpage, 
embeds its content, and answers natural-language questions grounded in 
that source material — with full conversation memory.

## How it works
1. Loads content from a given URL using `WebBaseLoader`
2. Splits the text into chunks with `RecursiveCharacterTextSplitter`
3. Embeds the chunks and stores them in a FAISS vector store
4. Retrieves relevant chunks based on the user's question
5. Passes the context + chat history to GPT-4o-mini to generate an answer

## Tech stack
- LangChain
- FAISS (vector search)
- OpenAI (GPT-4o-mini)
- Python

## Setup
1. Clone this repo
2. Install dependencies: `pip install -r requirements.txt`
3. Add your OpenAI API key to a `.env` file
4. Run the notebook and call `chat("your question here")`