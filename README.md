# 🎥 Video-to-Text Transcriber (Python)

Ever needed to pull a specific quote from a long video lecture or meeting recording? This project automates that process by converting video content into searchable text using Python.

It extracts audio, splits long files into manageable chunks, sends them to Google’s Speech Recognition API, and returns structured transcriptions—ready for analysis, search, or export.

---

## ✨ Key Features

* 🔄 **Automated Chunking**
  Splits long videos into 60-second segments to avoid API limitations and improve processing reliability.

* 🔊 **Audio Extraction**
  Converts video files (MP4) into WAV format for compatibility with speech recognition.

* 🌐 **Google Speech Recognition Integration**
  Uses a powerful cloud-based API for accurate transcription.

* 📁 **Smart File Management**
  Automatically creates and manages directories for chunks and processed audio.

* 📊 **Structured Output**
  Stores transcriptions in a Python dictionary (`diz`) for easy export to JSON or text formats.

---

## 🚀 Quick Start

### 📋 Prerequisites

Make sure you have:

* Python **3.7 or higher**
* A stable internet connection (required for API requests)
* A video file named `videorl.mp4` placed in the project directory

---

### ⚙️ Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your-username/Video-to-Text-Transcriber.git
   cd Video-to-Text-Transcriber
   ```

2. **Create a Virtual Environment (Recommended)**

   ```bash
   python -m venv .venv
   ```

   Activate it:

   * Windows (PowerShell):

     ```bash
     .venv\Scripts\Activate.ps1
     ```
   * macOS/Linux:

     ```bash
     source .venv/bin/activate
     ```

3. **Install Dependencies**

   ```bash
   pip install moviepy==1.0.3 SpeechRecognition
   ```

---

## ▶️ Running the Application

With your environment activated, run:

```bash
python project.py
```

The script will:

1. Process the video
2. Split it into chunks
3. Extract audio
4. Transcribe each segment
5. Output results in the terminal

---

## 🧠 How It Works

| Component            | Role                                                    |
| -------------------- | ------------------------------------------------------- |
| `moviepy`            | Handles video processing and audio extraction           |
| `speech_recognition` | Sends audio to Google Speech API for transcription      |
| `os`, `sys`          | File handling, directory management, and error handling |

### Workflow Overview

1. Load video file
2. Split into 60-second chunks
3. Convert chunks to WAV audio
4. Send audio to Google API
5. Store results in a dictionary

---

## 📦 Output Example

```python
{
  "chunk_1": "Welcome to today's lecture on machine learning...",
  "chunk_2": "In this section we will discuss neural networks...",
}
```

You can easily export this to:

* `.json` for structured use
* `.txt` for readability
* Databases for advanced applications

---

## 🛠️ Future Improvements

* 🎛️ Add CLI arguments for custom input/output files
* 📈 Implement progress bars (e.g., using `tqdm`)
* 💾 Export results automatically to `.txt` or `.json`
* 🧹 Improve error handling for failed API calls
* 🗣️ Support multiple languages
* ⚡ Parallel processing for faster transcription

---

## ⚠️ Known Limitations

* Depends on internet connectivity (Google API)
* May struggle with:

  * Heavy accents
  * Background noise
  * Low-quality audio
* API rate limits may apply for very long videos

---

## 🤝 Contributing

Contributions are welcome and encouraged!

1. Fork the repository
2. Create a feature branch (`feature/your-feature-name`)
3. Commit your changes
4. Push to your fork
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 💬 Feedback & Support

If you encounter any issues or have ideas for improvement:

* Open an issue on GitHub
* Suggest enhancements
* Submit a pull request

---

## 🙌 Acknowledgements

* Inspired by the need to make long-form video content searchable
* Built using open-source Python libraries
* Powered by Google Speech Recognition API

---

⭐ If you found this project useful, consider giving it a star!

Happy Transcribing! 🎧
