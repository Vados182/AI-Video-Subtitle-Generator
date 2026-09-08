# 🎬 AI Video Subtitle Generator

> A web application for automatic generation, editing, translation, and hardcoding of video subtitles, powered by OpenAI models (Whisper & GPT-4).

## 🚀 About the Project

The application was created to drastically reduce the time required to produce professional subtitles for video content. It allows users to upload a video, automatically generate an audio transcript, translate it into one of many supported languages, manually edit the text in an interactive editor, and finally download either the `.srt` file or the final video with hardcoded subtitles.

**💡 View the live application: [https://ai-video-subtitle-generator-cjdtjdjrbdusghdisffsnv.streamlit.app/]**

---

## 🛠️ Technologies & Architecture

The project is designed with a strong focus on separating business logic from the user interface (Modular Architecture), making testing and future development easier.

-   **Python (3.11)** - Main development environment.
-   **Streamlit** - Framework for rapid web interface creation.
-   **OpenAI API** - Integration with Whisper (v3) and GPT-4 models.
-   **Pydub** - Library for audio file manipulation.
-   **FFmpeg** - External system tool for advanced conversion and hardcoding subtitles.
-   **Git** - Version control system.

### Project Structure (Separation of Concerns):

In VS Code:
```text
├── .streamlit/config.toml  # Configuration for the 1GB limit in the Streamlit interface.
├── app.py                  # Main file, views, and application state controller (Streamlit).
├── audio_processor.py      # Audio processing logic, validation, and system operations (FFmpeg).
├── openai_service.py       # Service class handling communication with the OpenAI API (Whisper & GPT).
├── requirements.txt        # List of Python dependencies.
├── .gitignore              # List of files ignored by Git (e.g., caches, __pycache__).
├── movie.jpg               # Interface background image.
└── translate.png           # Sidebar image.