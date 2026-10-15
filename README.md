# VaultMind ERP

VaultMind ERP is a Google Colab-hosted Streamlit application for faculty and administration. It combines department-aware assistance with document search, voice input, and persistent conversation records.

## Features

- Department-aware assistant for faculty and administration.
- Document processing and search using ChromaDB and sentence-transformer embeddings.
- Voice transcription and translation using Whisper (Hindi and English are supported).
- Conversation history and application data stored in Google Drive.
- Audit and conversation records stored in SQLite databases.
- Streamlit interface exposed through the Google Colab port proxy.

## Project file

- `final_project (1).ipynb` — notebook containing the application setup and launch code. It includes earlier iterations as well as the v10 memory-and-voice version.

## Run in Google Colab

1. Upload `final_project (1).ipynb` to Google Colab and open it.
2. Select a GPU runtime if available. Model downloads and first startup can take several minutes.
3. Run the cell titled **“VAULTMIND ERP v10 — MEMORY + VOICE”**. It mounts Google Drive, installs the required packages and `ffmpeg`, writes the Streamlit app, and starts the server.
4. Open the application using the URL printed at the end of the cell. Keep the Colab runtime running while using the app.

The app stores its files under `MyDrive/vaultmind`, including its data, uploads, logs, and a copy of the generated application script.

## Dependencies

The v10 setup cell installs the Python dependencies in Colab, including Streamlit, ChromaDB, sentence-transformers, Transformers, PyMuPDF, pandas, Plotly, and audio-processing packages. No separate local installation is needed for the documented Colab workflow.

## Important notes

- The v10 startup cell deletes `MyDrive/vaultmind/data/users.json` before launching and initializes the users again. Back up that file before rerunning the cell if you have user changes you need to preserve.
- Treat the generated application URL and any demo credentials as private. Do not expose real personal or confidential documents in a public or shared runtime.
- This notebook is designed for Google Colab and Google Drive; it is not a standalone local deployment guide.
