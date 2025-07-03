# 🤖 Resume Analyzer AI (Langchain + Groq + Flask)

##### An intelligent Resume Analyzer web application that matches candidate resumes against job descriptions using cutting-edge LLMs. Built using **Langchain**, **Groq (LLaMA3)**, **Flask**, and **HuggingFace Embeddings**.

---

## 🚀 Features

- 📄 Upload & parse multiple resumes (PDF / text-based)
- 🧠 Extracts meaningful information using LLM (LLaMA3 via Groq)
- 🔍 Compares resume against job description using semantic search
- 📊 Returns structured JSON analysis with:
  - Match Score
  - Missing Skills
  - Matched Keywords
  - Suggestions for Improvement
- 💻 Easy-to-use Flask frontend
- 🗂️ Uses vectorstore-based retrieval (FAISS or Chroma)
- 🧪 Fully local or cloud-deployable

---

## 🛠️ Tech Stack

| Layer             | Technology                     |
|------------------|--------------------------------|
| Backend LLM       | Groq API (LLaMA3 8B)           |
| Framework         | Langchain (v0.2+)              |
| Embeddings        | HuggingFaceEmbeddings          |
| File Parsing      | PyMuPDF                        |
| Frontend          | Flask + HTML form              |
| Retrieval         | FAISS                          |

---

## 📁 Folder Structure

# Resuma_Analyzer/

├── app.py # Flask web interface

├── cv_analyzer.py # Core logic (Langchain chains)

├── helper.py # Helper functions (embedding, parsing)

├── resume_parser.py # Output parser using Pydantic

├── Uploads_Files/ # Folder where resumes are uploaded

├── templates/ 

│ └── index.html # Simple HTML interface

├── requirements.txt # Python dependencies

└── README.md # Project report


---

## ⚙️ Setup Instructions

### 1. Clone the repo
git clone https://github.com/your-username/resume-analyzer.git
cd resume-analyzer

## 2. Create virtual environment
python -m venv venv
venv\Scripts\activate    
## 3. Install dependencies
pip install -r requirements.txt
## 4. Add your Groq API key
In cv_analyzer.py:
llm = ChatGroq(temperature=0, model="llama3-8b-8192",
               groq_api_key="your_groq_api_key")

## ▶️ Run the App
python app.py
Visit 👉 http://127.0.0.1:5000 in your browser.

## 📊 Sample Output (JSON)

{
  "match_score": "82%",
  
  "matched_skills": ["Python", "Machine Learning", "Pandas"],
  
  "missing_skills": ["Deep Learning", "AWS"],
  
  "summary": "The resume matches well with the job description but lacks cloud experience.",
  
  "recommendations": [
  
    "Include experience with cloud platforms like AWS or GCP.",
    
    "Add deep learning projects or coursework."
    
  ]
}

## 🧪 Future Improvements
###   ✅ Drag & drop file uploader

###   ✅ Streamlit version (no HTML needed)

###   ✅ Downloadable PDF reports

###   ✅ Email integration for sharing results

# 🧑‍💻 Author
## Made with ❤️ by Malik Anas
## For demo, freelance or enterprise use.
