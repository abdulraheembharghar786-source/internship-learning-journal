# Week 3, Session 4

## 📌 Overview
This session focused on **OpenAI API usage** with `httpx` and `curl`, exploring embeddings, chatbot design, and image encoding. It blended **theory (semantic embeddings)** with **hands‑on coding (API calls, Base64, role‑based chat)**.

---

## 📝 Detailed Notes

### 1. Session Agenda
- API requests, headers, JSON payloads  
- Base64 encoding/decoding of images  
- Word embeddings and vector databases  
- Multimodal embeddings and function calling  
- Mini‑projects:
  - Chatbot with history (memory simulation)  
  - Product detail extraction from images  

---

### 2. Word Embeddings
- **Analogy**: child deciding where to place an apple (kitchen, room, hall) based on probabilities.  
- Embeddings assign **probabilities across dimensions**.  
- Key points:
  - Lexicographic similarity ≠ semantic similarity  
  - Embeddings capture meaning in **high‑dimensional vectors**  
  - Foundation for semantic search and vector databases  

---

### 3. OpenAI API Documentation
- **Model chosen**: GPT‑4.1 nano (cost‑efficient).  
- **API types**:
  - Chat completion (older, widely used)  
  - Response API (newer, more features, not fully integrated yet)  
- Importance of endpoints and references.  

---

### 4. Secure API Key Setup
- Store keys in `.bashrc` for safety.  
- Avoid exposing keys in GitHub repos.  
- Alternative: load keys in Python via `os.environ`.  

---

### 5. Building the Chatbot
- **Message structure**: list of dicts with `role` + `content`.  
- Roles: `developer/system`, `user`, `assistant`.  
- LLMs lack memory → pass **conversation history manually**.  
- Demonstration:
  - User query → assistant reply → both appended to history.  
  - Context maintained across multiple queries.  
- Optimization: limit history length to save tokens.  

---

### 6. Base64 Encoding Project
- Convert image → binary → Base64 string.  
- Convert Base64 string back → binary → image file.  
- Verified **no data loss** using SHA256 checksum.  
- Ensures reproducibility of image data.  

---

### 7. Vector Embeddings & Databases
- Words mapped into **vectors in high‑dimensional space**.  
- Each dimension captures semantic features.  
- Foundation for:
  - Vector databases (retrieval‑augmented generation)  
  - Multimodal embeddings (text + image)  
  - Function calling (structured outputs)  

---

## 🎯 Key Takeaways
- **Embeddings** enable semantic understanding.  
- **API calls** require secure key handling and structured JSON.  
- **Chatbots** simulate memory via message history.  
- **Base64 encoding** ensures reproducibility of binary data.  
- **Vector databases + multimodal embeddings** power advanced AI workflows.  

---

## ✅ Checklist for Practice
- [ ] Set up API key securely in `.bashrc`  
- [ ] Make a sample `httpx` request to OpenAI API  
- [ ] Build a chatbot with role‑based messages  
- [ ] Encode/decode an image with Base64 and verify checksum  
- [ ] Experiment with embeddings and visualize vectors  
