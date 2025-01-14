# Chat-with-files-RAG-application
The RAG Agent is an interactive tool that allows users to upload documents and query them using natural language. It processes the uploaded files, extracts relevant information, and provides accurate answers. 


**Use Case**

The RAG Agent is designed for users who need to extract information from documents efficiently. It is particularly useful for:
* Students and Researchers: Quickly finding information in academic papers or textbooks.
* Professionals: Accessing key insights from reports or manuals without reading the entire document.
* General Users: Engaging with any uploaded content in a conversational manner, making information retrieval intuitive.
-------------------------------------------------------------------------------------------

**Tech Stack**

**Python**: The primary programming language for implementing the agent.

**Sentence Transformers**: For generating embeddings of text paragraphs, enabling semantic search capabilities.

**ChromaDB**: A vector database for storing and retrieving document embeddings efficiently.

**PyMuPDF**: For handling PDF file uploads and extracting text content.

**Google Generative AI**: For generating responses based on user queries and context derived from the uploaded documents.

**NumPy & SciPy**: For numerical operations and data manipulation.

-------------------------------------------------------------------------------------------

**Code Flow**


**Setup Environment**: Install necessary libraries using pip:
bash
pip install -q sentence-transformers wikipedia-api numpy scipy flash_attn PyMuPDF google-generativeai chromadb==0.3.29

**File Upload**: Users upload their documents (e.g., PDFs). The code captures the uploaded file name.

**Text Extraction**: The agent reads the contents of the uploaded document using PyMuPDF, extracting text page by page.

**Chunking Text**: The extracted text is split into paragraphs for more manageable processing.

**Embedding Generation**: Using Sentence Transformers, each paragraph is converted into an embedding vector for semantic search.

**Database Storage**: The embeddings are stored in ChromaDB along with their corresponding text paragraphs for efficient retrieval.

**Query Handling**: Users input their queries, which are also converted into embeddings.

**Similarity Search**: The agent performs a similarity search in ChromaDB to find the most relevant paragraphs based on the user's query.

**Response Generation**: The relevant contexts are compiled and passed to Google Generative AI to generate a coherent response based on the query and context.

**Output Display**: Finally, the generated response is displayed to the user, providing answers directly related to their query.

-------------------------------------------------------------------------------------------
This structured approach ensures that users can interact with their documents effectively, enhancing their ability to retrieve information quickly and accurately.
