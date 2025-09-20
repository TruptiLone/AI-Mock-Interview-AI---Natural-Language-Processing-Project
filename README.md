# AI-Powered Mock Behavioral Interview (NLP & LangChain)

## Project Overview
This project implements an **AI-powered mock interview system** that simulates **behavioral interview rounds** tailored to specific job roles.  
It combines **web scraping, NLP, LangChain, and speech processing** to generate dynamic interview questions, capture responses, and provide structured evaluation feedback.  

The system helps candidates **practice behavioral interviews** in a realistic, voice-enabled environment.  

---

## Features
- **Job Role Extraction**: Scrapes career pages using **BeautifulSoup**, summarizes job role with **OpenAI GPT-4o**.  
- **AI Interview Flow**: Powered by **LangChain**, with conversational memory to maintain context.  
- **Dynamic Questioning**: AI interviewer introduces role, asks structured STAR-style behavioral questions, and adapts follow-ups.  
- **Speech Processing**:  
  - **Groq Distil-Whisper** – converts speech to text (fast, cost-optimized).  
  - **Whisper AI** – generates lifelike text-to-speech audio.  
- **Evaluation Engine**: AI evaluates answers on **answer quality, confidence, clarity, depth of knowledge**, and provides feedback.  
- **Interactive UI**: Built with **Gradio** for easy voice-based practice.  

---

## Tech Stack
- **Languages & Libraries**: Python, Pandas, NumPy, BeautifulSoup, LangChain, OpenAI API  
- **AI Models**: GPT-4o (LLM), Groq Distil-Whisper, Whisper AI  
- **Frameworks**: Gradio, FastAPI (optional integration)  
- **Tools**: dotenv, Requests, Soundfile  

---

## Project Structure
- **Web Scraping**: Extracts job details and passes them into GPT for summarization.  
- **LangChain Interview Flow**:  
  - Introduction → Questions → Candidate Responses → Follow-ups.  
- **Speech Layer**: Converts candidate voice to text and AI responses back to speech.  
- **Evaluation**: Scores candidate answers with structured feedback.  
- **UI Layer**: Gradio app for starting interviews, recording answers, and receiving evaluation.  

---

## Workflow
1. Input a **career/job posting URL**.  
2. System scrapes role details → GPT generates **role summary**.  
3. **AI Interviewer** introduces role & starts behavioral interview.  
4. **Candidate answers** via speech input.  
5. System evaluates responses → generates **feedback & report**.  

---

## Example Evaluation Metrics
- **Answer Quality**: Completeness & relevance  
- **Confidence Level**: Tone & certainty  
- **Clarity & Communication**: Articulation of ideas  
- **Depth of Knowledge**: Technical/behavioral substance  
- **Overall Score**: Aggregated candidate performance  

---

## How to Run (Google Colab)

1. Open the project notebook in **Google Colab**.  

2. Install dependencies (already included in the notebook setup):  
   ```python
   !pip install langchain langchain-openai openai langchain_community gradio groq numpy soundfile python-dotenv
   ```  

3. Store your API keys securely in **Colab’s Key Management** section:  
   - Go to **Colab → Tools → Secrets**.  
   - Add the following keys:  
     - `OPENAI_API_KEY`  
     - `GROQ_API_KEY`  

4. Access the keys inside the notebook:  
   ```python
   from google.colab import userdata
   openai.api_key = userdata.get("OPENAI_API_KEY")
   groq_api_key = userdata.get("GROQ_API_KEY")
   ```  

5. Run all cells in the notebook to launch the AI-powered mock interview system.  

6. Use the **Gradio interface** to start a mock interview by pasting a job posting link.  

---

## Screenshots
- Flow diagram of system components
  <img width="1433" height="806" alt="Screenshot 2025-09-19 at 4 34 46 PM" src="https://github.com/user-attachments/assets/111c913a-0888-400b-b66f-27710df9eb28" />

- Key architecture (scraping, LangChain, STT/TTS, UI)
   <img width="1433" height="806" alt="Screenshot 2025-09-19 at 6 31 58 PM" src="https://github.com/user-attachments/assets/49223429-2b4c-41e7-961d-12946b63e64a" />

- Evaluation sample with **score breakdown**
  <img width="1788" height="935" alt="Screenshot 2025-09-19 at 6 42 01 PM" src="https://github.com/user-attachments/assets/1abd80c7-c4f6-466f-b730-ad2f517f3203" />


---

## Future Enhancements
- Support for **multilingual interviews**  
- Integration with **ATS-style scoring rubrics**  
- Enhanced analytics dashboard for tracking progress over multiple sessions  
