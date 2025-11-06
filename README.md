# 🧠 Text Summarizer using LangChain & Groq API

This project is a **Text Summarization System** built with **LangChain**, **Groq API**, and **Python**.  
It takes a long speech or text as input and produces a **concise, meaningful summary** — with the ability to **translate** the summary into multiple languages.

---

## 🚀 Features

- ⚙️ **LLM-Powered Summarization:** Uses **Groq’s Gemma-7B-It model** for fast and high-quality text summarization.  
- 🌍 **Multilingual Support:** Summaries can be translated into different languages dynamically.  
- 🔒 **Environment Variable Security:** API keys are securely loaded using `python-dotenv`.  
- 🧩 **Prompt-Driven Workflow:** Uses LangChain’s `PromptTemplate` and `LLMChain` for structured, reusable logic.  
- 📄 **Jupyter Notebook-Based Implementation:** Simple, visual, and easy to experiment with.

---

## 📁 Project Structure

Text_Summarizer/
│
├── text_summarization.ipynb # Main notebook for summarization logic
├── requirements.txt # All dependencies
├── .env # API keys (excluded from Git)
├── .gitignore # Ignoring venv and secret files
└── venv/ # Virtual environment (excluded)

yaml
Copy code

---

## ⚙️ Installation and Setup

### 1️⃣ Clone the repository
```bash
git clone https://github.com/aaryan7174/Text_Summarizer.git
cd Text_Summarizer
2️⃣ Create a virtual environment
bash
Copy code
python -m venv venv
3️⃣ Activate the environment
Windows (PowerShell):

bash ```

Copy code

venv\Scripts\activate
macOS/Linux:

bash
Copy code
source venv/bin/activate
4️⃣ Install dependencies

bash
Copy code
pip install -r requirements.txt
5️⃣ Create a .env file
Inside your project folder, create a file named .env and add your keys:

ini
Copy code
GROQ_API_KEY=your_groq_api_key_here
LANGCHAIN_API_KEY=your_langchain_api_key_here
⚠️ Never share or commit your API keys.
GitHub will automatically block commits containing sensitive keys (as you experienced earlier).

🧠 How It Works
Loads environment variables with dotenv.

Initializes the Groq-powered ChatGroq model (Gemma-7b-It).

Uses LangChain’s PromptTemplate to define a summarization + translation prompt.

Executes an LLMChain to generate a concise summary.

Optionally translates the output into any specified language (e.g., Hindi, French).

💡 Example
Input Speech:

"My parents impressed on me the value of hard work, keeping promises, and treating people with respect..."

Generated Summary (Hindi):

"यह भाषण मेहनत, ईमानदारी और सम्मान के मूल्यों को नई पीढ़ी तक पहुँचाने के महत्व पर केंद्रित है।"

🧰 Tech Stack
Component	Description
Python	Core programming language
LangChain	Framework for prompt templating and LLM orchestration
Groq API	High-speed inference for LLMs
dotenv	Secure key management
Jupyter Notebook	Interactive development

🧩 Requirements
shell
Copy code
langchain>=0.2.0
langchain-groq>=0.1.0
python-dotenv
tiktoken
Install using:

bash
Copy code
pip install -r requirements.txt
🔐 Security Notes
Keep your .env file private.

.gitignore ensures .env and venv/ are never uploaded to GitHub.

Regenerate keys if accidentally exposed.

🌟 Future Enhancements
Add Streamlit/Flask UI for text input and real-time summarization.

Support for multiple summarization models.

Integrate speech-to-text for summarizing spoken audio.


