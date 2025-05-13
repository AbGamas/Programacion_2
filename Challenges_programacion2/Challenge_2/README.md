
# Challenge 2 – Web Scraping and Sentiment Analysis with MLflow

This project performs **web scraping**, **text preprocessing**, and **sentiment analysis** on books descriptions extracted from a live website. The entire process is tracked and logged using **MLflow**.

GitHub Repository: [AbGamas/Programacion_2](https://github.com/AbGamas/Programacion_2)

---

##  Project Structure

```
Programacion_2/
├── data/                      # Optional folder for local data storage
├── figures/                   # Stores generated visualizations
├── notebooks/
│   └── Challenge_2.ipynb      # Main Jupyter Notebook
├── src/
│   └── mlops_pipeline.py      # Python script to run entire pipeline
├── requirements.txt           # Dependencies
└── README.md                  # Project documentation
```

---

##  Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/AbGamas/Programacion_2.git
cd Programacion_2
```

### 2. Install Required Dependencies

```bash
pip install -r requirements.txt
```

---

##  Running the Pipeline

To execute the sentiment analysis pipeline and track with MLflow:

```bash
python src/mlops_pipeline.py
```

Make sure the MLflow tracking server is running locally before executing:

```bash
mlflow ui
```

This will launch the MLflow UI at: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

##  Documentation

### Dataset Extraction

The dataset is obtained via **live web scraping** from the website:  
 [https://books.toscrape.com/](https://books.toscrape.com/)

Each book entry includes:
- Title
- Description

### Model Construction

The pipeline performs:
- **Tokenization** using NLTK
- **Stopword removal**
- **Sentiment scoring** with VADER from `vaderSentiment`

No supervised model is trained — this is a **rule-based sentiment analysis** project.

### MLOps Integration

We use **MLflow** to track:
- Parameters (source URL, number of books)
- Metrics (average, min, max sentiment)
- Artifacts:
  - CSV with results
  - Sentiment distribution plot
- Tags (project name, author)

---

## MLflow Results Example

- Experiment: `Books_Sentiment_Analysis`
- Run Name: `main_analysis`
- Artifacts:
  - `books_with_sentiment.csv`
  - `sentiment_distribution.png`

---

## Requirements

This project depends on the following libraries:

- `requests`
- `beautifulsoup4`
- `nltk`
- `vaderSentiment`
- `mlflow`
- `matplotlib`
- `seaborn`
- `pandas`

---

