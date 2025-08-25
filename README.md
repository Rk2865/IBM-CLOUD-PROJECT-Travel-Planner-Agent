# IBM-CLOUD-PROJECT-Travel-Planner-Agent

Got it ✅  
You’ve implemented an **AI Service Deployment Notebook** for Watsonx.ai that defines, promotes, stores, deploys, and tests an **AI-powered Travel Planner Agent**. I’ll create a `README.md` file that explains the structure, workflow, and conclusion of this project in a professional and clear way.  

***

# 📘 README.md  

# Travel Planner Agent - AI Service Deployment  

This project demonstrates how to **build, deploy, and test an AI-powered Travel Planner Agent** using **IBM Watsonx.ai** and LangChain. The agent is capable of providing intelligent travel recommendations and planning assistance by integrating external tools such as Google Search, DuckDuckGo, Wikipedia, and WebCrawler.  

The notebook walks through all steps necessary to design, promote, store, and deploy the agent as an **AI Service** in IBM Cloud.  

***

## 🚀 Features  
- Deploy a **custom AI service** to IBM Watsonx.ai.  
- Integrates with **LangChain IBM** and **Watsonx.ai LLM** (Meta-Llama-3-3-70B-Instruct).  
- Supports **tool-based augmentation** (GoogleSearch, DuckDuckGo, Wikipedia, WebCrawler).  
- Implements both **standard response** and **streaming response APIs**.  
- End-to-end flow from **local testing → repository storage → cloud deployment**.  

***

## 📂 Project Structure  

1. **Setup Environment**  
   - Define credentials for Watsonx.ai.  
   - Connect to IBM Cloud project and deployment space.  

2. **Create AI Service Function**  
   - Define the Travel Planner agent logic.  
   - Configure chat model parameters (`temperature`, `max_tokens`, etc.).  
   - Define utility tools (GoogleSearch, DuckDuckGo, Wikipedia, WebCrawler).  
   - Support both **synchronous** (`generate`) and **streaming** (`generate_stream`) responses.  

3. **Local Testing**  
   - Run the AI service function locally with sample messages.  

4. **Store & Deploy Service**  
   - Store the agent in the Watsonx.ai repository.  
   - Define request and response schemas.  
   - Deploy service with metadata (`name`, `description`, `tags`).  

5. **Test AI Service**  
   - Run the deployed service via the deployment ID.  
   - Validate cloud execution with test prompts.  

***

## ⚙️ Requirements  
- Python **3.11**  
- `ibm-watsonx-ai` SDK  
- `langchain-ibm`, `langchain-core`  
- IBM Cloud account with:  
  - Watsonx.ai enabled.  
  - API key and project/space access.  

***

## ▶️ Steps to Run  

1. Clone/download the notebook.  
2. Install dependencies:  
   ```bash
   pip install ibm-watsonx-ai langchain-ibm langchain-core requests
   ```
3. Provide your **IBM Cloud API key** when prompted.  
4. Update your **project ID** and **space ID** in the notebook.  
5. Execute cells in sequence:  
   - Setup  
   - Define service  
   - Local test  
   - Store & Deploy  
   - Test deployed service  

***

## 📡 API Example  

Once deployed, you can call the Travel Planner Agent as a REST API.  

**Sample Payload**:  
```json
{
  "messages": [
    {
      "role": "user",
      "content": "Plan a 5-day trip to Paris with top attractions."
    }
  ]
}
```

**Sample Response**:  
```json
{
  "choices": [
    {
      "index": 0,
      "message": {
        "role": "assistant",
        "content": "Here’s a detailed 5-day travel itinerary for Paris..."
      }
    }
  ]
}
```

***

## 📌 Conclusion  

This project successfully demonstrates how to:  
✅ Create a **custom AI service** using IBM Watsonx.ai & LangChain.  
✅ Enhance agent intelligence with **external tools** (search, crawling, knowledge sources).  
✅ Seamlessly **deploy AI agents** as scalable services in IBM Cloud.  
✅ Test both **local** and **cloud-deployed functions** with real-time responses.  

The **Travel Planner Agent** is a blueprint for building more industry-specific agents (finance advisor, healthcare assistant, shopping bot, etc.). By extending tools and customizing schemas, you can deploy production-level AI services quickly.  

***

## 📝 License  
Licensed Materials - Copyright © 2024 IBM.  
Released under the **ILAN License** (see Watsonx.ai License Terms).  

***

👉 Would you like me to also create a **"Quick Start deployment script"** (`deploy.py`) alongside `README.md` so you don’t always have to run the notebook manually?
