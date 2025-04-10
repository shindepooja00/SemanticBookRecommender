
# Semantic Book Recommender with LLMs

This repository contains the full code for building a **Semantic Book Recommender** using Large Language Models (LLMs). The project utilizes several techniques, including semantic search, text classification, sentiment analysis, and a Gradio-based web interface for recommendations. The project is broken down into five key components:

---

## Project Overview

### 1. **Text Data Cleaning**  
*Located in the notebook:* `data-exploration.ipynb`  
This step involves cleaning the raw text data to prepare it for further analysis. We remove unnecessary characters, format the text, and handle any missing or irrelevant data to ensure high-quality input for the recommender model.

### 2. **Semantic (Vector) Search and Vector Database Creation**  
*Located in the notebook:* `vector-search.ipynb`  
This section demonstrates how to build a **vector database** using semantic search. We convert book descriptions into vector embeddings that represent their semantic meaning. By doing this, the system can find the most similar books to a natural language query (e.g., "a book about a person seeking revenge"). This allows users to retrieve more contextually relevant recommendations.

### 3. **Text Classification Using Zero-Shot Classification with LLMs**  
*Located in the notebook:* `text-classification.ipynb`  
This notebook walks through using **zero-shot classification** to categorize books into different genres, such as "fiction" or "non-fiction". This classification creates an additional layer of filtering, enabling users to search for books based on genre alongside other criteria.

### 4. **Sentiment Analysis Using LLMs**  
*Located in the notebook:* `sentiment-analysis.ipynb`  
Here, we implement sentiment analysis to classify the emotional tone of books. We use LLMs to analyze text and extract emotions such as joy, sadness, or suspense. This feature allows users to sort books by their tone, helping them find books that match their mood.

### 5. **Web Application Using Gradio**  
*Located in the file:* `gradio-dashboard.py`  
The final component of the project is the creation of a simple web interface using **Gradio**. This allows users to interact with the recommender system and get book suggestions based on their inputs. The application is easy to use and provides an intuitive way to engage with the system.

---

## Project Setup

To run this project locally, you will need Python 3.11 or higher. The following dependencies are required:

- `kagglehub`
- `pandas`
- `matplotlib`
- `seaborn`
- `python-dotenv`
- `langchain-community`
- `langchain-opencv`
- `langchain-chroma`
- `transformers`
- `gradio`
- `notebook`
- `ipywidgets`

A `requirements.txt` file is provided in the repository to help you install all the necessary dependencies.

---

## Environment Setup

1. **Create a `.env` file**  
   In the root directory of the project, create a `.env` file containing your **OpenAI API key**. This is essential for interacting with the language model. Instructions on how to get your API key can be found in the repository.

2. **Download the Data**  
   The dataset used in this project is available on Kaggle. To use the data, follow the instructions provided in the repo to download and load the dataset into your environment.

---

## How to Use the Project

1. **Install Dependencies**  
   Run the following command to install all required libraries:
   ```bash
   pip install -r requirements.txt
   ```

2. **Set Up the `.env` File**  
   Make sure to set up the `.env` file with your OpenAI API key as mentioned in the setup instructions.

3. **Run the Jupyter Notebooks**  
   Start by exploring the individual Jupyter notebooks:
   - `data-exploration.ipynb` for text cleaning
   - `vector-search.ipynb` for building the vector database
   - `text-classification.ipynb` for the genre classification model
   - `sentiment-analysis.ipynb` for sentiment analysis  
   These notebooks contain detailed explanations and code to walk you through the entire process.

4. **Launch the Gradio Web Interface**  
   After everything is set up and the models are trained, you can run the Gradio dashboard to interact with the system:
   ```bash
   python gradio-dashboard.py
   ```

   This will launch a web interface where you can enter book descriptions and receive semantic recommendations in return.

---

## Contributing

If you would like to contribute to this project, feel free to fork the repo and submit a pull request. Any improvements, bug fixes, or feature suggestions are welcome!
