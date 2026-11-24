<div align="center">

# 🎙️ GHX VOICE STUDIO V5

**Professional multilingual voice cloning, voice design and audio production in one workspace.**

<a href="https://colab.research.google.com/github/GHX-STUDIO-786/GHX-VOICE-STUDIO-V5/blob/main/GHX_VOICE_STUDIO_V5.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Google Colab"></a>

**Developer: GHX STUDIO**

</div>

---

## ✨ Features

| Tool | What it does |
|---|---|
| **Voice Clone** | Clone a voice from a 3–10 second reference recording. A reference transcript is optional and can be transcribed automatically. |
| **Voice Design** | Create a voice using gender, age, pitch, style, accent and ready-made presets. |
| **Auto Voice** | Generate speech without supplying a saved voice or reference recording. |
| **Expressions** | Add non-verbal expression tags such as `[laughter]` and `[sigh]` to scripts. |
| **Voice Library** | Save, reuse, refresh and delete voice profiles. |
| **Batch Export** | Render one audio file per line and download the results as a ZIP. |
| **Advanced Settings** | Configure language, duration, guidance scale, denoising and audio preprocessing/postprocessing. |
| **Guide** | View system status, usage tips and responsible-use guidance. |

Additional capabilities include automatic sentence-level splitting for long scripts, adjustable generation quality and speaking speed, a live processing log, and 24 kHz WAV output.

## 🚀 Quick start — Google Colab

1. Open this repository's **Open in Google Colab** button above.
2. In Colab, select **Runtime → Change runtime type → T4 GPU** (or another available GPU).
3. Run **Step 1 — Verify GHX Access**. Enter the registered Gmail and sign in to Colab with that same Google account.
4. The notebook checks the email against the GHX Cloudflare license server. Only an active client with status `ok` can continue.
5. Run **Step 2 — Setup**, then **Step 3 — Launch**.
6. Open the public Gradio link shown in the output. Keep the launch cell running while using the studio.

## 💻 Run locally

Local developer runs do not perform the Colab Google-account check or Cloudflare license gate. Use the Colab launcher above when testing customer access control.

```bash
git clone https://github.com/GHX-STUDIO-786/GHX-VOICE-STUDIO-V5.git
cd GHX-VOICE-STUDIO-V5
pip install -r requirements.txt
python app.py
```

The local interface is normally available at `http://localhost:7860`. A CUDA-capable GPU is recommended. To test the interface without downloading the voice model, set `AS_DEMO_MODE=1`.

## 🎯 Tips for best results

- Use a clean 3–10 second reference clip with minimal background noise.
- Use a reference recording in the same language as the target script when possible.
- Quality settings: **16** for faster generation, **32** for balanced output, and **48+** for higher quality (at the cost of time).
- Write numbers as words when exact spoken pronunciation matters.
- Long scripts are split at sentence boundaries automatically.
- Use the preprocessing and postprocessing controls to manage silence in reference and generated audio.

## 🗂️ Project structure

```text
├── app.py                    # Studio interface and workflow
├── engine.py                 # Voice engine wrapper
├── GHX_VOICE_STUDIO_V5.ipynb # Google Colab setup and launcher
├── requirements.txt          # Python dependencies
├── NOTICE.md                 # Third-party credits and licenses
└── README.md                 # Project documentation
```

## 🛠️ Troubleshooting

| Issue | What to try |
|---|---|
| Generation is slow | Select a GPU in **Runtime → Change runtime type**. |
| Colab public link does not appear | Wait for model loading to finish; then check the launch cell output. |
| Processing failed | Check the script and reference audio, then review the Colab output and `studio.log`. |
| GPU memory error | Reduce generation quality or shorten the script. |
| Output accent is unexpected | Try a reference clip in the target language. |

## ⚠️ Responsible use

Only clone your own voice or a voice for which you have explicit permission. Do not use this software for fraud, impersonation, harassment or other unlawful activity. You are responsible for your use of the tool.

## 🙏 Third-party credits

This project uses open-source components. See [NOTICE.md](NOTICE.md) for third-party credits and license information.

---

<div align="center">Developed by <strong>GHX STUDIO</strong></div>
