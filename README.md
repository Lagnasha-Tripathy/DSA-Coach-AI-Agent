# 🧠 DSA Coach — AI-Powered Personalized DSA Learning & Feedback System

DSA Coach is an AI-powered learning platform designed to improve **how students solve Data Structures and Algorithms problems**, rather than simply telling them whether their answer is correct or incorrect.

The system analyzes a student's **problem-solving approach**, provides personalized feedback, identifies areas for improvement, and gives optimized hints to help students develop better problem-solving patterns.

## 🚀 Problem Statement

On traditional coding platforms, students usually receive only:

* ✅ Correct
* ❌ Wrong

This tells students **whether** their solution worked, but not **how good their approach was** or how they could improve it.

DSA Coach addresses this gap by evaluating the student's reasoning and guiding them toward more efficient and optimized solutions.

## 💡 Key Features

* 🔐 User authentication
* 📚 DSA question bank
* 📄 Upload personal DSA notes, PDFs and documents
* 🧩 Document chunking and processing
* 🔎 Semantic retrieval of relevant learning material
* 🤖 AI-powered approach evaluation
* 💬 Personalized feedback
* 💡 Progressive hints instead of directly revealing solutions
* ⚡ Optimization suggestions for time and space complexity
* 📊 Personalized learning experience
* 🧠 Memory-based interaction
* 📈 Rubric-based evaluation of problem-solving approaches

## 🏗️ System Architecture

```text
                    ┌──────────────────────┐
                    │      Student         │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   Streamlit UI       │
                    │  streamlit_app.py    │
                    └──────────┬───────────┘
                               │
                ┌──────────────┼──────────────┐
                ▼              ▼              ▼
          ┌──────────┐  ┌────────────┐  ┌───────────┐
          │  Agents  │  │ Retrieval  │  │  Rubric   │
          └────┬─────┘  └─────┬──────┘  └─────┬─────┘
               │              │               │
               └──────────────┼───────────────┘
                              ▼
                    ┌──────────────────────┐
                    │   Knowledge Base     │
                    │ PDFs / Notes / Data  │
                    └──────────────────────┘
                              │
                              ▼
                    ┌──────────────────────┐
                    │ AI Generated Feedback │
                    └──────────────────────┘
```

## 🛠️ Tech Stack

### Frontend

* Streamlit

### Backend / Application

* Python
* LangChain
* AI/LLM integration
* Agent-based workflow

### NLP / Retrieval

* Text embeddings
* Semantic search
* FAISS
* Document chunking
* Retrieval-Augmented Generation (RAG)

### Document Processing

* PDF processing
* DOCX processing
* TXT processing

### Data & Storage

* JSON
* Local vector/document storage

### Development Tools

* Git
* GitHub
* VS Code

## 📂 Project Structure

```text
DSA-Coach/
│
├── agents/
│   ├── graph.py
│   ├── memory.py
│   ├── nodes.py
│   ├── state.py
│   └── test_agent.py
│
├── data/
│   ├── memory.json
│   ├── txt/
│   └── uploads/
│
├── embeddings/
│   └── embed_store.py
│
├── ingestion/
│   ├── chunking.py
│   ├── document_loader.py
│   └── __init__.py
│
├── retrieval/
│   └── retrieve.py
│
├── rubric/
│   ├── rubric_generator.py
│   └── __init__.py
│
├── requirements.txt
├── rubric.json
├── streamlit_app.py
└── .gitignore
```

## 🔄 How DSA Coach Works

### 1. Student selects a DSA problem

The student chooses a problem from the available question bank.

### 2. Student provides their approach

Instead of immediately asking for the final solution, the student explains their intended approach.

### 3. AI evaluates the approach

The system evaluates factors such as:

* Logical correctness
* Algorithm selection
* Time complexity
* Space complexity
* Edge-case handling
* Optimization opportunities

### 4. Personalized feedback

The student receives feedback explaining what is good about the approach and what needs improvement.

### 5. Progressive hints

Instead of directly providing the answer, DSA Coach can provide hints that guide the student toward discovering the solution themselves.

### 6. Optimization

The system suggests how the solution can be improved in terms of efficiency and problem-solving strategy.

## 📚 RAG Pipeline

User-provided learning material goes through the following pipeline:

```text
PDF / DOCX / TXT
       ↓
Document Loader
       ↓
Text Extraction
       ↓
Chunking
       ↓
Embeddings
       ↓
Vector Store
       ↓
Semantic Retrieval
       ↓
Relevant Context
       ↓
AI Feedback
```

This allows DSA Coach to use the student's own learning material when generating feedback.

## ⚙️ Installation

### Clone the repository

```bash
git clone https://github.com/Shivashukla25/DSA_COACH-Feedback-generator-.git
cd DSA_COACH-Feedback-generator-
```

### Create a virtual environment

```bash
python -m venv .venv
```

### Activate the environment

Windows:

```bash
.venv\Scripts\activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Configure environment variables

Create a `.env` file and add the required API credentials.

**Never commit `.env` or API keys to GitHub.**

### Run the application

```bash
streamlit run streamlit_app.py
```

The application will open in your browser.

## 🌐 Deployment

The application can be deployed using **Streamlit Community Cloud**.

Deployment flow:

```text
GitHub Repository
       ↓
Streamlit Community Cloud
       ↓
Public Web Application
```

## 🎯 Future Improvements

* User performance analytics
* Difficulty-based personalized question recommendations
* Progress tracking
* More advanced code analysis
* Multi-language code evaluation
* Competitive programming mode
* Learning streaks and achievements
* Cloud database integration
* Improved AI-generated learning paths

## 👨‍💻 Team

**CodeCurry**

Built as an AI-powered personalized DSA learning and feedback system.

## 📄 License

This project is intended for educational and academic purposes.
