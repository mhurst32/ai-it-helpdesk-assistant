AI Internal IT Helpdesk Assistant

A lightweight AI-powered helpdesk assistant that answers common Microsoft 365 IT questions using a local FAQ database and (optionally) an LLM.
Designed as a practical demo project for IT operations, Upwork clients, and AI engineering portfolios.

⭐ Overview

The goal of this project is to show how AI can streamline internal IT support by providing fast, consistent answers to everyday Microsoft 365 questions such as password resets, MFA setup, file sharing, device enrollment, and more.

This assistant:

Reads from a structured FAQ file you can edit

Searches for the best-matching answer

Uses an LLM fallback when no FAQ entry exists

Runs in a simple Streamlit web interface

Is easy to understand, extend, and deploy

This repository acts as a sample AI IT helpdesk tool, demonstrating beginner-friendly Python, documentation, and real-world IT problem-solving.

🚀 Features

🔍 FAQ-based retrieval using JSON

🤖 Optional OpenAI fallback for complex/unlisted questions

🖥️ Streamlit UI for easy demos

🗂️ Modular folder structure

📘 Prebuilt FAQ with 20+ Microsoft 365 questions

🔐 Supports .env for API keys (no hardcoded secrets)

🧩 Use Cases

This project demonstrates skills useful for:

IT administrators (especially Microsoft 365)

AI engineers building helpdesk automation

Upwork / freelance portfolio projects

Small business IT support

Internal tools for ticket deflection

RAG-style (Retrieval Augmented Generation) demos

📂 Project Structure
ai-it-helpdesk-assistant/
│
├── app.py                         # Main Streamlit application
├── faq/
│   └── faq_it_helpdesk.json       # Local IT FAQ database
├── data/
│   └── examples.md                # Example questions and answers
├── .env.example                   # Template for API keys
├── README.md
└── requirements.txt

🛠️ Tech Stack

Python 3.10+

Streamlit — UI

OpenAI API (optional)

JSON — FAQ storage

dotenv — API key management

▶️ How to Run Locally
1. Clone the repo
git clone https://github.com/yourusername/ai-it-helpdesk-assistant.git
cd ai-it-helpdesk-assistant

2. Install dependencies
pip install -r requirements.txt

3. Add your OpenAI key

Create a file named .env:

OPENAI_API_KEY=your_api_key_here


(Optional — app still works with FAQ only.)

4. Run the app
streamlit run app.py


The app will open in your browser at:
http://localhost:8501

📝 Example Questions

You can ask things like:

“How do I reset my Microsoft 365 password?”

“How do I set up MFA?”

“My OneDrive says it’s out of sync — what should I do?”

“How do I add a shared mailbox?”

“Why can’t I share files with someone outside my organization?”

📘 FAQ Data File Format

faq_it_helpdesk.json looks like:

[
  {
    "question": "How do I reset my Microsoft 365 password?",
    "answer": "Go to https://aka.ms/sspr, verify your identity, and follow the steps to set a new password."
  },
  {
    "question": "How do I set up MFA?",
    "answer": "Visit https://aka.ms/mfasetup and follow the prompts to enroll the Authenticator app or phone number."
  }
]


Feel free to customize or expand it.

🔧 How It Works (Simple Version)

User enters a question into the Streamlit UI

App searches the FAQ JSON using keyword similarity

If a close match is found → answer from FAQ

If no match → fallback to OpenAI model

Display response back to the user

📌 Future Enhancements (Optional)

These are not required for the demo but great next steps:

Add vector embeddings + semantic search

Connect to a SharePoint or M365 API

Logging + analytics dashboard

Role-based responses (admin vs employee)

Voice input + speech output (Siri-like mode)

Integration with Intune/Defender alerts

🎯 Why This Project Matters

This is exactly the type of small-but-real AI solution businesses are beginning to adopt.

It demonstrates:

Practical AI application

Internal IT automation

Real M365 knowledge

Beginner-friendly Python + Streamlit

Clean documentation

A portfolio-ready deliverable

Perfect for freelance work or showcasing AI engineering skills.

📄 License

MIT License
Free to use, modify, and build upon.
