# 🎶 Audio Extractor and Separator for Karaoke and Personal Use

A Python-based tool to extract and process audio from videos or music files, powered by **Spleeter** for advanced vocal and instrumental separation. Ideal for creating karaoke tracks or isolating individual stems for personal use. The tool supports YouTube, direct URLs, and local files, with a user-friendly GUI or direct Python scripting.

---

## ✨ Features

1. **Input Options**:
   - Process audio from:
     - **YouTube URLs**
     - **Direct audio URLs**
     - **Uploaded local files** (video: `.mp4`, `.mov`, audio: `.wav`, `.mp3`, `.aif`, `.aiff`).
   - Choose one input method per session.

2. **Flexible Separation**:
   - **2 stems** (default): Vocals + Accompaniment.
   - **5 stems** (optional): Vocals, Drums, Bass, Piano, and Other.

3. **Output Formats**:
   - Default: High-quality **WAV**.
   - Optional: Compact **MP3** (44100 Hz, 192 kbps).

4. **Bundled ZIP Downloads**:
   - Processed files are automatically packaged into a ZIP for easy downloading.

5. **Run Anywhere**:
   - Use in **Google Colab** with a GUI.
   - Integrate into your own Python projects — only a CPU is required, no GPU needed.

---

## 🛠️ How to Use

### **1. Using in Google Colab**
1. Open the Colab notebook from here or via link [Colab Public file](https://colab.research.google.com/drive/1nvtp_UJF2QqtGamPlJHJx9aUSgyOtGMs?usp=sharing)
2. Run the setup cells to install required dependencies.
3. Choose your input method:
   - **Use URL**: Enter a YouTube or direct audio URL.
   - **Upload File**: Select a local file via the upload widget.
4. Select processing options:
   - **Stems**: Default (2 stems) or advanced (5 stems).
   - **Download as MP3**: Check this option for MP3 outputs.
5. Click the **Process** button to extract, separate, and download the processed ZIP.

### **2. Using in Your Own Python Program**
- Clone the repository and integrate the provided Python code.
- Modify the functions as needed for batch processing or custom workflows.
- Example entry points:
  - `download_and_extract_audio()`
  - `separate_audio()`
  - `convert_to_mp3()`

> **Note**: This project only requires a CPU for all operations. No GPU is needed.

---

## 🧠 How It Works

**Spleeter** uses deep learning to separate audio into stems:

- **Model Architecture**: A convolutional neural network (CNN) trained on a large dataset of music tracks.
- **Spectrogram-Based Processing**:
  - Audio is converted into a spectrogram (a visual representation of frequency over time).
  - The model predicts which parts of the spectrogram belong to each stem.
  - Stems are reconstructed into separate audio files.

For more details, visit the [Spleeter GitHub page](https://github.com/deezer/spleeter).

---

## ⚖️ Legal Disclaimer

- This project is intended for **personal use only**.
- Ensure compliance with copyright laws and terms of service when processing media.
- Do not distribute or share processed files from copyrighted materials without proper permissions.
- Users are responsible for any legal issues arising from misuse of this tool.

---

## 📦 Dependencies

This project relies on the following tools and libraries:
1. **[yt-dlp](https://github.com/yt-dlp/yt-dlp)** (MIT License): For downloading videos or audio from YouTube.
2. **[Spleeter](https://github.com/deezer/spleeter)** (MIT License): For audio separation.
3. **[FFmpeg](https://ffmpeg.org/)** (GPL or LGPL License): For audio and video processing. Users must install FFmpeg separately.
4. **Python Standard Libraries**: `os`, `shutil`, `zipfile`, `subprocess`, and others.

> **Note**: The repository does not bundle FFmpeg binaries. Users are responsible for ensuring FFmpeg is installed and complies with its license.

---

## 🛡️ License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for more details.

> The use of third-party tools like FFmpeg is subject to their respective licenses. Ensure compliance when using or distributing your project.

---

## 📧 Contact

If you have questions or suggestions, feel free to reach out:
- **Email**: riccardo.solimena@gmail.com
- **GitHub Issues**: [Submit an issue](https://github.com/solimena/audio-extractor-separator/issues)
