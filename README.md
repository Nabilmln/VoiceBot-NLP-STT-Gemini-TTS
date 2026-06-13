# 🎤 Suara Cerdas — Voice Chatbot UAS (STT + Gemini LLM + TTS)

> 📚 **Proyek Ujian Akhir Semester (UAS)** — Mata Kuliah **Pemrosesan Bahasa Alami (NLP)**, Semester Genap Tahun Ajaran 2024/2025

Proyek ini adalah implementasi chatbot berbasis suara yang memungkinkan interaksi dua arah secara alami melalui web. Sistem menangkap ucapan pengguna, mengubahnya menjadi teks, merespons menggunakan model bahasa besar dari Google (Gemini API), lalu membacakan kembali respons menggunakan teknologi Text-to-Speech.

## 🌟 Fitur Unggulan

* **Pengenalan Suara (STT)** — Menggunakan `whisper.cpp` dari OpenAI untuk mentranskripsikan ucapan ke teks secara akurat.
* **Pemrosesan Bahasa (LLM)** — Terintegrasi dengan Google Gemini API untuk menghasilkan respons cerdas dalam Bahasa Indonesia.
* **Konversi Teks ke Suara (TTS)** — Menggunakan model TTS dari Coqui, dilengkapi dukungan suara Bahasa Indonesia.
* **Antarmuka Web Interaktif** — Dibangun dengan `Gradio`, memudahkan pengujian langsung di browser tanpa setup kompleks.

## 🏗️ Struktur Folder

- **voice_chatbot_project/**
  - **app/**
    - `main.py` — Endpoint utama FastAPI
    - `llm.py` — Integrasi Gemini API
    - `stt.py` — Transkripsi suara (whisper.cpp)
    - `tts.py` — TTS dengan Coqui
    - `whisper.cpp/` — Hasil clone whisper.cpp
    - `coqui_utils/` — Model dan config Coqui TTS
  - **gradio_app/**
    - `app.py` — Frontend dengan Gradio
  - `.env` — Menyimpan Gemini API Key
  - `requirements.txt` — Daftar dependensi Python
 
## ⚙️ Teknologi dan Rekomendasi

* Seluruh file audio menggunakan format `.wav`
* Model Whisper yang direkomendasikan: `ggml-large-v3-turbo`
* Speaker yang digunakan: `wibowo` dari model Coqui TTS v1.2
* Output dari Gemini dikonversi ke bentuk fonetik sebelum dibacakan oleh TTS
  * Contoh konversi: `dengan` → `dəˈnɡan`

## 🚀 Cara Menjalankan

```bash
# 1. Clone repository
git clone https://github.com/USERNAME/voicebot-nlp-stt-gemini-tts.git
cd voicebot-nlp-stt-gemini-tts

# 2. Install dependencies
pip install -r requirements.txt

# 3. Tambahkan API key Gemini ke file .env
GEMINI_API_KEY=your_api_key_here

# 4. Jalankan aplikasi
python gradio_app/app.py
```

## 🎓 Tujuan Proyek

Proyek ini dikembangkan sebagai **tugas Ujian Akhir Semester (UAS)** pada mata kuliah **Pemrosesan Bahasa Alami (NLP)**, Semester Genap Tahun Ajaran 2024/2025. Proyek ini mendemonstrasikan bagaimana teknologi STT, LLM, dan TTS dapat diintegrasikan menjadi sebuah sistem chatbot suara berbasis web yang interaktif dan *user-friendly*.

## 👤 Penulis

Dikembangkan oleh M Nabil Maulana dan Farhanul Khair — Mahasiswa Informatika, Universitas Syiah Kuala
