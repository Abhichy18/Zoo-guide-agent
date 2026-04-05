
# 🦁 Zoo Guide Agent (ADK + LangChain + GCP)


An AI-powered Zoo Tour Guide Agent built using **Google ADK, LangChain, and Cloud Run**.  
This agent intelligently answers user queries about zoo animals by combining **internal zoo data + external knowledge (Wikipedia)**.



---

## 🚀 Features

- 🤖 Multi-Agent Architecture (using Google ADK)
- 🔍 Smart Research using Wikipedia (LangChain Tool)
- 🧠 Sequential Workflow (Research → Response Formatting)
- ☁️ Deployed on Google Cloud Run
- 🔐 Secure environment handling using `.env`
- 📊 State management using ToolContext

---

## 🏗️ Architecture

This project uses a **Sequential Agent Workflow**:

1. **Greeter Agent**
   - Takes user input
   - Stores prompt in state using `ToolContext`

2. **Researcher Agent**
   - Uses:
     - 📚 Wikipedia Tool (external knowledge)
     - 🐾 Zoo data (internal context)
   - Decides which tool(s) to use
   - Generates `research_data`

3. **Response Formatter Agent**
   - Converts research into user-friendly output
   - Makes response conversational & engaging

---
## 🛠️ Tech Stack

- Python
- Google ADK (Agent Development Kit)
- LangChain
- Wikipedia API
- Google Cloud Run
- Google Cloud Logging

---

## 📂 Project Structure

```bash
Zoo-guide-agent/
│
├── agent.py          # Main agent workflow (multi-agent logic)
├── requirements.txt  # Project dependencies
├── __init__.py       # Python module initialization
├── .gitignore        # Ignored files (env, cache, etc.)
└── .env              # Environment variables (not uploaded for security)
```

---

## 🔌 **API Reference**

This project uses multiple Google Cloud APIs to enable deployment, CI/CD, and AI capabilities:

* **Cloud Run API (`run.googleapis.com`)**
  Used to deploy and run the AI agent as a scalable serverless service.

* **Artifact Registry API (`artifactregistry.googleapis.com`)**
  Stores and manages container images securely for deployment.

* **Cloud Build API (`cloudbuild.googleapis.com`)**
  Builds the container image from source code using serverless CI/CD.

* **Vertex AI API (`aiplatform.googleapis.com`)**
  Connects the application with Gemini models for AI-powered responses.

* **Compute Engine API (`compute.googleapis.com`)**
  Provides underlying infrastructure support required by various cloud services.

## ⚙️ Setup Instructions

```bash
git clone https://github.com/Abhichy18/Zoo-guide-agent.git
cd Zoo-guide-agent
pip install -r requirements.txt
```

Create a `.env` file:

```
MODEL=your-model-name
```

Run the project:

```bash
python agent.py
```

---

## 🧠 How It Works

* User gives a query (e.g., “Tell me about lions”)
* **Greeter Agent** stores the prompt
* **Researcher Agent** fetches data from:

  * Zoo data (internal)
  * Wikipedia (external)
* **Response Formatter Agent** combines everything into a final answer
## ⭐ Future Improvements

* 🌐 Add real-time zoo database integration
* 🎤 Voice-based interaction (speech-to-text + text-to-speech)
* 🌍 Multi-language support
* 🖥️ Build a frontend UI (Streamlit / React)
* 📱 Mobile-friendly interface
* 🧠 Add memory for personalized responses

---

## 💡 Inspiration

This project is inspired by **Google Cloud Codelabs (ADK Agent Deployment)** and the concept of building **real-world AI agents** that combine internal data with external knowledge to solve user queries intelligently.

## 🔗 Links

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhishek-choudhary18/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://x.com/Abhichy18)

## 🤝 Collaborators
- **Anushka Sharma**: [https://github.com/AnushkaSharma05](https://github.com/AnushkaSharma05)

