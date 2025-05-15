# SQL-Vector-Search Solution Accelerator

## Objective

This repository showcases two Streamlit applications that demonstrate how to build Retrieval-Augmented Generation (RAG) solutions using Azure SQL Database's native vector capabilities and Azure OpenAI. The apps are designed for:

- **Product Review Search**: Upload and semantically search product reviews using CSV data.
- **Resume Matching**: Upload and semantically match resumes using PDF documents.

Both apps allow users to generate embeddings, store/query them in Azure SQL DB, and perform LLM-powered Q&A for intelligent retrieval and recommendations.
These demo follow the Jupyter notebook provided in the [azure-sql-db-vector-search repo](https://github.com/Azure-Samples/azure-sql-db-vector-search/tree/main) under the Azure-Samples GitHub repo. 
---

## Products & Services Used

- Azure SQL Database (VECTOR data type)
- Azure OpenAI Service
- Azure Document Intelligence (for resume parsing)
- SQL on Fabric *(alternative to Azure SQL DB)*
- Streamlit
- Python (pandas, pyodbc, tiktoken, etc.)

---

## Deployment

### One Click Deployment
Automated deployment scripts are available in a separate [GitHub repository](https://github.com/Kushagra-2000/ARM_SQL_OpenAI):

This includes ARM templates to provision:
- Azure SQL DB
- Azure OpenAI
- Azure Document Intelligence (for resume app)

### Steps to Deploy SQL DB on Fabric
- Create a workspace in Fabric, if not existed before.
- New Item > SQL Database (preview) > Provide DB name > Create

---

## 📚 Resources

- [Azure SQL DB Vector Support](https://devblogs.microsoft.com/azure-sql/eap-for-vector-support-refresh-introducing-vector-type/)
- [Azure Document Intelligence](https://learn.microsoft.com/azure/ai-services/document-intelligence/)
- [Azure OpenAI Service](https://learn.microsoft.com/azure/ai-services/openai/)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [Project GitHub Repository](https://github.com/Azure-Samples/azure-sql-db-vector-search/tree/main/RAG-with-Documents)

---
