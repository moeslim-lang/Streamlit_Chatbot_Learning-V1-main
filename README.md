# Streamlit Chatbot Learning - V1
![WhatsApp Image 2025-10-06 at 08 59 48](https://github.com/user-attachments/assets/1fec3e72-dd53-4fb6-8015-65ef9cfd828d)

[More - Streamlit User Interface](https://drive.google.com/file/d/1yoltcfXPI1i2_mMaXePF3bspyEgboJZn/view)

**StudyBuddy AI** is an interactive chatbot app built with Streamlit and Google Gemini, designed as your virtual study buddy. It helps students dive into lesson materials through casual Q&A sessions, adaptive quizzes, and quick reviews of those tricky concepts. Just upload your study files (PDF, TXT, MD) or drop in a topic, and start exploring in a fun, effective way.

### **Key Features**
- **Learning Mode (Chat)**: Jump into free-flowing Q&A about your materials, backed by file context for spot-on answers.
- **Quiz Mode**: Generate automatic multiple-choice quizzes with adjustable difficulty levels (easy, medium, hard). Track your accuracy progress and answer history.
- **Review Mode**: Summarize tough concepts based on your past mistakes, complete with tips and quick practice drills.
- **File Upload**: Seamless integration with Google Gemini File API to analyze PDFs, TXT files, or Markdown as your learning context.
- **Progress Tracking**: Metrics on attempts, accuracy, and a summary of your last 5 answers.
- **Indonesian Language Support**: All interactions are friendly and adaptive in Bahasa Indonesia.
- **Reset & Settings**: Easily wipe your data and tweak modes or difficulty levels on the fly.

### **System Requirements**
- Python 3.8+
- Streamlit 1.36.0 or higher
- Access to Google AI Studio (for your Gemini API Key)

### **Installation**
1. Clone the Repository:
```text
git clone https://github.com/andhiksu/studybuddy-ai.git
cd studybuddy-ai
```
2. Create a Virtual Environment (recommended):
```text
python -m venv venv
source venv/bin/activate  # Linux/Mac
# atau
venv\Scripts\activate  # Windows
```
3. Install Dependencies:
```text
pip install -r requirements.txt
```
The `requirements.txt` file includes:
- `streamlit>=1.36.0`
- `google-genai>=1.0.0`
- `pypdf>=5.0.0`
4. Get Your API Key:
  - Head over to [Google AI Studio](https://aistudio.google.com/app/api-keys) to grab your API Key.
  - Create a new one and keep it safe.
 
### **Running the App**
1. Launch the Application:
```text
streamlit run streamlit_chatbot_learning.py
```
2. Open in Your Browser: Navigate to `http://localhost:8501`.
3. In the Sidebar:
   - Enter your Gemini API Key and hit "Set API Key".
   - Upload a study file or type in a topic (e.g., "Quantum Physics").
   - Pick a mode (Learning, Quiz, Review) and difficulty level.
   - Click "Explore Topic" to get started.

The app will automatically load prompts from `prompts_chatbot_learning.txt` for system instructions and quiz generation.

### **Usage**
- API Key: Required to tap into Gemini—don't skip this!
- File Upload: Supports PDF/TXT/MD; files get uploaded to the Gemini File API for context.
- Manual Topic: No file? Just describe the topic for on-the-fly exploration.
- Modes & Levels: Choose your vibe—Learning for chats, Quiz for tests, Review for recaps.
- Reset: Clear everything and start fresh whenever you want.

### **Project Structure**
```text
studybuddy-ai/
├── streamlit_chatbot_learning.py  # Main Streamlit app
├── prompts_chatbot_learning.txt   # Prompt templates for system, quizzes, and reviews
├── requirements.txt               # Python dependencies
└── README.md                      # This doc
```
- `streamlit_chatbot_learning.py`: Core logic, including file uploads, response generation, and UI rendering.
- `prompts_chatbot_learning.txt`: Gemini prompt configs (system roles, JSON quiz instructions, review tips).

### **Troubleshooting**
- API Key Errors: Make sure `google-genai>=1.0.0` is installed; restart the app after updates.
- Upload Failures: Check your file's MIME type; the app auto-detects PDF/TXT/MD.
- Broken Quiz JSON: Gemini models can be quirky with outputs— the app tries to parse it automatically.
- No Internet?: The app needs a stable connection to the Gemini API, so double-check your setup.
