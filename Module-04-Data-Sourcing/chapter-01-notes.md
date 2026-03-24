# Week 4, Session 1

## 📌 Overview
This was a **live Q&A session** focused on troubleshooting and clarifying doubts about **Project 1 submissions, API usage, deployment issues, and graded assignments**.  
Unlike lecture sessions, this was designed to resolve student queries.

---

## 📝 Detailed Notes

### 1. Project 1 Queries
- Submission must be **publicly accessible**.  
- Evaluation uses **YAML test scripts** with realistic queries.  
- Marks depend on correctness of responses, not just endpoint availability.  
- Common issues:
  - Endpoint returning JSON but portal rejecting submission.  
  - Misconfigured headers or incorrect response formats.  

---

### 2. API & Tooling Issues
- **OpenAI API keys**:
  - Students reported expired/invalid keys.  
  - Instructor explained differences between **AI Pipe** and **AI Proxy** setups.  
- **FastAPI deployment**:
  - Errors on Vercel/Ngrok traced to headers and endpoint mismatches.  
  - Fixes: adjust headers, check Chrome DevTools.  
- **Google Authentication (GA2)**:
  - Client ID defaults caused failures.  
  - Required multiple services running in parallel.  

---

### 3. Graded Assignment Challenges
- **GA2 Q2 – Image compression**:
  - Difficulty reducing image size to 400 KB.  
  - Suggested tools: Pillow, Sharp, ImageOptim.  
- **GA3 Q11 – Prompt engineering**:
  - Task: force LLM to answer “Yes.”  
  - Highlighted creativity in prompt design over coding.  
- **GA3 Q7 – Topic modeling**:
  - Some answers not saving correctly in portal.  
  - Advised raising issue in Discourse for debugging.  

---

### 4. Course Design Insights
- Early weeks are **tool-heavy**: WSL, FastAPI, Ngrok, image compression, deployment.  
- Later weeks shift to **data science tasks**: regression, correlation, sourcing, preparation.  
- Aim: simulate real-world projects requiring multiple tools quickly.  

---

### 5. Instructor Guidance
- Raise debugging issues early, not last minute.  
- Collaboration encouraged: peer troubleshooting is part of learning.  
- Non-coding background students reminded that persistence builds skill.  
- Distinction: **learning sessions** focus on teaching; **query sessions** focus on troubleshooting.  

---

## 🎯 Key Takeaways
- Secure API key management and correct endpoint formatting are critical.  
- Project evaluation depends on YAML test scripts, not just deployment.  
- Creativity in prompt engineering is as important as coding.  
- Early weeks intentionally heavy to build tool familiarity.  
- Debugging and collaboration are essential parts of the workflow.  

---

## ✅ Checklist for Practice
- [ ] Verify API key setup (AI Pipe/Proxy)  
- [ ] Test FastAPI deployment on Vercel/Ngrok with correct headers  
- [ ] Practice image compression with Pillow/Sharp  
- [ ] Experiment with creative prompt engineering  
- [ ] Document and debug topic modeling outputs  
