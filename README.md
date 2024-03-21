# Document-Query-with-Ollama
How to build a RAG chatbot using Ollama - Serve LLMs locally


Why Ollama?
Ollama is a streamlined tool for running open-source LLMs locally, including Mistral and Llama 2. Ollama bundles model weights, configurations, and datasets into a unified package managed by a Model file.
Ollama supports a variety of LLMs including LLaMA-2, uncensored LLaMA, CodeLLaMA, Falcon, Mistral, Vicuna model, WizardCoder, and Wizard uncensored.


By using Ollama, you will be able to run LLMs locally, which means your data stays safe and secure.
App Overview
On a fundamental level, the workflow of the app is remarkably straightforward:
1. A user submits a list of URLs (one per line) and enters a question.
2. The app processes the input, fetching the content from the provided URLs.
3. The text content is split into manageable chunks.
4. These chunks are converted into embeddings using the nomic-embed-text model and stored in a vector database ( Chroma ).
5. The user's question is processed through a Retrieval-Augmented Generation (RAG) pipeline, which retrieves relevant document sections and generates an answer using the Mistral 7B model.
