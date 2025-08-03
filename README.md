# Personal Fitness Tool

A fitness application that combines the power of Vector Databases (Astra DB) with AI capabilities using Langflow and Datastax, featuring RAG for contextual workout recommendations.
As i've been working on spring boot but as this era I had knowledge of python , So learned new things like Langflow,Streamlit,Vector DB,RAG,etc.


## Features

- Personal fitness data management
- AI-powered workout recommendations using RAG
- Contextual note-taking with RAG integration
  - Example: Notes about gym equipment limitations are considered when generating workouts
  - If you note "no leg press machine available", the AI will adapt workout plans accordingly
- Profile management
- Real-time macros calculation

## Tech Stack

- **Frontend**: Streamlit
- **Database**: Astra DB (Vector Database by DataStax)
- **AI Integration**: 
  - Langflow
  - RAG (Retrieval Augmented Generation)
- **Python Libraries**:
  - streamlit
  - astrapy
  - langflow
  - python-dotenv
  - requests

## Environment Setup

Create a `.env` file with:
```
ASTRA_DB_APPLICATION_TOKEN=your_token_here
ASTRA_ENDPOINT=your_endpoint_here
LANGFLOW_TOKEN=your_langflow_token_here
```

## Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/WorkoutApp.git
```

2. Install dependencies
```bash
pip install streamlit astrapy langflow python-dotenv requests
```

3. Run the application
```bash
streamlit run main.py
```

## Vector Database: Astra DB

This project uses Astra DB, a vector database service by DataStax, to store and manage:
- User profiles
- Workout data
- Personal notes
- Vector embeddings for AI recommendations

## Langflow Integration

Langflow is used for:
- Generating personalized workout plans
- Analyzing user data
- Providing fitness recommendations
- Processing natural language queries

## RAG Implementation

The application uses Retrieval Augmented Generation to:
- Store user notes as vectors in Astra DB
- Retrieve relevant context when generating workout plans
- Adapt recommendations based on:
  - Available equipment
  - User preferences
  - Gym limitations
  - Previous workout history

Example:
```
User Note: "My gym doesn't have a leg press machine"
AI Query: "Create a leg day workout routine"
Result: AI generates a routine without leg press, substituting with alternative exercises
```

## Project Structure

```
WorkoutApp/
├── main.py          # Main Streamlit application
├── ai.py            # AI and Langflow integration
├── db.py            # Database operations
├── profiles.py      # User profile management
├── form_submit.py   # Form handling
├── .env             # Environment variables
└── README.md        # Documentation
```

## Contributing

Feel free to open issues and pull requests!

## License

MIT License
