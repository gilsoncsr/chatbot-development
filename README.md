# 🩺 ChatGPT-Like Medical Assistant

This project is a simple **Streamlit web app** that simulates a **ChatGPT-like experience** tailored to a **medical clinic receptionist** scenario. It uses the OpenAI GPT API to interact with users and help simulate booking medical appointments.

---

## 🧰 Features

- Chat interface powered by OpenAI's `gpt-3.5-turbo` model.
- Persistent conversation through `st.session_state`.
- Custom behavior: the assistant acts like a **medical clinic secretary**.
- Step-by-step flow for scheduling consultations.
- Rejects unsupported health plans (e.g., NotreDame).

---

## 📦 Requirements

Install the dependencies with:

```bash
pip install streamlit openai
```

---

## 🔐 API Key Setup

Create a `.streamlit/secrets.toml` file with the following structure:

```toml
OPENAI_API_KEY = "your-openai-api-key"
```

This file is used by `st.secrets["OPENAI_API_KEY"]` to securely load your OpenAI key.

---

## 🚀 Running the App

Simply run:

```bash
streamlit run app.py
```

---

## 🧠 Assistant Instructions

The assistant is instructed to behave like a **medical clinic receptionist**, handling multiple specialties and following a defined protocol when a user requests an appointment:

1. Ask which health insurance the user has.
2. Ask for preferred date and time.
3. If the insurance is **Notredame**, inform the user that it's not accepted.

---

## 📸 User Interface Example

- Users type questions or requests using the `st.chat_input` at the bottom.
- The assistant replies in a chat bubble format.
- Chat history is preserved during the session.

---

## 💡 Sample Conversation

**User:** I want to book an appointment.  
**Assistant:** Sure! What health insurance do you have?  
**User:** Notredame.  
**Assistant:** I'm sorry, we do not accept Notredame.  

---

## 📁 File Structure

```
📦 your-project
├── app.py
└── .streamlit
    └── secrets.toml
```
