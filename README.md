# Group_7_DL
### Group 7 Milestone 3 Project Page




#### Project Title: Twitter-XLM-RoBERTa Multilingual Sentiment Analysis (Model Review and Demo Track)

#### Project Scope: 
This project presents a detailed analysis of XLM-T, a domain-adapted multilingual language model specifically designed for sentiment analysis on Twitter. By examining its architecture, technical innovations, and performance metrics, we demonstrate how XLM-T bridges the gap between general multilingual models and the noisy, emoji-rich environment of social media. Through continued masked language model pretraining on 198 million multilingual tweets, XLM-T adapts to the unique linguistic challenges of Twitter while maintaining cross-lingual transfer capabilities. We discuss key innovations including emoji-aware tokenization and adapter-based fine-tuning, providing implementation examples and comparative performance analysis across multiple languages. We fine-tuned the model on TweetEval and built an interactive Gradio demo to analyze tweet sentiment in real time.


#### Locations:
The cleaned_Demo.ipynb file contains the Google Colab notebook with two of the demos.
The Gradio_Demo_CLEAN file contains the static version of the Google Colab notebook with the Gradio demo
The notebooks folder contains Google Colab notebooks with model use cases and fine tuning 
The Twitter XLM roberta sentiment Analysis folder contains our plan for the project and the project overview



#### Deliverables: 

Live Demo: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lola12313/Group_7_DL/blob/main/Gradio_Demo.ipynb)


Video: https://drive.google.com/file/d/1Y_fTwNq9AnIjr3nquzZLksrMVM4onaGF/view

Paper: https://drive.google.com/file/d/1N6MG0FngTh7OtMtCveEAhOMqOLygafbM/view?usp=share_link


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
* Brandon Coutinho: Evaluation Lead – metric computation, performance analysis
* Lauren Mercer: Model & Demo Lead – inference scripts, UI development
* Deepthi Sachidanand: Documentation & Presentation Lead – base model architecture analysis, innovations, slides
