# RAG Document Assistant: Querying the EU AI Act with LangChain

Developed Oct 2025–Jan 2026 as part of IBM RAG course; refactored and published March 2026.

**Stack:** Python · LangChain (LCEL) · Groq (Llama 3.3 70B) · HuggingFace Embeddings · ChromaDB · PDFPlumber

* A conversational RAG agent that answers questions about the EU AI Act (144 pages) in a grounded and hallucination-resistant way.
* Incorporated prompt engineering to handle out-of-context queries, and conversation memory for coherent multi-turn conversations.
* Built with LangChain's modern LCEL pipeline, replacing the deprecated `ConversationalRetrievalChain` with `create_history_aware_retriever` 
and `create_retrieval_chain`. 


## Setup
1. `pip install -r requirements.txt`
2. Create a `.env` file in the project root:
```
   GROQ_API_KEY=your_key_here
```
   Get a free key at [console.groq.com](https://console.groq.com)

3. Open the notebook

## Data

This project uses the EU AI Act (Regulation 2024/1689) as its source document,
included in `data/eu_ai_act.pdf`. The document is EU legislation and freely
available in the public domain via [EUR-Lex](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32024R1689).

## Future work
- Add a Gradio chat UI for interactive use without running the notebook
- Compare performance across different open-source models
