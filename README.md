# Group_7_DL
Group 7 Milestone 3 Project Page




Project Title: Twitter-XLM-RoBERTa Multilingual Sentiment Analysis

Summary: This project explores multilingual sentiment analysis using XLM-RoBERTa. We fine-tuned the model on TweetEval and built an interactive Gradio demo to analyze tweet sentiment in real time.


Deliverables: 

Live Demo: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lola12313/Group_7_DL/blob/main/Gradio_Demo.ipynb)


Video
Paper


Model: 
Model: https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment
Paper: https://aclanthology.org/2022.lrec-1.27/


How to run: 

from transformers import pipeline
sentiment_pipeline = pipeline("sentiment-analysis", model="cardiffnlp/twitter-xlm-roberta-base-sentiment")
result = sentiment_pipeline("Estoy muy feliz con el servicio.")
print(result)



Team Roles: 	
	•Brandon Coutinho (DS): Evaluation Lead – metric computation, performance analysis
* Lauren Mercer: Model & Demo Lead – inference scripts, UI development
* Deepthi Sachidanand: Docs & Presentation Lead – architecture, innovations, slides
