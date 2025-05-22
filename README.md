# AtliQ Tees: Natural Language to SQL Database System

![AtliQ Tees](atliq_tees.png)

An end-to-end LLM project that enables natural language interactions with a MySQL database. This system converts user questions in plain English into SQL queries and executes them against a t-shirt store's inventory database.

## 🎯 Overview

AtliQ Tees is a t-shirt store management system where store managers can ask questions about inventory, sales, and discounts in natural language. The system intelligently generates and executes SQL queries to provide accurate answers.

**Example Queries:**
- "How many white color Adidas t-shirts do we have left in stock?"
- "How much sales will we generate if we sell all extra-small size t-shirts after applying discounts?"

## 🚀 Features

- **Natural Language Processing**: Ask questions in plain English
- **Intelligent SQL Generation**: Automatically converts questions to accurate SQL queries
- **Real-time Database Interaction**: Direct connection to MySQL database
- **User-friendly Interface**: Clean Streamlit web application
- **Multi-brand Support**: Handles Adidas, Nike, Van Heusen, and Levi's inventory

## 🛠️ Tech Stack

- **LLM**: Google Palm
- **Embeddings**: Hugging Face
- **Frontend**: Streamlit
- **Framework**: LangChain
- **Vector Store**: ChromaDB
- **Database**: MySQL
- **Learning Approach**: Few-shot learning

## 📋 Prerequisites

- Python 3.8+
- MySQL Server
- Google API Key (from [Google MakerSuite](https://makersuite.google.com))

## ⚡ Quick Start

### 1. Clone the Repository
```bash
https://github.com/Abdulla-1234/langchain_genai_retail.git
cd atliq-tees-nlp-sql
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Environment Setup
Create a `.env` file in the project root:
```bash
GOOGLE_API_KEY="your_api_key_here"
```

### 4. Database Setup
Run the SQL script in your MySQL Workbench:
```bash
database/db_creation_atliq_t_shirts.sql
```

### 5. Launch the Application
```bash
streamlit run main.py
```

The web application will open in your browser at `http://localhost:8501`

## 💬 Sample Questions

Try asking these questions in the application:

- "How many total t-shirts are left in stock?"
- "How many t-shirts do we have for Nike in XS size and white color?"
- "What's the total price of inventory for all S-size t-shirts?"
- "How much sales will we generate if we sell all small size Adidas shirts after discounts?"

## 📁 Project Structure

```
atliq-tees-nlp-sql/
├── main.py                 # Main Streamlit application
├── langchain_helper.py     # LangChain implementation
├── few_shots.py           # Few-shot learning prompts
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables
├── database/
│   └── db_creation_atliq_t_shirts.sql
└── README.md
```

## 🔧 Configuration

### Environment Variables
- `GOOGLE_API_KEY`: Your Google Palm API key

### Database Configuration
Ensure your MySQL server is running and accessible. Update database connection parameters in `langchain_helper.py` if needed.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🎉 Acknowledgments

- Built with [LangChain](https://langchain.com/)
- Powered by [Google Palm](https://ai.google.dev/)
- UI created with [Streamlit](https://streamlit.io/)

---

⭐ **Star this repository if you find it helpful!**
