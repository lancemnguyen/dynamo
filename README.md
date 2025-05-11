# Gemini Dynamo

Gemini Dynamo generates flashcards from YouTube transcripts, revolutionizing study processes and enhancing digital learning experiences. By leveraging advanced AI and semantic extraction algorithms, the tool helps students and educators distill hours of lecture material into concise, digestible insights.

Tech stack: GCP (Vertex AI), FastAPI, Langchain, React

## Features
- **Youtube Transcript Retrieval & Summarization**: Parses YouTube transcripts and converts them into concise summaries to identify key concepts.
- **Flashcard Management**: Generates flashcards for key concepts
- **Frontend-Backend Integration**: Frontend displays flashcards and backend handles video analysis.

## Prerequisites
- Python 3.7 or higher
- Node.js and npm (for React frontend)
- Google Cloud account with Vertex AI enabled

## Setup
1. Clone the Repository
```bash
git clone https://github.com/lancegosu/dynamo.git
cd dynamo
```

2. Set Up Google Cloud and Vertex AI
- Create a Google Cloud account and project.
- Enable Vertex AI APIs.
- Create a service account and download the key JSON file.
- Set the GOOGLE_APPLICATION_CREDENTIALS environment variable to the path of the key JSON file.
```bash
export GOOGLE_APPLICATION_CREDENTIALS="path/to/your/service-account-file.json"
```

3. Set Up Backend Environment

```bash
cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

4. Set Up Frontend Environment
```bash
cd frontend
npm create vite@latest dynamocards
```
- Select React and JavaScript
```bash
cd dynamocards
npm install
npm install axios
```

## Usage
1. Start the Backend Server
```bash
cd backend
source venv/bin/activate
uvicorn main:app --reload
```

2. Start the Frontend Server
```bash
cd dynamocards
npm run dev
```

3. Analyze YouTube Videos
- Open your browser and navigate to the frontend application (typically running at http://localhost:5173/).
- Enter a YouTube video link and submit it for analysis.

4. View Flashcards
- The frontend will display the parsed key concepts and terms along with their definition from the YouTube transcript.

5. Manage Flashcards
- Use the provided functionality to discard any unwanted flashcards.

By following this guide, you should be able to set up and use Gemini Dynamo to parse and organize lengthy YouTube transcripts to create flashcards.

### Acknowledgements
A special thank you to Radical AI for providing the foundation of this project. Their support and resources have been invaluable in developing DynamoCards, ensuring that we can offer a revolutionary tool for enhancing digital learning experiences for students and educators worldwide.
