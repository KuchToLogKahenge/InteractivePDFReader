# Creating an interactive PDF reader using LangChain and Streamlit. 
### 1. When a file is uploaded, the PDF reader will extract chunks of text from it and generate embeddings for each chunk. It will then create a searchable database.
### 2. Users can interact with the PDF reader with a chatbot.
### 3. When a question is presented to the chatbot, the reader generates an embedding for the question and searches the database for answers.
### 4. The most relevant chunk and the chat history are then used as context to generate an answer in natural language using a large language model (LLM).
### 5. This response is shown to the user and appended to the chat history.

## Task1 -
### Import the libraries and modules that will be used to build the application. To complete this task, import the following libraries:

* ### streamlit: This library will be used to create the frontend of the application.
* ### load_dotenv: This library will be used to import the API keys from the .env file.
* ### HuggingFaceEmbeddings and OpenAIEmbeddings: These methods are from the langchain.embeddings module and will be used to create embeddings for the text.
* ### ChatOpenAI: This method is from the langchain.chat_models module and will be used to initialize the LLM chat model.
* ### ConversationalRetrievalChain: This is a method from the langchain.chains module and will be used to create prompt chains.
* ### Chroma: This is a method from the langchain.vectorstores module and creates the database that you’ll be using to store your PDF embeddings.
* ### PyPDFLoader: This is a method in the langchain.document_loaders module and will be used to load the PDF.
* ### PdfReader and PdfWriter: These are methods in the PyPDF2 library and will be used to extract sections of the PDF files.
* ### NamedTemporaryFile: This is a method in the tempfile library and will be used to create a temporary PDF file.
* ### base64: This method is used for encoding binary files as text for displaying them on web pages.
* ### Note: The CSS is already written and available in the htmlTemplates.py file in the usercode directory. Import the expander_css, css, bot_template, and user_template strings from it.