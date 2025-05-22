🧠 AtliQ Tees: Natural Language to SQL with LLM
An end-to-end LLM-powered application that allows users to interact with a MySQL database using natural language. Built using Google PaLM, LangChain, and Streamlit, this system empowers store managers to ask questions about inventory, sales, and discounts without needing SQL knowledge.



🚀 Project Overview
AtliQ Tees is a T-shirt store offering brands like Adidas, Nike, Van Heusen, and Levi's. All product data — including inventory, sales, and discounts — is stored in a MySQL database.

This project builds an intelligent interface where a store manager can ask:

“How many white Adidas t-shirts do we have left in stock?”

The system translates the question into an SQL query using LLM and retrieves the accurate answer from the database.

🧩 Tech Stack
LLM: Google PaLM (via Makersuite API)

Embeddings: Hugging Face

Frontend: Streamlit

Backend Framework: LangChain

Vector Store: ChromaDB

Database: MySQL

Learning Technique: Few-shot prompting

📸 Sample Use Cases
🧾 "How many total t-shirts are left in stock?"

👕 "How many Nike XS white t-shirts are available?"

💰 "What’s the inventory value for all S-size t-shirts?"

📉 "What’s the total sales amount if all small-size Adidas t-shirts are sold after discounts?"

📁 Project Structure
bash
Copy
Edit
4_sqldb_tshirts/
├── main.py                 # Streamlit app entry point
├── langchain_helper.py     # LangChain-based logic and SQL generation
├── few_shots.py            # Few-shot learning prompt templates
├── requirements.txt        # Python dependencies
├── .env                    # API keys and environment variables
└── database/
    └── db_creation_atliq_t_shirts.sql  # SQL script to create MySQL DB
⚙️ Setup & Installation
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/codebasics/langchain.git
cd 4_sqldb_tshirts
2. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
3. Configure API Key
Get your API key from Makersuite

Create a .env file in the project root:

bash
Copy
Edit
GOOGLE_API_KEY="your_api_key_here"
4. Set Up MySQL Database
Open MySQL Workbench (or similar)

Run the SQL script:

sql
Copy
Edit
database/db_creation_atliq_t_shirts.sql
▶️ Running the Application
Start the Streamlit web app:

bash
Copy
Edit
streamlit run main.py
The app will open in your browser, ready to take natural language questions.

🧠 How It Works
User Input: Store manager types a question.

LLM & LangChain: The system uses Google PaLM + LangChain to convert the question to SQL.

Execution: Query is executed on MySQL DB.

Answer Displayed: Clean, structured answer shown in the UI.

🌟 Features
Real-time SQL generation from natural questions

Hugging Face embeddings + ChromaDB for context management

Few-shot learning to improve SQL accuracy

Lightweight UI with Streamlit
