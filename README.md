📄✨ Resume Screening System (Production Ready)

A fully modular, production-ready, and scalable Resume Screening System built in Python.
It leverages NLP preprocessing, TF-IDF vectorization, and supervised machine learning to classify resumes into relevant categories.
Designed for real-world deployment with saved model artifacts, CLI usage, logging, and extensible architecture. 🚀


---

🧠 Key Features

✔️ Clean & Modular Architecture

TextCleaner transformer class

Pipeline-based ML workflow

Clear separation of data loading, preprocessing, training, and inference


✔️ Production-Ready Design

CLI for both training and prediction

Automatic saving of model artifacts (pipeline.joblib, label_encoder.joblib)

Robust error handling

Logging for traceable processes


✔️ NLP + Machine Learning

Text cleaning (URLs, stopwords, punctuation)

Tokenization

TF-IDF vectorization

Logistic Regression & Random Forest options 🌲

Label encoding for consistent category mapping


✔️ Easy to Deploy

Works as a standalone Python script

Can be wrapped in Flask/FastAPI or Docker 🐳

Suitable for enterprise HR or ATS pipelines



---

🗂️ Repository Structure

📁 Resume-Screening-System
│
├── resume_screening_prod.py      # Main production script
├── artifacts/                    # Saved model pipeline + label encoder (after training)
├── sample.csv                    # Example dataset (optional)
└── README.md                     # Documentation


---

⚙️ Installation

🔧 1. Clone the Repository

git clone https://github.com/yourusername/resume-screening-system.git
cd resume-screening-system

🔧 2. Install Dependencies

pip install -r requirements.txt

🔧 3. Ensure NLP Models are Installed

The script automatically downloads:

NLTK stopwords + punkt

SpaCy en_core_web_sm model



---

🏋️‍♂️ Training the Model

Run the script in training mode:

python resume_screening_prod.py \
    --mode train \
    --data-path sample.csv \
    --text-column Update_Resume \
    --target-column Category \
    --output-dir artifacts \
    --classifier logreg

📌 Output

artifacts/pipeline.joblib

artifacts/label_encoder.joblib

Training accuracy + classification report



---

🔍 Making Predictions

Use the script in predict mode:

python resume_screening_prod.py \
    --mode predict \
    --input-text "Experienced Python developer with ML background..." \
    --output-dir artifacts

📌 Output

Predicted category label

Class probability distribution (if available)



---

🧰 Supported Classifiers

Classifier	Purpose	Emoji

Logistic Regression	Fast, baseline, high accuracy	⚡
Random Forest	Robust ensemble, interpretable	🌳



---

🔮 Future Enhancements

Here are potential extensions you may add:

✨ FastAPI-based microservice endpoint

📦 Docker container for deployment

🔍 Resume similarity scoring (cosine similarity)

🧬 BERT/Transformer-based embedding models
