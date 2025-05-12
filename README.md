# Group_7_DL
### Group 7 Milestone 3 Project Page




#### Project Title: Twitter-XLM-RoBERTa Multilingual Sentiment Analysis (Model Review and Demo Track)

#### Project Scope: 
This project presents a detailed analysis of XLM-T, a domain-adapted multilingual language model specifically designed for sentiment analysis on Twitter. By examining its architecture, technical innovations, and performance metrics, we demonstrate how XLM-T bridges the gap between general multilingual models and the noisy, emoji-rich environment of social media. Through continued masked language model pretraining on 198 million multilingual tweets, XLM-T adapts to the unique linguistic challenges of Twitter while maintaining cross-lingual transfer capabilities. We discuss key innovations including emoji-aware tokenization and adapter-based fine-tuning, providing implementation examples and comparative performance analysis across multiple languages. We fine-tuned the model on TweetEval and built an interactive Gradio demo to analyze tweet sentiment in real time.


#### Deliverables: 

Live Demo: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lola12313/Group_7_DL/blob/main/Gradio_Demo.ipynb)


Video: 

Paper: 


#### Model: 
Model: https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment

Reference Paper: https://aclanthology.org/2022.lrec-1.27/

#### Run Sentiment Analysis
```python
from transformers import pipeline
sentiment_pipeline = pipeline("sentiment-analysis", model="cardiffnlp/twitter-xlm-roberta-base-sentiment")
result = sentiment_pipeline("Estoy muy feliz con el servicio.")
print(result)
```

#### Team Roles: 	
* Brandon Coutinho (DS): Evaluation Lead – metric computation, performance analysis
* Lauren Mercer: Model & Demo Lead – inference scripts, UI development
* Deepthi Sachidanand: Documentation & Presentation Lead – base model architecture analysis, innovations, slides
