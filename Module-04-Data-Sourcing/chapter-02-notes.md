# 📘 Tic Tac Toe AI Agent – Evaluation & Deployment Workflow

This project demonstrates:
- JSON‑driven evaluation workflow
- Round‑based GitHub repo automation
- Deployment with Docker + Hugging Face Spaces
- AI integration using FastAPI + Pydantic

---

## 📌 Core Concepts Covered

### Evaluation Workflow
- Round‑based tasks:
  - **Round 1**: create repo, add files, enable GitHub Pages
  - **Round 2**: update files in existing repo
- JSON request/response cycle with evaluation URL
- Immediate “OK” response required before task execution
- Automatic API‑triggered evaluation within 10 minutes

### Project Structure
- Separate folders:
  - `src` → source code
  - `test` → testing
  - `README.md` → documentation
- Importance of `__init__.py` for Python package recognition
- Requirements management via `requirements.txt` generated with `pip freeze`

### Deployment
- Hugging Face Spaces setup with SSH keys
- Dockerfile essentials:
  - base image
  - copy files
  - install dependencies
  - expose port
  - run server
- Secrets management via environment variables (model name, API keys, etc.)
- Demo: deploying Tic Tac Toe app with FastAPI

### AI Integration
- Pydantic `BaseModel` for structured outputs (AI move must be integer 0–8)
- Prompt engineering for Tic Tac Toe agent:
  - Provide board state, available moves, winning combos
  - AI chooses best move; retry mechanism if invalid
- Environment variable‑driven model selection (OpenAI, Gemini, etc.)

---

## 📝 Step‑by‑Step Notes

### Round 1 Workflow
1. Receive JSON request → send immediate “OK” response  
2. Create new GitHub repo  
3. Add specified files (provided in JSON)  
4. Enable GitHub Pages  
5. API auto‑hits evaluation URL with repo URL, commit ID, and task metadata  

### Round 2 Workflow
1. Receive JSON request → send immediate “OK” response  
2. Update files in existing repo (identified via unique task ID)  
3. Maintain previous context (licenses, attachments)  
4. Auto‑hit evaluation URL with updated repo info  

### Deployment Demo (Tic Tac Toe App)
- Generate SSH key → add to Hugging Face  
- Create new Space → choose Docker template  
- Clone repo locally → add `src`, `requirements.txt`, `Dockerfile`, `README.md`  
- Push changes → Hugging Face auto‑builds container  
- Run app locally with `uvicorn` for testing  

### AI Agent Setup
- Define `AI_move` class with constraints (0–8)  
- Use `agent.run_sync()` with structured prompt:  
  - Board state (array of 9 positions)  
  - Available moves  
  - Winning combos  
- Return structured integer output instead of free text  

---

## 🎯 Key Takeaways
- **Automation‑first mindset**: JSON‑driven evaluation ensures reproducibility  
- **Repo discipline**: Each Round 1 task = new repo; Round 2 = updates only  
- **Deployment best practices**: Docker + Hugging Face Spaces with secrets for secure API usage  
- **AI reliability**: Structured outputs via Pydantic prevent invalid moves; retry logic ensures robustness  
- **Flexibility**: Environment variables allow switching between models (OpenAI, Gemini, etc.) without code changes  

---

## 📜 License
MIT License
