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

##  How to Run
1. Clone this repo and install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```  

2. Set up your API keys in a `.env` file:  
   ```
   OPENAI_API_KEY=your_key
   GROQ_API_KEY=your_key
   ```  

3. Run the notebook or Gradio app:  
   ```bash
   jupyter notebook Mock_interview_final_changed_to_whisperAI.ipynb
   ```  
   or  
   ```bash
   python app.py
   ```  

4. Start your mock interview by pasting a job link in the UI.  

---

## 📷 Screenshots
- Flow diagram of system components  
- Key architecture (scraping, LangChain, STT/TTS, UI)  
- Evaluation sample with **score breakdown**  

---

## Future Enhancements
- Support for **multilingual interviews**  
- Integration with **ATS-style scoring rubrics**  
- Enhanced analytics dashboard for tracking progress over multiple sessions  
