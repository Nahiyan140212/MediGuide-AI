# MediGuide AI 🏥💡

MediGuide AI is an **AI-powered medical chatbot** that leverages **Large Language Models (LLMs)** and the **Gale Encyclopedia of Medicine** to provide **reliable health information**. The chatbot helps users get **medical insights, symptom explanations, and general healthcare guidance** through an intuitive interface. **Gale Encyclopedia of Medicine** is a book with around 4500+ pages. Here is the link: 

---

## Features ✨
✅ **AI-Powered Medical Assistance** – Provides reliable answers based on the Gale Encyclopedia of Medicine.  
✅ **Retrieval-Augmented Generation (RAG)** – Ensures accurate responses by retrieving relevant medical data.  
✅ **Pinecone Vector Search** – Enables efficient information retrieval from medical documents.  
✅ **Seamless LLM Integration** – Uses OpenAI’s model for natural language understanding.  
✅ **User-Friendly Interface** – Simple chat-based interaction for laypeople to access medical insights.  
✅ **Fast & Scalable** – Built with efficient architecture to handle multiple queries.  

---

## Tech Stack 🛠
🔹 **Frontend:** HTML, CSS (for user-friendly chatbot UI)  
🔹 **Backend:** Python (Flask/FastAPI for API integration)  
🔹 **Database:** Pinecone (for vector storage)  
🔹 **LLM:** OpenAI GPT-based model  
🔹 **Deployment:** GitHub, Docker, Cloud Services (AWS/GCP/Azure)  

---

# End-to-End Medical Chatbot - Generative AI

## How to Run? 🏥

### 1️⃣ Clone the Repository:
```bash
Project repo: https://github.com/
```

### 2️⃣ Create a Conda Environment:
```bash
conda create -n medibot python=3.10 -y
conda activate medibot
```

### 3️⃣ Install Dependencies:
```bash
pip install -r requirements.txt
```

### 4️⃣ 🔑 Set Up API Keys
Create a `.env` file in the root directory and add your Pinecone & OpenAI credentials as follows:
```ini
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
OPENAI_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```

### 5️⃣ Store Embeddings in Pinecone:
```bash
python store_index.py
```

### 6️⃣ Run the Application:
```bash
python app.py
```

### 7️⃣ Open Your Browser:
```bash
open up localhost:
```

---

## Customization 📝
If you want to modify this chatbot based on your preferred book or document, just **upload that PDF file into the `Data` folder** and then run:
```bash
python store_index.py
```
This will store the embeddings for the new document, allowing the chatbot to reference it when answering queries.

---

## Use Cases 🚑
🔹 **Medical education & self-learning**  
🔹 **Quick healthcare Q&A**  
🔹 **Symptom insights & medical term explanations**  
🔹 **Assisting non-experts with medical guidance**  

---

## Tech Stack Used:
- Python
- LangChain
- Flask
- GPT
- Pinecone

---

## Disclaimer ⚠
**MediGuide AI does not provide medical diagnoses or professional healthcare advice.** It is an **educational tool** that delivers medical information based on available sources. **Always consult a healthcare provider for medical concerns.**



## Future Plan
# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 970547337635.dkr.ecr.ap-south-1.amazonaws.com/medicalchatbot

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

   - AWS_ACCESS_KEY_ID
   - AWS_SECRET_ACCESS_KEY
   - AWS_DEFAULT_REGION
   - ECR_REPO
   - PINECONE_API_KEY
   - OPENAI_API_KEY
