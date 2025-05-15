# RAG Resume Matcher Streamlit App with Azure SQL DB, Document Intelligence, and OpenAI

## Objective
This Streamlit app demonstrates how to build a Retrieval-Augmented Generation (RAG) solution for resume matching using Azure SQL Database's native vector capabilities, Azure Document Intelligence, and Azure OpenAI. The app enables users to upload PDF resumes, extract and chunk their content, generate embeddings, store/query them in Azure SQL DB, and perform LLM-powered Q&A for candidate search and recommendations.

## Key Features
- **PDF Resume Upload & Processing:** Upload multiple PDF resumes and extract text using Azure Document Intelligence.
- **Text Chunking:** Automatically split extracted text into manageable chunks (500 tokens each) for embedding.
- **Embedding Generation:** Generate semantic embeddings for each chunk using Azure OpenAI's embedding models.
- **Vector Storage in Azure SQL DB:** Store embeddings in Azure SQL DB using the new VECTOR data type for efficient similarity search.
- **Vector Search:** Query the database for the most relevant resume chunks based on a user query using built-in vector distance functions.
- **LLM Q&A:** Augment search results with GPT-4.1-based recommendations and summaries, grounded in the retrieved data.
- **Modern UI:** Interactive, step-by-step workflow with persistent results and clear progress indicators.

## Target End Users
- Recruiters and HR professionals seeking AI-powered candidate search.
- Data scientists and engineers building RAG or vector search solutions on Azure.
- Solution architects and technical decision makers evaluating Azure's vector and AI capabilities.

## Prerequisites
- **Azure Subscription**
- **Azure SQL Database** (with vector support enabled)
- **Azure Document Intelligence Resource**
- **Azure OpenAI Resource** (with embedding and GPT-4.1 models deployed)
- **Python 3.8+**
- **Required Python packages** (see `requirements.txt`)
- **ODBC Driver 18+ for SQL Server** (for pyodbc)

## Products & Services Used
- Azure SQL Database (VECTOR data type)
- Azure Document Intelligence (Form Recognizer)
- Azure OpenAI Service
- Streamlit
- Python (pandas, tiktoken, pyodbc, etc.)

## Automated Deployments
- **ARM Template Scripts:**
    - ARM templates are provided separately to automate the deployment of Azure SQL DB, Document Intelligence, and OpenAI resources. Please refer to the `Assets/` or deployment folder for scripts and instructions.

## Steps to Execute
1. **Clone the Repository**
2. **Install Requirements:**
   ```
   pip install -r requirements.txt
   ```
3. **Deploy Azure Resources:**
   - Use the provided ARM templates or Azure Portal to deploy SQL DB, Document Intelligence, and OpenAI resources.
4. **Configure Credentials:**
   - Launch the app and enter your Azure endpoints, API keys, and SQL connection string in the sidebar.
5. **Create Table:**
   - Use the UI to create the `resumedocs` table in your Azure SQL DB if it does not exist.
6. **Upload Resumes:**
   - Upload one or more PDF resumes.
7. **Process & Chunk:**
   - The app will extract and chunk text from each PDF.
8. **Generate Embeddings:**
   - Click to generate embeddings for all chunks.
9. **Insert into SQL DB:**
   - Store the embeddings in the Azure SQL DB vector table.
10. **Query & Q&A:**
    - Enter a role or skill to find candidates and get LLM-powered recommendations.

## Troubleshooting
- **Connection Errors:**
  - Ensure your SQL connection string is correct and the ODBC driver is installed.
  - Verify API keys and endpoints for Azure services.
- **Table Creation Issues:**
  - Confirm your user has permissions to create tables in the target database.
- **Embedding/Vector Errors:**
  - Ensure the VECTOR data type is enabled in your Azure SQL DB (preview feature).
  - Use the correct double-casting in SQL queries as shown in the app.
- **Performance:**
  - Large PDFs or many files may take time to process and embed. Monitor resource usage.
- **Streamlit UI Issues:**
  - Refresh the page or restart the app if UI elements do not update as expected.

## Resources
- [Azure SQL DB Vector Support](https://devblogs.microsoft.com/azure-sql/eap-for-vector-support-refresh-introducing-vector-type/)
- [Azure Document Intelligence](https://learn.microsoft.com/azure/ai-services/document-intelligence/)
- [Azure OpenAI Service](https://learn.microsoft.com/azure/ai-services/openai/)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [Project GitHub Repository](https://github.com/Azure-Samples/azure-sql-db-vector-search/tree/main/RAG-with-Documents)

---

**For any additional questions or to contribute, please refer to the main project README or open an issue in the repository.**
