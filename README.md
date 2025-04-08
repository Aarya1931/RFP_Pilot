# RFP_Pilot
# 🧠 RFPilot – Your AI Co-Pilot for RFP Mastery

RFPilot is a LangChain + Ollama-powered GenAI application that helps businesses understand, evaluate, and respond to Request for Proposals (RFPs) faster and more accurately using Retrieval-Augmented Generation (RAG) and agentic workflows.

## 🚀 Features

- 🔍 **Smart RFP Summarization** – Extracts the core of complex RFPs instantly.
- ✅ **Eligibility Assessment** – Verifies if your company fits the bid.
- 🏗️ **Proposal Structure Generator** – Lays out the skeleton of your proposal.
- 🧠 **Improvement Suggestions** – Refines your response strategy.
- 💡 **Tailored Recommendations** – Offers smart suggestions aligned with your strengths.
- 📝 **Draft and Final Proposal Generation** – Writes your first draft and polishes the final version.
- 🔗 **Document Retrieval with FAISS** – Find supporting documents with local vector search.
- 🤖 **Agent Workflows** – AI agent fetches relevant documents to support your response.

---

## 🛠️ Tech Stack

- **💬 LLM**: [Ollama](https://ollama.com/) (e.g., Gemma 2B or LLaMA3)
- **🧱 Framework**: [LangChain](https://www.langchain.com/)
- **🧠 Embeddings**: `OllamaEmbeddings`
- **📚 Vector Store**: `FAISS`
- **🧠 Agent Toolkit**: `langchain.agents`
- **🖼️ UI**: [Streamlit](https://streamlit.io/)
🧠 How It Works
🧩 1. RAG Pipeline
Chunks and embeds RFP documents.

Stores embeddings in FAISS for local, fast retrieval.

Custom prompts analyze summary, eligibility, structure, and recommendations.

🤖 2. Agent Workflow
A LangChain agent uses get_supporting_docs_tool() to search FAISS.

Enhances final output with fact-supported suggestions.

🔐 Security Note
If you load the FAISS index locally, enable allow_dangerous_deserialization=True only when:

You trust the source of the FAISS .pkl files.

You built the vectorstore yourself.
