# Box AI API Master Class

A comprehensive workshop designed to teach developers how to leverage the Box AI API capabilities through hands-on Jupyter notebook exercises. This interactive learning experience covers the full spectrum of Box AI APIs, from basic document Q&A to advanced structured data extraction and custom AI agents.

## What You'll Learn

This workshop provides practical, hands-on experience with:

- **Document Intelligence**: Ask questions and get answers from single documents or curated document collections
- **Data Extraction**: Extract structured and unstructured data from various document types (PDFs, Word docs, etc.)
- **Box Hubs**: Use Box's Retrieval Augmented Generation (RAG) capabilities across large document sets
- **Custom AI Agents**: Create and deploy specialized AI agents through Box AI Studio
- **Enterprise Integration**: Build production-ready workflows using the Box Python SDK

## Prerequisites

### Box Account Requirements

- **Box Enterprise Account** with the following enabled:
  - Box AI APIs
  - Box AI Studio  
  - Box Hubs
- **Box Application** configured with:
  - Client Credentials authentication
  - `Manage AI` scope enabled
  - Application enabled in Box admin console
- **Box User ID** of the application creator

### Technical Requirements

- **Python 3.11+**
- **Jupyter Notebook** or **JupyterLab**
- Ability to create Python virtual environments
- Basic familiarity with Python and REST APIs

## Setup Instructions

### 1. Environment Setup

Clone this repository and create a virtual environment:

```bash
git clone [repository-url]
cd box-ai-api-master-class

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

### 2. Install Dependencies

```bash
pip install -r .requirements.txt
```

Or install manually:
```bash
pip install box-sdk-gen python-dotenv jupyter
```

### 3. Launch Jupyter

```bash
jupyter notebook
# or
jupyter lab
```

### 4. Complete Setup

**Important**: Start with `1-Setup.ipynb` first. This notebook will:

- Guide you through entering your Box credentials
- Create all necessary Box objects (folders, files, hubs, metadata templates, AI agents)
- Generate a `.env` file with all required configuration
- Upload sample documents to Box for the exercises

**⚠️ Security Note**: This workshop uses a `.env` file for convenience. In production, use secure credential management solutions.

## Workshop Structure

### Exercise 1: Setup (`1-Setup.ipynb`)
**Prerequisites Setup & Box Object Creation**
- Configure authentication with Box APIs
- Create folder structure and upload sample documents
- Set up Box Hubs, metadata templates, and AI agents
- Generate environment configuration for subsequent exercises

### Exercise 2: Document Q&A (`2-Document_QnA_with_ask.ipynb`)  
**Single Document Question Answering**
- Learn the `/ask` endpoint for document Q&A
- Implement conversation history for contextual follow-ups
- Work with citations and document references
- **Sample Document**: US Parole Commission policy guidelines

### Exercise 3: Hub Q&A (`3-Hub_QnA_with_ask.ipynb`)
**Multi-Document RAG with Box Hubs**
- Query across curated document collections
- Understand Box's managed RAG implementation  
- Analyze complex document relationships
- **Sample Documents**: Clinical drug trial documentation

### Exercise 4: Flexible Extraction (`4-Flexible_extraction_with_extract copy.ipynb`)
**Unstructured Data Extraction**
- Use the `/extract` endpoint with natural language prompts
- Extract key-value pairs without predefined schemas
- Handle various document formats and structures
- **Sample Document**: W-2 tax form

### Exercise 5: Structured Extraction (`5-Structured_extraction_with_extract_structured copy.ipynb`)
**Metadata Template-Based Extraction**
- Leverage Box Metadata Templates for consistent extraction
- Process multiple documents with identical schemas
- Understand enterprise data standardization
- **Sample Documents**: Invoice collection

### Exercise 6: AI Agents (`6-Box_agents_and_AI_APIs.ipynb`)
**Advanced AI Agents & Custom Models**
- Use Box's Enhanced Extract Agent for improved accuracy
- Create and deploy custom Box AI Studio agents
- Compare default vs. specialized agent performance
- **Sample Documents**: Legal due diligence and purchase agreements

## Generated Code Files

Each exercise generates standalone Python scripts that you can use as:
- **Starting points** for your own projects
- **Reference implementations** for production workflows
- **CLI tools** for testing and development

Generated files:
- `box_ai_qna_single.py` - Interactive single document chat
- `box_ai_qna_hub.py` - Interactive multi-document chat
- `box_ai_flexible_extract.py` - Flexible data extraction
- `box_ai_structured_extract.py` - Template-based extraction
- `box_ai_enhanced_extract.py` - Enhanced extraction agent
- `box_ai_studio_agent.py` - Custom AI Studio agent

## Sample Documents

The workshop includes carefully selected sample documents that demonstrate real-world use cases:

- **Government Policy Documents** (Exercise 2)
- **Clinical Trial Data** (Exercise 3)  
- **Tax Forms** (Exercise 4)
- **Business Invoices** (Exercise 5)
- **Legal Contracts** (Exercise 6)

## Key Features Demonstrated

- **Stateless Conversation Management**: Maintain context across API calls
- **Citation Tracking**: Trace AI responses back to source documents
- **Batch Processing**: Handle multiple documents efficiently  
- **Custom Field Definitions**: Define extraction schemas programmatically
- **Agent Customization**: Tailor AI behavior for specific use cases
- **Error Handling**: Robust error management for production environments

## Production Considerations

While this workshop uses simplified authentication and storage for learning purposes, consider these factors for production deployments:

- **Security**: Use secure credential management (AWS Secrets Manager, Azure Key Vault, etc.)
- **Scalability**: Implement proper async/await patterns for concurrent processing
- **Monitoring**: Add logging, metrics, and error tracking
- **Rate Limiting**: Implement appropriate throttling for API calls
- **Data Privacy**: Ensure compliance with your organization's data handling policies

## Support & Resources

- **Box Developer Documentation**: [developer.box.com](https://developer.box.com)
- **Box AI APIs**: [Box AI Documentation](https://developer.box.com/guides/box-ai/)
- **Box Python SDK**: [box-python-sdk](https://github.com/box/box-python-sdk-gen)
- **Box Community**: [Box Developer Community](https://community.box.com/box-platform-5)

## Getting Help

If you encounter issues:

1. **Check Prerequisites**: Ensure all Box features are enabled in your account
2. **Verify Setup**: Confirm the setup notebook completed successfully
3. **Review Logs**: Check Jupyter output for detailed error messages
4. **Community Support**: Post questions in the Box Developer Community

---

**Ready to get started?** Open `1-Setup.ipynb` and begin your Box AI journey!