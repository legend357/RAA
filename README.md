from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def home():
    return {"message": "Welcome to RAA API"}

@app.get("/chat")
def chatbot_response(query: str):
    return {"response": f"AI Response for: {query}"}

# Run this using: uvicorn main:app --host 0.0.0.0 --port 8000
