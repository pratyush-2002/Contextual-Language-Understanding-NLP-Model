# Sentiment, Emotion, and Cultural Context Analysis API

This is a Flask-based NLP application that analyzes text for sentiment, emotion, and cultural references using pre-trained transformer models.

## Features
- **Sentiment Analysis**: Uses `cardiffnlp/twitter-xlm-roberta-base-sentiment` to classify text sentiment.
- **Emotion Detection**: Uses `j-hartmann/emotion-english-distilroberta-base` to determine the emotional tone of the text.
- **Cultural Context Detection**: Identifies cultural references in text and fetches relevant information from Wikipedia.

## Installation

### Prerequisites
- Python 3.7+
- `pip` installed

### Clone the Repository
```bash
git clone https://github.com/your-repo/nlp-analysis-app.git
cd nlp-analysis-app
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

## Usage

### Run the Flask App
```bash
python app.py
```
The app will be available at `http://127.0.0.1:5000/`.

### API Endpoints
#### 1. Home Page
- **Endpoint**: `/`
- **Method**: `GET`
- **Description**: Renders the home page.

#### 2. Analyze Text
- **Endpoint**: `/analyze`
- **Method**: `POST`
- **Description**: Accepts text input and returns sentiment, emotion, and cultural context.
- **Request Body (JSON)**:
  ```json
  {
    "text": "I love Bollywood movies!"
  }
  ```
- **Response (JSON)**:
  ```json
  {
    "sentiment": [{"label": "positive", "score": 0.98}],
    "emotion": [{"label": "joy", "score": 0.95}],
    "cultural_context": [{"term": "Bollywood", "meaning": "Bollywood is the Hindi-language film industry based in Mumbai, India."}],
    "dynamic_response": "I'm so glad to hear that you're feeling joy! Keep it up!"
  }
  ```

## Technologies Used
- **Flask**: Web framework for Python
- **Transformers**: Hugging Face library for NLP models
- **XLM-RoBERTa**: Pre-trained model for sentiment analysis
- **DistilRoBERTa**: Pre-trained model for emotion classification
- **Wikipedia API**: Fetches cultural context


