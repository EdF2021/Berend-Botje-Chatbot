# Berend Botje Chatbot
> **powered by ChatGPT 

Kickstarter om snel de Basis van een Chatbot te maken die gebruik maakt van de ChatGPT API en een eigen knowledge base. 
This repo contains one notebook and two basic Streamlit apps:
- `powering_your_products_with_chatgpt_and_your_data.ipynb`: A notebook containing a step by step process of tokenising, chunking and embedding your data in a vector database, and building simple Q&A and Chatbot functionality on top.
- `search.py`: A Streamlit app providing simple Q&A via a search bar to query your knowledge base.
- `chat.py`: A Streamlit app providing a simple Chatbot via a search bar to query your knowledge base.

To run either version of the app, please follow the instructions in the respective README.md files in the subdirectories.

## How it works

The notebook is the best place to start, and is broadly laid out as follows:
- **Lay the foundations:**
    - Set up the vector database to accept vectors and data
    - Load the dataset, chunk the data up for embedding and store in the vector database
- **Make it a product:**
    - Add a retrieval step where users provide queries and we return the most relevant entries
    - Summarise search results with GPT-3
    - Test out this basic Q&A app in Streamlit
- **Build your moat:**
    - Create an Assistant class to manage context and interact with our bot
    - Use the Chatbot to answer questions using semantic search context
    - Test out this basic Chatbot app in Streamlit

Once you've run the notebook and tried the two Streamlit apps, you should be in a position to strip out any useful snippets and start your own Q&A or Chat application.

## Limitations

- This app uses Redis as a vector database, but there are many other options highlighted `../examples/vector_databases` depending on your need.
- This is a simple starting point - if you hit issues deploying your use case you may need to tune (non-exhaustive list):
    - The prompt and parameters for the model for it to answer accurately
    - Your search to return more relevant results
    - Your chunking/embedding approach to store the most relevant content effectively for retrieval
