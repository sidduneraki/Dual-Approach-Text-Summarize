# Dual-Approach-Text-Summarize
Implements both extractive (Scikit-learn) and abstractive (Hugging Face BART) methods for text summarization.

This repository contains a project exploring two fundamental techniques for text summarization: Extractive and Abstractive. It provides a practical comparison between a classic statistical method (TF-IDF) and a modern deep learning model (Transformers).

## Methods Implemented

### 1. Extractive Summarization (TF-IDF)
This method works by identifying the most important sentences from the original text and extracting them to form a summary. The implementation in `text_summarizer_using_Tfidf.ipynb` uses:

* **NLTK** for sentence tokenization.
* **Scikit-learn's `TfidfVectorizer`** to calculate the statistical importance of words across sentences.
* A scoring system to rank sentences based on their cumulative TF-IDF scores and select the top N sentences.

### 2. Abstractive Summarization (Transformers)
This method generates new sentences that capture the core meaning of the source text, rather than simply copying them. The implementation in `TextSummarizerUsingTransformers.ipynb` uses:

* The **Hugging Face `transformers` library**.
* The pre-trained **`facebook/bart-large-cnn` model**, which is fine-tuned for summarization tasks.
* The `model.generate()` function to create a new, coherent summary from the input text.

## Technologies Used
* Python
* Jupyter Notebook
* NLTK
* Scikit-learn
* Hugging Face Transformers
* PyTorch (as a backend for Transformers)

## Setup and Usage

To run these notebooks on your local machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3.  **Install the required libraries:**
    A `requirements.txt` file is included for easy setup.
    ```bash
    pip install -r requirements.txt
    ```

4.  **Download NLTK data:**
    The first time you run the TF-IDF notebook, you will need to download the necessary NLTK packages. The code to do this is included in the notebook.

5.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    Now you can open and run `text_summarizer_using_Tfidf.ipynb` and `TextSummarizerUsingTransformers.ipynb`.

