# 🤖 Gemini Chatbot

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![Google Gemini](https://img.shields.io/badge/Google-Gemini%202.5%20Flash-4285F4?style=for-the-badge&logo=google)
![REST API](https://img.shields.io/badge/REST-API-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

A modern AI-powered chatbot built using **Python**, **Google Gemini API**, and a lightweight **REST API** architecture. The project provides a clean web interface for chatting with Google's Gemini model while exposing REST endpoints that can easily integrate with React, Flutter, mobile applications, or any frontend capable of making HTTP requests.

Unlike the original project, this version includes multiple UI and usability enhancements such as Dark Mode, ChatGPT-style chat bubbles, copy response functionality, conversation download, timestamps, and an improved user experience.

---

# ✨ Features

## 🤖 AI Chat

- Google Gemini 2.5 Flash integration
- REST API architecture
- Multi-turn conversations
- Mock responses when no API key is provided
- Lightweight Python backend
- Beginner-friendly project structure

---

## 🎨 Enhanced User Interface

Compared to the original project, the following improvements have been added:

- 🌙 Dark Mode
- 💬 ChatGPT-style chat bubbles
- 📋 Copy AI response with one click
- ⏳ "Gemini is thinking..." status indicator
- 📥 Download complete chat history (.txt)
- 🕒 Timestamp for every message
- 📜 Automatic scrolling to the latest message
- ⚡ Cleaner and more responsive interface

---

# 📸 Screenshots

> Add screenshots after uploading them.

### Home Page

```
images/home.png
```

---

### Dark Mode

```
images/dark-mode.png
```

---

### Chat Conversation

```
images/chat.png
```

---

# 🚀 Tech Stack

## Backend

- Python
- Google Gemini API
- google-genai SDK
- REST API

---

## Frontend

- HTML5
- CSS3
- JavaScript

---

## Tools

- Git
- GitHub
- VS Code

---

# 📁 Project Structure

```
gemini-chatbot/
│
├── server.py
├── server_function_calling.py
├── index.html
├── requirements.txt
├── .env.example
├── README.md
└── LICENSE
```

---

# 🎯 Project Objectives

This project was developed to:

- Learn Google Gemini API integration
- Understand REST API development
- Build AI-powered web applications
- Improve frontend user experience
- Practice Git and GitHub workflows
- Serve as a reusable chatbot backend for future applications

---

# ⭐ Key Highlights

- Beginner-friendly codebase
- RESTful architecture
- Easy to integrate with any frontend
- Responsive UI
- Improved user experience
- Production-ready project structure
- Open-source and customizable

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone https://github.com/Pushpa2-ai/gemini-chatbot.git
```

Move into the project directory.

```bash
cd gemini-chatbot
```

---

## 2. Create a Virtual Environment (Recommended)

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

The project uses the official **Google GenAI SDK** for communicating with Gemini models.

---

# 🔑 Environment Variables

Create a `.env` file in the root directory.

Example:

```env
SERVER_PORT=8000
GEMINI_API_KEY=YOUR_GEMINI_API_KEY
```

If you don't have a Gemini API key, simply leave it blank.

```env
GEMINI_API_KEY=
```

The application will automatically switch to mock responses for testing.

---

# ▶️ Running the Project

Start the chatbot server:

```bash
python server.py
```

For the Function Calling version:

```bash
python server_function_calling.py
```

Once the server starts successfully, open your browser:

```
http://localhost:8000
```

You can now start chatting with Gemini.

---

# 📡 REST API Endpoints

## Send Message

**POST**

```
/chat
```

Example Request

```json
{
    "text":"Hello Gemini!"
}
```

---

## Get Conversation History

**GET**

```
/messages
```

Returns the complete conversation.

---

## Reset Conversation

**DELETE**

```
/messages
```

Deletes all stored messages.

---

# 💻 API Testing

Using **cURL**

### Send a Message

```bash
curl -X POST ^
-H "Content-Type: application/json" ^
-d "{\"text\":\"Hello\"}" ^
http://localhost:8000/chat
```

---

### Fetch Messages

```bash
curl http://localhost:8000/messages
```

---

### Clear Chat

```bash
curl -X DELETE http://localhost:8000/messages
```

---

# 🌐 Access from Other Devices

To access the chatbot from another device connected to the same network:

Replace

```
http://localhost:8000
```

with

```
http://YOUR_LOCAL_IP:8000
```

Example

```
http://192.168.1.100:8000
```

On Windows, find your IP address:

```bash
ipconfig
```

On Linux/macOS:

```bash
ifconfig
```

or

```bash
ip addr
```

---

# 📂 Folder Structure

```
gemini-chatbot
│
├── server.py
├── server_function_calling.py
├── index.html
├── requirements.txt
├── .env.example
├── .env
├── README.md
└── LICENSE
```

---

# 🧠 How It Works

1. User enters a prompt.
2. The frontend sends the request to the Python REST API.
3. The server communicates with Google Gemini.
4. Gemini generates a response.
5. The response is returned to the frontend.
6. The chat history is updated and displayed instantly.

```
User
   │
   ▼
Frontend (HTML + JavaScript)
   │
   ▼
Python REST API
   │
   ▼
Google Gemini API
   │
   ▼
Frontend UI
```

---

# 🌟 UI & User Experience Enhancements

This version extends the original project with several usability and interface improvements to provide a cleaner and more user-friendly chatting experience.

## 🌙 Dark Mode

A built-in dark theme allows users to switch between light and dark modes for a more comfortable viewing experience.

**Benefits**

- Better readability in low-light environments
- Improved modern UI appearance
- One-click theme switching

---

## 📋 Copy AI Response

Each AI response includes a **Copy** button.

Users can instantly copy the generated response to the clipboard without manually selecting the text.

---

## 💬 ChatGPT-style Chat Interface

The chat interface has been redesigned with modern chat bubbles.

### User Messages

- Right aligned
- Blue background
- White text

### AI Messages

- Left aligned
- Light background
- Easy to distinguish from user messages

---

## ⏳ Thinking Status

Instead of waiting silently, users now see

```
🤖 Gemini is thinking...
```

This provides immediate feedback after sending a prompt and improves the overall user experience.

---

## 📥 Download Chat History

Users can download the complete conversation as a plain text file.

Useful for:

- Saving conversations
- Documentation
- Sharing responses
- Future reference

---

## 🕒 Message Timestamps

Every chat message displays its timestamp, making conversations easier to follow.

---

## 📜 Auto-scroll Optimization

Whenever a new message is received, the chat automatically scrolls to the latest message.

This creates a smoother messaging experience similar to modern chat applications.

---

# ⚙️ Gemini Configuration

The chatbot uses Google's **Gemini 2.5 Flash** model for fast and efficient text generation.

Current configuration includes:

| Setting | Value |
|---------|-------|
| Model | Gemini 2.5 Flash |
| Temperature | 0.5 |
| Thinking Budget | 0 |
| Response Type | Text Generation |

The temperature is configured to balance creativity and response consistency.

---

# 🔄 Function Calling Support

The project also includes a separate server implementation demonstrating **Gemini Function Calling**.

Run it using:

```bash
python server_function_calling.py
```

This implementation serves as a learning example for developers who want to understand how Gemini can invoke external functions and APIs.

---

# ⚡ Performance

- Lightweight Python backend
- Fast Gemini responses
- Minimal frontend
- Low memory usage
- RESTful architecture
- Easy deployment

---

# 🛠 Customization

You can easily customize the chatbot by modifying:

### System Prompt

Change the chatbot personality.

Examples:

- Personal Assistant
- Coding Assistant
- Travel Guide
- Medical Assistant
- AI Tutor
- Customer Support Bot

---

### Gemini Model

You can switch to other supported Gemini models by changing the model name inside the server configuration.

---

### Frontend

The UI can easily be extended with:

- React
- Vue
- Angular
- Flutter
- React Native

without changing the backend API.

---

# 🚀 Future Improvements

Potential enhancements include:

- Markdown rendering
- Syntax highlighting for code blocks
- Voice input
- Text-to-speech
- Chat search
- Export as PDF
- Database integration
- User authentication
- Persistent chat history
- Docker support
- Cloud deployment
- Multi-user support

---

# 🐞 Troubleshooting

## Server does not start

- Verify Python is installed.
- Ensure dependencies are installed.

```bash
pip install -r requirements.txt
```

---

## Gemini is not responding

- Check your API key inside the `.env` file.
- Restart the server after updating the key.

---

## Port already in use

Change the port inside `.env`.

Example

```env
SERVER_PORT=8001
```

---

## Web page not loading

Ensure:

- `server.py` is running.
- `index.html` exists in the project directory.
- Browser is opened at:

```
http://localhost:8000
```

---

# 📚 Learning Outcomes

This project helped strengthen understanding of:

- Python programming
- REST API development
- Google Gemini API integration
- HTTP request handling
- Frontend and backend communication
- Environment variable management
- Git and GitHub workflow
- Modern UI enhancement techniques
- JavaScript DOM manipulation
- Open-source project customization

---

# 🤝 Contributing

Contributions are welcome!

If you have ideas for improving this project, feel free to:

1. Fork the repository
2. Create a new feature branch

```bash
git checkout -b feature/your-feature-name
```

3. Commit your changes

```bash
git commit -m "Add your feature"
```

4. Push the branch

```bash
git push origin feature/your-feature-name
```

5. Open a Pull Request

Please ensure your code follows clean coding practices and is properly tested before submitting.

---

# 📜 License

This project is distributed under the **MIT License**.

You are free to:

- Use
- Modify
- Share
- Learn from

this project under the terms of the MIT License.

See the **LICENSE** file for more information.

---

# 🙏 Acknowledgements

This project is based on the open-source project:

**python-chatbot-server** by **supershaneski**

The original project provided a lightweight REST API example for integrating Google's Gemini API.

This repository extends the original implementation by introducing several UI improvements, enhanced usability, and a more polished user experience while preserving its educational purpose.

Special thanks to the original author for making the project available to the open-source community.

---

# 👨‍💻 Author

**Pushpa Kumari**

### GitHub

https://github.com/Pushpa2-ai

### LinkedIn

https://www.linkedin.com/in/pushpa-kumari-803226259/

---

# ⭐ If you like this project

Please consider giving this repository a ⭐ on GitHub.

It helps others discover the project and motivates future improvements.

---

# 📬 Contact

If you have any questions, suggestions, or feedback, feel free to connect with me through GitHub or LinkedIn.

I am always open to learning, collaboration, and discussing software development.

---

# 🚀 Roadmap

Planned future improvements include:

- Markdown rendering
- Code syntax highlighting
- Voice input (Speech-to-Text)
- Text-to-Speech
- Chat export as PDF
- Persistent database storage
- User authentication
- Multi-user chat sessions
- Docker deployment
- Cloud deployment (Render/AWS)
- Streaming AI responses
- Mobile-responsive interface improvements

---

# 📊 Project Summary

| Category | Details |
|----------|----------|
| Backend | Python |
| AI Model | Google Gemini 2.5 Flash |
| API Type | REST API |
| Frontend | HTML, CSS, JavaScript |
| Communication | HTTP |
| Environment Variables | .env |
| Version Control | Git & GitHub |

---

# 🌟 Why This Project?

This project demonstrates practical skills in:

- REST API development
- AI integration using Google Gemini
- Frontend and backend communication
- JavaScript DOM manipulation
- User interface enhancement
- Environment variable management
- Git version control
- Open-source collaboration
- API testing
- Clean project organization

It serves as a beginner-friendly yet extensible foundation for developers who want to explore AI-powered chatbot applications.

---

## Thank You ❤️

Thank you for visiting this repository.

If you found this project useful, consider giving it a ⭐ and sharing it with others.

Happy Coding! 🚀