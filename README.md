
# **Multilingual Retrieval-Augmented Generation (RAG) System**

## **Overview**
The Multilingual Retrieval-Augmented Generation (RAG) system is designed to extract data from multilingual PDFs and scanned documents. It enables users to query the extracted content and receive accurate responses in the same language as the input document. The system supports languages including English, Hindi, Bengali, and Chinese.

## **Key Features**
- **Multilingual Support**: Processes documents in multiple languages and provides responses in the query language.
- **Hybrid Search**: Combines keyword search (BM25) and similarity search (using cosine or L2 distance) to retrieve relevant content.
- **Contextual Response Generation**: Uses Google’s Gemini Pro model to generate contextually relevant answers based on extracted content.
- **Chat Memory Functionality**: Remembers previous interactions to provide coherent responses in multi-turn conversations.

## **System Architecture**
1. **Document Upload**: Users can upload PDFs in various languages for processing.
2. **Text Extraction**: The system extracts text from both scanned and digital PDFs.
3. **Chunking**: The extracted text is divided into chunks with overlaps to maintain context.
4. **Embedding Generation**: Multilingual BERT is used to generate embeddings for the text chunks.
5. **Storage**: Normalized embeddings are stored in a FAISS vector database.
6. **Retrieval Process**: Hybrid search retrieves relevant chunks based on the user’s query.
7. **Response Generation**: Relevant chunks are passed to the Gemini Pro model to generate answers.
8. **Chat Memory**: The system retains previous query responses for contextual awareness in ongoing conversations.


## **Usage**
1. Upload a PDF document via the user interface.
2. Enter a query in the same language as the document.
3. Receive generated responses based on the document’s content.

## **Limitations**
- Performance may vary with complex queries or documents with heavy formatting.
- The system's efficiency is dependent on the quality of the input PDFs.

## **Future Improvements**
- Fine-tuning retrieval models for better accuracy on specific tasks.
- Adding a translation feature to allow querying in a different language than the document.
