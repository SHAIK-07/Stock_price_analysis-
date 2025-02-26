# 🚀 CHAT WITH DB

## 📚 Overview

This application allows users to interact with a MySQL database using natural language queries. It leverages Large Language Models (LLMs) to generate SQL queries, retrieve relevant results, and display insights. The system uses LangChain, Google Gemini, Hugging Face Embeddings, and Chroma for vector storage and few-shot learning.

## ✨ Features

- **🗣️ Natural Language Querying:** Converts user queries into SQL.
- **🎓 Few-Shot Learning:** Enhances accuracy using relevant past examples.
- **🔍 Embeddings & Vector Store:** Uses ChromaDB and Hugging Face for similarity-based example selection.
- **🛢️ Supports MySQL Database:** Queries are optimized for MySQL.
- **📊 Real-Time Insights:** Fetches and displays relevant data from structured tables.

## 🛠️ Tech Stack

- **Frontend:** Streamlit (if applicable)
- **Backend:** Python (LangChain, SQLAlchemy, dotenv, pymysql)
- **LLM:** Google Gemini via LangChain
- **Embeddings & Vector DB:** Hugging Face, ChromaDB
- **Database:** MySQL

## 📥 Installation

1. **Clone the Repository**

    ```bash
    git clone <repo-url>
    cd <repo-name>
    ```

2. **Create a Virtual Environment**

    ```bash
    python -m venv venv
    source venv/bin/activate  # For macOS/Linux
    venv\Scripts\activate     # For Windows
    ```

3. **Install Dependencies**

    ```bash
    pip install -r requirements.txt
    ```

4. **Set Up Environment Variables** Create a `.env` file and add:

    ```ini
    GOOGLE_API_KEY=your_google_api_key
    DB_USER=root
    DB_PASSWORD=root
    DB_HOST=localhost
    DB_NAME=atliq_tshirts
    ```

## 🚀 Usage

1. **Run the Application**

    ```bash
    python app.py
    ```

2. **Interact with the System**

    - Input natural language queries.
    - Get structured SQL query responses.
    - View extracted insights.

## 📂 Folder Structure

```
.
├── app.py                  # Main application file
├── helper.py               # Functions for DB connection & query generation
├── few_shots.py            # Few-shot learning examples
├── requirements.txt        # Dependencies
├── .env                    # Environment variables
├── README.md               # Project documentation
```

## 💡 Example Queries

| User Query                                                    | Generated SQL                                                                       |
| ------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| How many white Levi’s t-shirts are left?                      | `SELECT SUM(stock_quantity) FROM t_shirts WHERE brand = 'Levi' AND color = 'White'` |
| What is the total revenue if we sell all Nike t-shirts today? | `SELECT SUM(price * stock_quantity) FROM t_shirts WHERE brand = 'Nike'`             |

## 🚀 Future Enhancements

- Add support for additional databases (PostgreSQL, SQLite, etc.).
- Improve NLP understanding with fine-tuned LLMs.
- Develop a web UI for better accessibility.

## 📄 License

This project is licensed under the MIT License.
