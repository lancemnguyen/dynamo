# Gemini Dynamo

## Overview
The DynamoCards project integrates frontend and backend technologies to efficiently parse and organize lengthy YouTube transcripts, revolutionizing study processes and enhancing digital learning experiences. By leveraging advanced AI and semantic extraction algorithms, the tool helps students and educators distill hours of lecture material into concise, digestible insights.

## Features
- **Youtube Transcript Retrieval & Summarization**: Streamlines the parsing of lengthy YouTube transcripts and converts it into concise summaries to identify and organize key concepts and terms.
- **Frontend-Backend Integration**: Seamless communication between frontend and backend to handle video analysis and display results.
- **User-Friendly Interface**: Manage and interact with parsed data through an intuitive React-based frontend.
- **Flashcard Management**: Generate and handle flashcards for key concepts, enhancing study habits and information retention.

## Tech Stack
- **Google Cloud**: Used for setting up and managing the cloud environment for the project.
- **FastAPI**: Backend framework to handle video analysis and API endpoints.
- **Langchain**: Utilized for retrieving video transcripts and integrating generative AI functionalities.
- **Vertex AI**: Employed in generating document summaries and extracting key concepts.
- **React**: Frontend framework to create a user-friendly interface for managing parsed data and flashcards.

## Installation
Prerequisites
- Python 3.7 or higher
- Node.js and npm (for React frontend)
- Google Cloud account with Vertex AI enabled

Setup Instructions
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
Select React and JavaScript
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
