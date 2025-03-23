# 🎵 Shazam Clone : Audio Transcription & Subtitle Search

## Overview

This project focuses on building **AI-powered search systems**, **audio-to-text conversion**, and **interactive search applications**. It integrates **search engine technologies, vector embeddings, speech-to-text models, and subtitle processing** to enable efficient information retrieval and media analysis.

## Objective

Develop an advanced search engine algorithm that efficiently retrieves subtitles based on user queries, leveraging natural language processing (NLP) and machine learning to enhance search relevance and accuracy.

- Keyword-based vs. Semantic Search Engines
- Keyword-Based Search Engine: Relies on exact keyword matches between user queries and indexed documents.
- Semantic Search Engine: Understands the meaning and context of queries and documents beyond keyword matching.

## Core Enhancements

### 1. **Real-time Audio Recognition**  
- Now supports **live microphone input** for real-time audio-to-text conversion.  
- Users can search using their voice instead of uploading audio files.  

### 2. **Multi-language Support**  
- The system now supports **multiple languages**, expanding beyond English.  
- Improves accessibility and usability across different regions.  

### 3. **Security & Performance Fixes**  
- **Removed hardcoded API keys** for better security.
- **Optimized GPU compatibility** for seamless performance across different environments.
- **Improved dependency management** by replacing inline `pip install` commands.  

## Core Logic

The search engine compares user queries against subtitle documents through these key steps:

### 1. Preprocessing the Data
- Extract and clean subtitle data (remove timestamps, punctuation, etc.).
- Subset the dataset if compute resources are limited (e.g., use 30% of the data).

### 2. Generating Text Vectors
- Convert subtitle text into vector embeddings using different techniques:
  - **BOW (Bag of Words) / TF-IDF** → For keyword-based search.
  - **BERT-based SentenceTransformers** → For semantic search.

### 3. Implementing a Document Chunker
- Break down large subtitles into smaller chunks to preserve context.
- Use overlapping windows to prevent information loss.

### 4. Storing Embeddings in FAISS (New Upgrade)
- **Replaced ChromaDB with FAISS** for **faster similarity search and better scalability**.
- Stores vector representations of subtitle chunks for efficient retrieval.

### 5. Retrieving Documents Based on User Query
- Convert user **audio query to text** (using AssemblyAI or other ASR models).
- Vectorize the text query and compute **cosine similarity** between query and subtitle embeddings.
- Rank and return the most relevant subtitle segments.

## Notebooks & Descriptions

### 1. Audio_2_Text.ipynb
- Converts **audio files or real-time speech** into text using **AssemblyAI**.
- Now supports **live microphone input** for real-time speech-to-text conversion.

### 2. FAISS_Embeddings.ipynb (Updated)
- Uses **FAISS** for **faster and optimized similarity search**.
- Enhances **scalability and performance for large datasets**.

### 3. Streamlit_Search_Engine_Demo.ipynb (New UI Upgrade)
- Implements an **interactive search engine UI using Streamlit**.
- Replaces Gradio for a more flexible and feature-rich web interface.
- Supports **voice search, text search, and hybrid search**.

### 4. Search_Engine_Extracting_Data.ipynb
- Focuses on **data extraction, scraping, and indexing** for a search engine.
- Handles **text preprocessing, tokenization, and document structuring**.

### 5. Shazam_Clone_Search_Engine.ipynb
- Builds a **music recognition system** similar to **Shazam**.
- Enables **identification of audio, speeches, or sound patterns from audio samples**.

### 6. Subtitles_Chunking.ipynb
- Processes **subtitle files** by **splitting them into smaller text segments**.
- Helps in **automatic subtitle generation, video search indexing, and multilingual translation**.

### 7. Testing_Search_Mechanism.ipynb
- Evaluates the effectiveness of different **search algorithms**.
- Tests **ranking models, BM25, TF-IDF, and vector-based retrieval methods**.

## Libraries Used :

- streamlit (New)
- gradio
- assemblyai
- pydub
- python-dotenv
- faiss (New)
- sentence-transformers

## Applications

- **Multimodal Search Engines**: Combining **text, audio, and embeddings** for **intelligent retrieval**.
- **Real-time Voice Search**: Users can **speak queries directly**, enhancing usability.
- **Audio & Music Recognition**: Implementing a **Shazam-like** system for **identifying songs and sound patterns**.
- **Semantic Search & NLP**: Using **vector embeddings for AI-driven document retrieval**.
- **Interactive Demos & UI**: **Streamlit-powered** web UI for easy-to-use search interfaces.
- **Video & Subtitle Processing**: Extracting and structuring **subtitles for indexing and accessibility**.

## Summary

This project integrates **cutting-edge AI search technologies**, **text/audio processing**, and **interactive search tools**. With **real-time voice search, multi-language support, FAISS-based search, and enhanced security**, it offers **advanced media analysis, transcription, and retrieval capabilities**. 🚀

---

### Special Thanks
A huge thank you to **Kanav Bansal** and **Innomatics Research Lab** for their support and insights in making this project better! 🙏

### Want to Contribute?

Feel free to **open issues, suggest improvements, or contribute** to enhance this project!

