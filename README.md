# Student Performance Analyzer App

An interactive Streamlit app that predicts student exam scores and provides AI-powered insights using Groq or GitHub Models API keys.

**Live demo:** https://edumetrixapp.streamlit.app/

## Features

- **Overview**: Project summary and feature descriptions
- **Dataset Statistics**: Visualizations of the Student Performance dataset
- **Analysis & Insights**: Key findings and conclusions from the data
- **Prediction**: Input student data to predict exam scores
- **AI Chatbot**: Ask questions about student performance (powered by Groq or GitHub Models)

## Prerequisites

1. **Python 3.8+** installed
2. A **Groq API key** and/or **GitHub Models API key**

### AI API Keys

Set keys in Streamlit secrets or environment variables:

```toml
# .streamlit/secrets.toml
GROQ_API_KEY = "your-groq-api-key"
GITHUB_API_KEY = "your-github-token-or-api-key"

# Optional
LLM_PROVIDER = "Groq"
GROQ_MODEL = "llama-3.3-70b-versatile"
GITHUB_MODEL = "openai/gpt-4.1-mini"
```

Environment variable names are the same. The app only supports `Groq` and `GitHub` as AI providers.

## Installation

1. Clone or download this repository

2. Install the required Python packages:

```bash
pip install -r requirements.txt
```

## Running the App

1. Make sure your Groq or GitHub API key is configured.

2. Run the Streamlit app:

```bash
streamlit run app.py
```

3. Open your browser and navigate to:

```text
http://localhost:8501
```

## Project Structure

```text
.
|-- app.py
|-- model_1_tubesAIlab.pkl
|-- dataset/
|   `-- StudentPerformanceFactors.csv
|-- requirements.txt
|-- Tubes_AI_LAB_LAHH.ipynb
`-- README.md
```

## Using the App

### 1. Overview

Read about the project and understand the features being analyzed.

### 2. Dataset Statistics

Explore the dataset with interactive visualizations:

- Numerical feature distributions
- Categorical feature distributions
- Correlation analysis

### 3. Analysis & Insights

View detailed analysis and conclusions:

- Key findings from correlation analysis
- Performance by gender
- Study hours vs exam score relationships

### 4. Prediction

Enter student information to predict exam scores:

- Fill in all the student details in the form
- Click "Predict Exam Score" to get the prediction
- Receive AI-powered feedback on the prediction

### 5. AI Chatbot

Ask questions about student performance:

- The chatbot is limited to student performance topics only
- It can provide insights based on the prediction context
- Ask about study tips, factors affecting scores, etc.

## Model Information

- **Primary Model**: Linear Regression
- **Target**: Exam Score (0-100)
- **Features**: 19 features including study hours, attendance, parental involvement, etc.

## Troubleshooting

### AI API Key Error

If the chatbot reports a missing API key:

1. Add `GROQ_API_KEY` or `GITHUB_API_KEY` to `.streamlit/secrets.toml`
2. Or set the same key as an environment variable
3. Select the matching provider in the Streamlit sidebar

### Model Not Found

Ensure `model_1_tubesAIlab.pkl` is in the same directory as `app.py`.

### Dataset Not Found

Ensure the `dataset/StudentPerformanceFactors.csv` file exists.

## Notes

- The AI chatbot uses Groq by default. You can switch to GitHub Models in the sidebar.
- You can override models with `GROQ_MODEL` and `GITHUB_MODEL`.
- The chatbot is specifically configured to only answer questions related to student performance.
- The prediction model was trained on the Student Performance Factors dataset.
