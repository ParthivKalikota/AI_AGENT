This project implements a sophisticated AI agent capable of interacting with various tools to answer user queries, retrieve information from custom documents (RAG - Retrieval Augmented Generation), perform web searches, and even generate detailed reports. The agent leverages the power of LangChain for orchestration, NVIDIA AI Endpoints for advanced language and embedding models, Milvus for vector storage, and Tavily for web search capabilities.

The core idea is to create an intelligent system that can decide which tool to use based on the user's intent:

1.  Ingest Documents: Load and process PDF documents to build a knowledge base.
2.  Query Internal Knowledge Base: Retrieve information from the ingested documents using a vector database (Milvus).
3.  Perform Web Search: If information isn't found internally, use Tavily Search to find answers on the web.
4.  Generate Reports: Create comprehensive reports on specified topics by breaking them down into sub-topics, gathering information, and synthesizing it.

5.  ## Features

PDF Ingestion: Easily load and process PDF documents to create a searchable knowledge base.
Vector Database (Milvus): Stores document embeddings for efficient semantic search and retrieval.
NVIDIA AI Endpoints Integration: Utilizes powerful NVIDIA language models (Nemotron-3 70B) for generation and embedding models (Llama-3.2 EmbedQA) for semantic understanding.
Multi-Query Retriever: Enhances retrieval quality by generating multiple perspectives on a query.
Tavily Search Integration: Provides up-to-date web search capabilities for general knowledge queries.
Report Generation Tool: A specialized tool that can construct multi-paragraph reports on a given topic by dynamically generating sub-topics, retrieving information for each, and synthesizing them.
Conversation History Management: Maintains a trimmed conversation history to keep context while preventing excessive token usage.
ReAct Agent: Employs the ReAct (Reasoning and Acting) framework for the agent's decision-making process, allowing it to reason about which tool to use.

## Technologies Used
Python: The primary programming language.
LangChain: Framework for building LLM applications.
`langchain-nvidia-ai-endpoints`: For integrating NVIDIA LLMs and embedding models.
`langchain-milvus`: For Milvus vector database integration.
`langchain-tavily`: For web search capabilities.
`python-dotenv`: For managing environment variables (API keys).
`pypdf`: For loading PDF documents.
Milvus: Open-source vector database.
Tavily Search API: Web search API.
