# Turn Your Data into an AI Chatbot-1

## 🚀 Project Overview
This project demonstrates how to build an AI chatbot that specializes in answering questions about you, your work, and your knowledge. By leveraging **Retrieval Augmented Generation (RAG)**, we train an AI model on your personal documents using **Amazon Bedrock**, integrating various AWS services to create a powerful, knowledge-driven chatbot.
![image](https://github.com/user-attachments/assets/b2c1c387-e5e3-4c58-b6d3-12d892ae6c46)


## 🏗️ Services Used
- **Amazon Bedrock** – AI model management and inference
- **Amazon OpenSearch Serverless** – Vector database for efficient retrieval
- **Amazon S3** – Storage for personal documents

## 🧠 What is RAG (Retrieval Augmented Generation)?
AI models like ChatGPT are powerful but limited to their training data and online searches. RAG enhances this by allowing AI models to retrieve information from a specialized **Knowledge Base**, enabling:
- Chatbots that can answer **specific** questions based on personal/company documents
- Customer support chatbots with tailored knowledge
- Research assistants for technical and academic fields

## 📌 Key Features
✅ Build a Knowledge Base in **Amazon Bedrock**  
✅ Store and retrieve documents using **Amazon S3** & **OpenSearch**  
✅ Select and integrate AI models to **generate human-like responses**  
✅ **Test, refine, and enhance chatbot performance**  

---

## 📚 Step-by-Step Implementation

### 🔹 Step 1: Setting Up a Knowledge Base
- Navigate to **Amazon Bedrock → Knowledge Bases**
- Create a **Knowledge Base with Vector Store**
- Store personal documents in **Amazon S3** for retrieval
- Use **IAM roles** to grant Bedrock access to S3

### 🔹 Step 2: Storing Documents in Amazon S3
- Create an **S3 bucket** in the same AWS region (e.g., `us-east-2`)
- Upload **personal or company documents** for chatbot training

### 🔹 Step 3: Connecting Knowledge Base to Data Source
- Link the **S3 bucket** to the **Knowledge Base** in Bedrock
- Configure **parsing strategy** (text extraction) & **chunking** for efficient search
- Select **Titan Text Embeddings v2** for vector representation

### 🔹 Step 4: Enabling AI Models in Amazon Bedrock
- Navigate to **Bedrock Model Access**
- Enable **Titan Text Embeddings v2, Llama 3.1 8B Instruct, Llama 3.3 70B Instruct**
- Accept terms & submit for approval

### 🔹 Step 5: Synchronizing Knowledge Base
- Sync S3 data with the **Knowledge Base**
- Configure **OpenSearch Serverless** for **vector retrieval**

### 🔹 Step 6: Testing and Refining the Chatbot
- Select **Llama 3.1 8B Instruct** model for inference
- Ask sample queries to test response quality
- Switch to **Llama 3.3 70B Instruct** for improved performance if needed

---

## 🎯 Optimizing Chatbot Responses
- Increase **number of source chunks** for broader context
- Customize **prompts** for refined chatbot behavior
- Compare **response quality** using different models

### 💡 Example Query:
❓ *"What AWS services were used to build this chatbot?"*  
✅ The chatbot retrieves data from the **Knowledge Base** and provides a well-structured answer.

---

## 🧹 Cleaning Up Resources (Post-Project)
- **Delete** Knowledge Base in Amazon Bedrock
- **Remove** documents from S3
- **Delete** vector store in OpenSearch
