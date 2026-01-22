# EduMiniAI
Lightweight AI for solving school problems.

---

# 📘 EduMiniAI  
### A Lightweight Offline AI for Solving Elementary School Tasks (Grades 1–5)

**EduMiniAI** is a compact, fast, fully offline AI assistant designed to help children in grades 1–5 solve school tasks.  
It is powered by **Qwen2.5**, runs locally through **Ollama**, and includes a custom **FastAPI backend**, **Next.js frontend**, and full **Docker containerization**.

This project demonstrates how to build a real, production‑ready product on top of a local LLM — from idea to architecture to deployment.

---

## 🚀 Features

- Solves tasks for grades 1–5:
  - arithmetic  
  - word problems  
  - logic  
  - Russian language basics  
  - general knowledge  
- Step‑by‑step explanations  
- Simple, child‑friendly answers  
- Fully offline (no external APIs)  
- Fast inference thanks to a lightweight model  
- Clean, extensible architecture  

---

## Tech Stack
----------------------------------------------
| Component        | Technology              |
|------------------|-------------------------|
| Model            | Qwen2.5 (via Ollama)    |
| Backend          | FastAPI, Python 3.11    |
| Frontend         | Next.js / React         |
| Containerization | Docker + Docker Compose |
| API Format       | REST                    |
----------------------------------------------
---

## Project Architecture

```
EduMiniAI/
  backend/
    app/
      main.py
      routers/
        solve.py
      services/
        llm.py
      models/
        request.py
        response.py
    Dockerfile
    requirements.txt

  frontend/
    ... (Next.js application)
    Dockerfile

  docker/
    docker-compose.yml

  README.md
```

---

## API

### POST `/api/solve`

**Request:**

```json
{
  "grade": 3,
  "task": "Masha had 5 apples and gave away 2. How many are left?"
}
```

**Response:**

```json
{
  "steps": [
    "She had 5 apples",
    "She gave away 2",
    "5 - 2 = 3"
  ],
  "answer": "3 apples"
}
```

---

## Prompt Logic

The model uses a system prompt optimized for elementary‑level explanations:

```
You are a school assistant for children in grades 1–5.
Explain answers simply and clearly.
For math tasks, show step-by-step reasoning.
For word problems, explain in plain language.
Response format:
1. Short restatement of the task
2. Step-by-step solution
3. Final answer
```

---

## Running with Docker

### 1. Install Ollama and pull the model

```
ollama pull qwen2.5
```

### 2. Start the full stack

```
docker compose up -d
```

### 3. Open the frontend

```
http://localhost:3000
```

---

## Example Tasks

### Math  
**Task:**
“Masha had 12 candies. She ate 4. How many are left?”

**AI Output:**
Step‑by‑step explanation + final answer.

---

### Russian Language  
**Task:**
“Parse the sentence: Мама мыла раму.”

**AI Output:**
Parts of speech + simple explanation.

---

### Logic  
**Task:**
“You have 3 boxes: apples, pears, apples+pears. All labels are wrong. How do you find the correct one?”

**AI Output:**
Clear step‑by‑step reasoning.

---

## Roadmap

- Add “Explain like a teacher” mode
- Add task generation
- Add history of solved tasks
- Add English‑language support
- Build a mobile version

---

## Author

**Vepa Allamyradov**
AI Architect • Backend Developer • Digital Transformation Engineer
Dubai, UAE

---
