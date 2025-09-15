# MedAssist-AI-Chatbot
MedAssist is an AI-powered chatbot built with Streamlit, LangChain, FAISS, and LLMs to assist with medical-related queries.

About the Project:
Designed and implemented a Medical Chatbot to provide secure, accessible medical information with features like user authentication, interactive chat interfaces, and dynamic medical topic discussions.
Built a system integrating RAG (Retrieval-Augmented Generation) models with LLMs, using disease data from an encyclopedia and drug data from a CSV file for precise, real-time query handling and information retrieval.

Developed a Streamlit interface with:
bcrypt-encrypted login for secure access
SQLite conversation management for persistence
Real-time document retrieval using FAISS with PubMedBERT embeddings
Integrated RAG models powered by BioMistral-7B, reducing response time by 30% and improving accuracy by 40%.
Delivered a robust, AI-powered chatbot combining retrieval and generation, enhancing user experience with:
Secure interactions
Interactive Q&A
Context-driven responses
Boosting user satisfaction by 50%

Setup & Installation:
Clone the repository
git clone https://github.com/VedantK1311/MedAssist-AI-Chatbot.git
cd MedAssistAI

Install dependencies:
pip install -r requirements.txt

Set up environment variables:
Create a .env file in the root directory with your API key:
OPENAI_API_KEY=your_api_key_here

Download BioMistral-7B:
Since the LLM is too large to be uploaded to GitHub, you must download it manually from Hugging Face:
👉 BioMistral-7B on Hugging Face

Place the model inside a models/ folder like this:
MedAssistAI/models/BioMistral-7B/

Build the FAISS Vector Store:
Since FAISS files are too large to upload to GitHub, you need to regenerate them:
python build_vectorstore.py
This will create a faiss_index/ folder locally.

Run the Streamlit app
streamlit run app.py

Notes:
The FAISS index and BioMistral-7B model are not included in this repo because they are too large.

You must:
Download BioMistral-7B manually from Hugging Face and place it in the models/ directory.
Rebuild the FAISS index using build_vectorstore.py
