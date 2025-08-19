# Comic Scribe

*Automated Manga Translation Pipeline*

This project is an end-to-end pipeline that translates manga/comics using Computer Vision + NLP.
It runs through **4 main stages**:

1. Speech Bubble Detection (Roboflow)
2. OCR (Text Extraction)
3. Translation
4. Text Placement

---

## Features

* Automatic speech bubble detection.
* OCR for Japanese (or other source languages).
* Neural Machine Translation (NMT) to English (or other targets).
* Bubble inpainting + translated text placement with manga fonts.
* Modular design — replace any stage with your own implementation.

---

## Project Structure

```
NLPVision4Comics/
│── data/                  # Sample manga pages
│── detection/             # Speech bubble detection
│── ocr/                   # OCR preprocessing & recognition
│── translation/           # Translation pipeline
│── placement/             # Inpainting & text placement
│── utils/                 # Shared utilities
│── main.py                # End-to-end runner
│── requirements.txt       # Dependencies
│── README.md              # Documentation
```

---

## Installation

```bash
git clone https://github.com/reiyonna/NLPVision4Comics.git
cd NLPVision4Comics
pip install -r requirements.txt
```

---

## Usage

Run the full pipeline on a manga page:

```bash
python main.py --input data/sample_page.png --output output/
```

**Options:**

* `--lang_source ja` → Source language (default: Japanese)
* `--lang_target en` → Target language (default: English)
* `--model_translation marian` → Translation model

---

## Dependencies

* Python 3.9+
* PyTorch / TensorFlow
* OpenCV
* Tesseract OCR / EasyOCR
* Hugging Face Transformers
* Pillow (PIL)
* (Optional) Stable Diffusion for advanced inpainting

Install all with:

```bash
pip install -r requirements.txt
```

---

## Roadmap

* [ ] Vertical Japanese text support.
* [ ] Multi-language translations (EN, FR, ES, etc.).
* [ ] Transformer-based bubble detection.
* [ ] Manga-specific translation fine-tuning.
* [ ] Web/GUI interface for interactive editing.

---
