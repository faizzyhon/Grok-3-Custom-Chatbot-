# Grok AI Chatbot UI

## Overview
Grok AI Chatbot UI is a **Python-based chatbot** built with **PyQt5**, designed to provide a responsive chat interface using the **Grok-3-Latest** API. This chatbot is customizable and can be used by anyone to provide AI-driven responses related to their website or business. 

## Features
✅ **Customizable Knowledge Base** – Restrict chatbot responses to specific topics or domains.
✅ **Light & Dark Mode Toggle** – Seamless theme switching for better user experience.
✅ **Real-time Chat Interface** – Users can enter queries and receive instant responses.
✅ **Grok API Integration** – Utilizes the **Grok-2-Latest** model for intelligent conversations.
✅ **Minimalistic UI** – Clean, simple, and easy-to-use interface.

## Installation & Setup
1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/Grok-Chatbot-UI.git
   cd Grok-Chatbot-UI
   ```

2. **Create a Virtual Environment & Install Dependencies**
   ```bash
   python -m venv myvenv
   source myvenv/bin/activate  # On Windows use: myvenv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Run the Application**
   ```bash
   python app.py
   ```

## Configuration
To customize the chatbot for your own website, update the following parts in `app.py`:

### 1. **Set Your API Key**
Replace `your-grok-api-key-here` with your actual API key:
```python
API_KEY = "your-grok-api-key-here"  # Replace with your actual key
```

### 2. **Modify Knowledge Base**
To make the chatbot specific to your website, update the `get_response` method in `app.py`. Add logic to filter responses based on allowed topics.

Example:
```python
allowed_topics = ["projects", "skills", "education", "certifications", "contact"]
if not any(topic in user_text.lower() for topic in allowed_topics):
    bot_response = "I'm sorry, but I can only answer questions related to the website."
```

### 3. **Change UI Elements**
Modify the window title and labels in `initUI`:
```python
self.setWindowTitle("Your Website AI Chatbot")
```

## Contributing
Feel free to fork this project and submit pull requests! If you encounter any issues, open a GitHub issue.

## License
This project is licensed under the **MIT License**.

---
Made with ❤️ by Muhammad Faizan
