# Professor AI Feynman: A Multi-Agent Tool for Learning Anything the Feynman way | A Microsoft's AI Agent Hackathon Submission - Jaward Sesay

### Project Description
Professor AI Feynman is a nascent multi-agent application designed to generate and teach personalized educational lecture materials using a multi-agent framework (Microsoft's Autogen). As a big fan of Professor Richard Feynman and his exceptional teaching methods, I was inspired to build his persona into a network of agents equipped with tools to deliver lectures in his engaging and delightful style. The project aims to simplify complex topics into compelling presentations for diverse audiences (e.g., conferences, universities, high schools). Leveraging advanced LLMs for text content generation and Coqui's TTS model (XTTS_v2) for speech generation along with search (via serpapi), it automates the creation and delivery of multimedia lectures, making it ideal for personalized learning.

### Features
- **Multi-Agent Collaboration**: Utilizes Autogen's Swarm to coordinate research, design and generate slides, scripting, review and delivery of lectures in an engaging and insightful manner.
- **Deep Research**: Has support for web search on given lecture topics, this accounts for higher accuracy in lecture content.
- **Autonomous Slide Generation**: Creates HTML custom slides with titles, content, and metadata based on user-provided topics and audience types.
- **Narration Script Generation**: Generates concise, academic scripts for each slide using a multi-agent workflow.
- **Script Speech Generation (audio for each slide)**: Produces high-quality speech narration using customizable speaker voices (MP3/WAV input).
- **Seamless Lecture Delivery**: Offers a web-based interface with simultaneous lecture flow of speech and slides. The UI has navigation (prev/next), play/pause controls, and dynamic font sizing for slides.
- **Downloadable Lecture Materials**: Exports slides, scripts, and audio as a zip file for offline use.

### Architecture
The application follows a modular, agent-based architecture:
- **Research Agent**: Does thorough research on the given topic using SerpApi for search.
- **Slide Agent**: Generates structured slide content in JSON format and converts it to HTML for easy rendering.
- **Script Agent**: Produces narration scripts for each slide aligned with overall lecture contents.
- **Feynman Agent**: Reviews and validates completed tasks by all other agents, then delivers the lecture.
- The UI is built with Gradio, providing a simple, user-friendly interface with real-time progress updates and file downloads. The design emphasizes responsiveness, ensuring compatibility across devices with dynamic font adjustments.

<img width="1115" alt="Image" src="https://github.com/user-attachments/assets/e120128f-41e0-4657-990d-699b26c58c1c" />

### Demo Video: https://drive.google.com/file/d/1mCsjyU-RjPDaeMk0bw37_D53ZwSL0-Cm/view?usp=sharing
### Try Demo on huggingface: https://huggingface.co/spaces/Jaward/Professor-AI-Feynman
<img width="1075" alt="Image" src="https://github.com/user-attachments/assets/2409ca02-43d4-4288-815a-6b442925f4bd" />

## Installation
1. Clone the repository: `git clone https://github.com/Jaykef/professor-ai-feynman.git`
2. Navigate to the project directory: `cd professor-ai-feynman`
3. Install dependencies: `pip install -r requirements.txt`
4. Set environment variables (e.g., API keys for OpenAI, Anthropic, SerpApi) in a `.env` file or system environment.
5. Run the application: `python app.py`
6. Ensure Coqui TTS model (XTTS_v2) is downloaded- this automatically happens once when you run the app: Follow Coqui TTS inference [instructions](https://github.com/coqui-ai/TTS).

## Usage
1. Open app in browser at: http://127.0.0.1:7860
2. Input lecture details: title, content description, audience type, prefered lecture style, number of slides, and sample speaker audio.
3. Select an AI model (e.g., OpenAI, Anthropic) and provide API keys if required.
4. Click "Generate Lecture" to initiate the multi-agent process.
5. Monitor progress and interact with the generated slides, audio, and download options once complete.

## Tech Stack
- **Languages**: Python
- **Frameworks/Libraries**: Microsoft Autogen (Swarm), TTS (Coqui), Pytorch
- **AI Models**: OpenAI GPT-4o, Anthropic Claude, Google Gemini, Ollama Llama, Azure AI Foundry
- **Tools**: SerpApi (web search), Azure AI services
- **Frontend**: Gradio, JavaScript
- **Hosting**: HF Space https://huggingface.co/spaces/Jaward/Professor-AI-Feynman

## Project Structure
```
professor-ai-feynman/
├── outputs/              # Generated slides, scripts, and audio files
├── slide_template.html   # HTML template for slides
├── app.py               # Main application script
├── requirements.txt      # Python dependencies
├── README.md            # Project documentation
└── feynman.mp3          # Default speaker audio (optional)
```
There is still room for improvements which I will continue to work on and I'm open to ideas as this might just be my first startup:)

## License
This project is licensed under the MIT License.
