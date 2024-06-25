# Autonomous-RAG-Phi_data-

Project Summary
- Environment Setup:

Utilizes the dotenv library to load environment variables, specifically the OpenAI API key.
Sets up the PostgreSQL database URL for storing the assistant's data.
- Assistant Setup:

Defines a function setup_assistant to create an instance of an assistant named "AutoRAG".
Configures the assistant with:
- A language model (LLM) from OpenAI.
- Storage in a PostgreSQL database.
- A knowledge base using vector embeddings for document retrieval.
- Clear instructions for handling user queries.
Knowledge Base Management:

Implements add_document_to_kb to read and add documents (PDF format) to the assistant's knowledge base.
Uses a PDF reader to extract and load document content into the knowledge base, logging the outcome.
Query Handling:

Defines query_assistant to process user queries through the assistant.
Collects responses incrementally and returns the final consolidated response.
Main Execution:

Applies asynchronous capabilities using nest_asyncio.
Retrieves the LLM model name from environment variables (defaulting to GPT-4o if not set).
Initializes the assistant with the specified LLM model.
Adds a sample PDF document to the assistant's knowledge base.
Runs a sample query to demonstrate the assistant's functionality.
Tools and Features:

Integrates tools like DuckDuckGo for web searches when the knowledge base lacks relevant information.
Enables capabilities to reference chat history and add timestamps to instructions.
Provides a detailed description and instructions to ensure the assistant delivers accurate and helpful responses.
Logging and Debugging:

Configures a logger to track the addition of documents to the knowledge base and any errors encountered.
Activates debug mode to facilitate troubleshooting and enhance transparency in the assistant's operations.
