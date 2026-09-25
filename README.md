# Moodify

An AI-powered mobile application that provides personalized music recommendations based on the user's current mood.

## Features

* **Mood Analysis:** A smart recommendation engine that analyzes the user's mood through Google Gemini API integration.
* **Dynamic Music Recommendations:** Delivers the most suitable songs and playlists for the user's emotional state using the Spotify Web API.
* **Cross-Platform:** A modern, fluid, and user-friendly mobile interface designed to work seamlessly across devices.
* **High-Performance Architecture:** An optimized server infrastructure built for asynchronous data processing and fast response times.

## Tech Stack

* **Frontend:** Flutter, Dart
* **Backend:** Python, FastAPI
* **Artificial Intelligence:** Google Gemini API
* **External Services:** Spotify Web API

## Installation

### Prerequisites

* Flutter SDK (version 3.x)
* Python 3.9 or higher
* `Client ID` and `Client Secret` from the Spotify Developer Dashboard
* `Gemini API Key` from Google AI Studio

### Backend Setup (FastAPI)

1. Clone the repository and navigate to the backend directory:
   ```bash
   git clone https://github.com/yourusername/moodify.git
   cd moodify/backend
   ```
2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # For Windows: venv\Scripts\activate
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Create a `.env` file in the root directory and add your API keys:
   ```env
   GEMINI_API_KEY=your_gemini_api_key_here
   SPOTIFY_CLIENT_ID=your_spotify_client_id_here
   SPOTIFY_CLIENT_SECRET=your_spotify_client_secret_here
   ```
5. Start the development server:
   ```bash
   uvicorn main:app --reload
   ```

### Frontend Setup (Flutter)

1. Open a new terminal window and navigate to the frontend directory:
   ```bash
   cd ../frontend
   ```
2. Install the necessary dependencies:
   ```bash
   flutter pub get
   ```
3. Run the application on a connected emulator or physical device:
   ```bash
   flutter run
   ```

## API Endpoints

* `GET /`: Health check endpoint to verify the API is running.
* `POST /analyze-mood`: Processes user text or parameters with the Gemini API to determine their mood.
* `GET /recommendations`: Fetches a list of songs from Spotify based on the determined mood and returns it to the mobile client.

## Contributing

If you would like to contribute to the project, please create a new branch and submit your changes as a Pull Request. For major architectural changes, please open an `Issue` first to discuss your ideas.
