# 🔍 Twitter-XLM-RoBERTa Multilingual Sentiment Analysis

## 🧠 Project Goal
Evaluate the multilingual performance of the `cardiffnlp/twitter-xlm-roberta-base-sentiment` model on a benchmark dataset of ~900 tweets with minimal preprocessing. Document model behavior, architecture, technical innovations, and provide a real-time web-based demo.

## 📦 Model Used
- **Model**: [Twitter-XLM-RoBERTa-base-Sentiment](https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment)
- **Paper**: [XLM-T: Multilingual Language Models for Twitter](https://aclanthology.org/2022.lrec-1.27)

## 🗂️ Folder Structure
```
📦 twitter-xlm-sentiment-analysis
├── data                  # Input test dataset (~900 tweets)
├── model                 # Inference notebooks/scripts
├── evaluation            # Metric results, plots, F1-scores
├── ui                    # Flask or Gradio-based sentiment demo
├── docs                  # Project report and references
├── presentation          # Final slides
├── updates               # Weekly progress notes
```

## ⚙️ Installation
```bash
pip install transformers pandas scipy scikit-learn matplotlib flask gradio
```

## 🚀 Quick Start: Run Sentiment Analysis
```python
from transformers import pipeline
sentiment_pipeline = pipeline("sentiment-analysis", model="cardiffnlp/twitter-xlm-roberta-base-sentiment")
result = sentiment_pipeline("Estoy muy feliz con el servicio.")
print(result)
```

### ✅ Output
```json
[{'label': 'Positive', 'score': 0.88}]
```

## 🖥️ Run the Web Demo
### Flask App
```bash
cd ui
python app.py
```
Visit `http://localhost:5000` in browser.

### Gradio App (Alternative)
```python
import gradio as gr
from transformers import pipeline

classifier = pipeline("sentiment-analysis", model="cardiffnlp/twitter-xlm-roberta-base-sentiment")

def analyze_sentiment(text):
    result = classifier(text)[0]
    return f"{result['label']} ({result['score']:.2f})"

gr.Interface(fn=analyze_sentiment, inputs="text", outputs="text", title="Tweet Sentiment Analyzer").launch()
```

## 📝 Team Roles
- **Member 1 (DS)**: Evaluation Lead – metric computation, performance analysis
- **Member 2**: Model & Demo Lead – inference scripts, UI development
- **Member 3**: Docs & Presentation Lead – architecture, innovations, slides

## 📅 Timeline & Progress
- Weekly commits and task summaries will be updated in `updates/week_x_summary.md`
- Major contributions will be pushed via PRs from dedicated branches (`eval/`, `model/`, `docs/`, `ui/`)

## 📈 Deliverables
- `project_report.md`
- Evaluation results with comparison to paper benchmarks
- Slide deck and code walkthrough
- Flask or Gradio web demo

## 📚 Dataset & Evaluation
- UMSAB/TweetEval subset (multilingual tweets with labels)
- Evaluation metrics: accuracy, precision, recall, macro-F1
- Visualization of prediction vs. truth

---
For detailed weekly plan, roles, and assignments, see `plan.md