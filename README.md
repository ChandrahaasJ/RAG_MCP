# RAG Information Retriever

A powerful MCP server that implements Retrieval-Augmented Generation (RAG) to efficiently retrieve and process important information from various sources. This server combines the strengths of retrieval-based and generation-based approaches to provide accurate and contextually relevant information.

## Features

1. **Intelligent Information Retrieval**
   - Semantic search capabilities
   - Context-aware information extraction
   - Relevance scoring and ranking
   - Multi-source data integration

2. **RAG Implementation**
   - Document embedding and indexing
   - Query understanding and processing
   - Context-aware response generation
   - Knowledge base integration

3. **Advanced Processing**
   - Text chunking and processing
   - Semantic similarity matching
   - Context window management
   - Response synthesis

## Setup

1. **Environment Configuration**
   Create a `.env` file with the following variables:
   ```
   OPENAI_API_KEY=your_openai_api_key
   VECTOR_DB_PATH=path_to_vector_database
   ```

2. **Dependencies**
   ```bash
   pip install langchain openai chromadb sentence-transformers
   ```

## Usage

### Basic Information Retrieval

```python
# Example: Simple query
query = "What are the key features of the system?"

# Example: Context-specific query
query = "How does the authentication system work?"
```

### Advanced Retrieval

```python
# Example: Multi-context query
query = {
    "question": "What are the system requirements?",
    "context": ["installation", "deployment", "configuration"]
}

# Example: Filtered retrieval
query = {
    "question": "Show me the API documentation",
    "filters": {
        "category": "api",
        "version": "2.0"
    }
}
```

## Architecture

```
retriever/
├── retrieverServer.py    # Main MCP server with RAG implementation
├── embeddings/          # Embedding models and processing
├── database/           # Vector database and storage
└── README.md
```

## How It Works

1. **Query Processing**
   - Input query is received and preprocessed
   - Query intent is analyzed
   - Relevant context is identified

2. **Information Retrieval**
   - Vector similarity search is performed
   - Relevant documents are retrieved
   - Context is assembled and ranked

3. **Response Generation**
   - Retrieved information is processed
   - Response is generated with context
   - Results are formatted and returned

## Performance Features

- Efficient vector search
- Caching of frequent queries
- Batch processing capabilities
- Asynchronous operations

## Security

- Input sanitization
- Rate limiting
- Access control
- Data encryption

## Running the Server

To start the MCP server in development mode:

```bash
mcp dev retrieverServer.py
```

## Error Handling

The system provides comprehensive error handling for:
- Invalid queries
- Missing context
- Database connection issues
- API rate limits
- Processing errors

## Best Practices

1. **Query Formulation**
   - Be specific in your queries
   - Provide relevant context
   - Use appropriate filters

2. **Context Management**
   - Keep context windows focused
   - Update knowledge base regularly
   - Monitor relevance scores

## Contributing

Feel free to submit issues and enhancement requests!

## Security Notes

- API keys should be kept secure
- Regular security audits
- Data privacy compliance
- Access control implementation
