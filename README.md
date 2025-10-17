🧠 Unstructured Data Analysis Dashboard

A comprehensive, multi-modal Streamlit application designed for processing and analyzing various forms of unstructured data, including Images, Audio, and Text.

✨ Features

This dashboard is divided into three main tabs, utilizing powerful Python libraries for real-time analysis:

🖼️ Image Analysis (DeepFace & Rembg)

Face Detection: Detects and crops faces from uploaded images.

Facial Attribute Analysis: Predicts Age, Gender, and Dominant Emotion.

Background Removal: Removes the background from the image using rembg.

🎧 Audio Analysis (gTTS & SpeechRecognition)

Text-to-Speech (TTS): Converts typed text into an audible MP3 file for download or playback.

Speech-to-Text (STT): Transcribes uploaded audio files (.wav, .mp3, .m4a) into text.

📝 Text Analysis (TextBlob, WordCloud & spaCy)

Part-of-Speech (POS) Tagging: Identifies nouns, verbs, adjectives, and adverbs.

WordClouds: Generates visualizations of word frequency based on POS categories.

Named Entity Recognition (NER): Uses spaCy to identify and visualize named entities (people, locations, organizations, etc.) within the text.

🛠️ Installation and Setup

1. Prerequisites

Before installing the Python dependencies, you must install the FFmpeg multimedia framework on your operating system.

Operating System

Installation Command (Examples)

Reason

Linux (Ubuntu/Debian)

sudo apt update && sudo apt install ffmpeg

Required by pydub for audio processing.

macOS

brew install ffmpeg (using Homebrew)

Required by pydub for audio processing.

Windows

Download from ffmpeg.org and add the /bin directory to your System PATH.

Required by pydub for audio processing.

2. Python Environment Setup

It is highly recommended to use a virtual environment.

# Clone the repository (if applicable)
# git clone <repository-url>
# cd unstructured-data-analysis

# Create a virtual environment
python -m venv venv
source venv/bin/activate # On Windows use: venv\Scripts\activate

# Save your dependencies to a requirements.txt (optional but recommended)
# e.g., pip freeze > requirements.txt

# Install the required Python packages
pip install streamlit gtts speechrecognition pydub rembg deepface numpy Pillow textblob wordcloud matplotlib spacy


3. spaCy Model Download

The text analysis tab requires the small English spaCy model to be explicitly downloaded.

python -m spacy download en_core_web_sm


🚀 Usage

Ensure you have completed all setup steps above.

Save the provided Python code as speech.py.

Run the application using Streamlit:

streamlit run speech.py


The application will open in your web browser (usually at http://localhost:8501).

Navigate between the three tabs to test the different unstructured data analysis capabilities.
