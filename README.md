# 🩺 Medical-Chatbot: LLMs-LangChain-Pinecone-Flask-AWS

An end-to-end AI-powered medical chatbot that delivers context-aware responses to medical queries using **Retrieval-Augmented Generation (RAG)**. The application retrieves relevant information from a medical knowledge base before generating responses with **Llama-3.3-70B-Versatile** (served via the Groq API), resulting in fast, reliable and accurate answers.

Built with **Python**, **Flask**, **LangChain**, **Pinecone Vector Database**, **Hugging Face Embeddings**, and **Docker**, the application is deployed on **AWS EC2** with an automated **CI/CD pipeline** powered by **GitHub Actions** and **Amazon ECR**.

🚀 **Live Demo:** Try the deployed application here: **http://100.54.24.62:8080/**

## 🎥 Project Demo

<p align="center">
  <a href="https://github.com/user-attachments/assets/57287ce5-584a-4a11-876e-b936df1dff09">
    <img src="assets/demo.png" width="900" alt="Medical Chatbot Demo">
  </a>
</p>

<p align="center">
<b>Click the thumbnail to watch the demo video.</b>
</p>

## ✨ Key Features

- 🧠 Retrieval-Augmented Generation (RAG) for context-aware medical responses
- 📚 Medical knowledge retrieval using *The Gale Encyclopedia of Medicine*
- 🔍 Semantic search with Hugging Face embeddings and Pinecone
- 🤖 AI-powered responses using **Llama-3.3-70B-Versatile** via the Groq API
- 🌐 Interactive chat interface built with Flask, HTML, and CSS
- 🐳 Dockerized application for consistent deployment
- ☁️ Automated CI/CD pipeline using GitHub Actions, Amazon ECR, and AWS EC2

### Techstack Used:

## 🛠️ Tech Stack

- Python
- Flask
- LangChain
- Llama-3.3-70B-Versatile (Groq API)
- Hugging Face Embeddings
- Pinecone Vector Database
- Docker
- GitHub Actions
- Amazon ECR
- AWS EC2

## 🚀 Getting Started
### STEPS:

Clone the repository

```bash
git clone https://github.com/Srinikesh-Mucha/Medical-Chatbot---LLMs-LangChain-Pinecone-Flask-AWS.git
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n medibot python=3.10 -y
```

```bash
conda activate medibot
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


### Create a `.env` file in the root directory and add your Pinecone & groq credentials as follows:

```ini
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
GROQ_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```


```bash
# run the following command to store embeddings to pinecone
python store_index.py
```

```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up localhost:
```


# AWS-CICD-Deployment-with-Github-Actions

## ☁️ Deployment

This project uses an automated CI/CD pipeline:

1. Push code to GitHub
2. GitHub Actions builds the Docker image
3. Docker image is pushed to Amazon ECR
4. AWS EC2 pulls the latest image
5. Docker container is restarted automatically

### Required GitHub Secrets

- AWS_ACCESS_KEY_ID
- AWS_SECRET_ACCESS_KEY
- AWS_DEFAULT_REGION
- ECR_REPO
- PINECONE_API_KEY
- GROQ_API_KEY
