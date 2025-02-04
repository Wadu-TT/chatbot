🎓 Course Recommender System

This repository contains a Course Recommender System built using Python, machine learning embeddings, FAISS for similarity search, and LLM (Large Language Model) for generating personalized explanations for course recommendations. The project provides a user-friendly interface using Gradio for querying courses based on user input and displaying results interactively.
🚀 Features

    Course Recommendation: Retrieve the most relevant courses for a given query based on course descriptions and skills.
    Similarity Search with FAISS: Efficiently search through high-dimensional embeddings for fast and accurate recommendations.
    LLM-based Explanation Generation: Use a Llama model (Mistral-7B-Instruct) to generate explanations for why a particular course matches the query.
    Gradio Interface: Simple and intuitive web-based interface for user interaction.

📂 Project Structure
Key Cells in the Jupyter Notebook:

    Dependencies Installation (cell 1):
    Installs necessary libraries like transformers, sentence-transformers, pandas, faiss, torch, and gradio.

    Model and Libraries Setup (cell 2 & 3):
        Loads required Python packages.
        Downloads the Mistral-7B-Instruct LLM model using hf_hub_download.

    Data Preprocessing (cell 4):
        Loads and preprocesses Coursera.csv by selecting relevant columns (Title, Skills, Ratings, etc.).
        Combines Skills and Organization into a Course Description column.
        Adds placeholders for Course URL and Difficulty Level.

    Embedding Creation and FAISS Index (cell 5):
        Creates sentence embeddings for course descriptions using SentenceTransformer (all-MiniLM-L6-v2).
        Builds a FAISS index for fast similarity search.

    LLM Initialization and Test (cell 5):
        Initializes the Llama model (mistral-7b-instruct).
        Runs a test prompt to ensure the model is ready for explanation generation.

    Course Recommendation Function (cell 6):
        Searches for the most similar courses in the FAISS index.
        Returns the top results with similarity scores.

    Explanation Generation (cell 7):
        Uses the Llama model to generate a natural-language explanation for the recommended courses based on the query.

    Gradio Interface (cell 8):
        Creates an interactive web interface using Gradio.
        Users can input queries like “data science” or “machine learning” to receive course recommendations and explanations.

🛠 Installation and Setup

    Clone the repository:

git clone https://github.com/Wadu-TT/chatbot.git
cd chatbot
run all the cells

📊 Dataset

The dataset (Coursera.csv) includes course details such as:

    Title
    Skills
    Ratings
    Review counts
    Organization

These columns are processed to create a searchable index for course recommendations.

⚙️ Technology Stack

    Python
    Transformers (for LLM integration)
    Sentence Transformers (for text embeddings)
    FAISS (for similarity search)
    Gradio (for web-based user interface)

🖥 Example Usage

    Enter a query like "Python programming" or "data science" in the Gradio interface.
    The system recommends relevant courses based on the query.
    An explanation is generated to help users understand why the suggested courses match the query.

🤝 Contributing

Contributions are welcome! Feel free to fork this repository and submit a pull request.
