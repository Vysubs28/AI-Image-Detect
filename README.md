# AI Image Classifier — Vision Transformer

[![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)](https://pytorch.org)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co/spaces/vysubs28/image-detect-app)
[![Gradio](https://img.shields.io/badge/Gradio-FF7C00?style=flat)](https://gradio.app)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)


---

## Overview

Image classification web app powered by a **Vision Transformer (ViT)** pretrained model from Hugging Face. Upload any image and receive a predicted label with confidence score — running on CPU, GPU, or Apple Silicon MPS.

Vision Transformers apply the transformer attention mechanism — originally developed for NLP — to image patches, treating an image as a sequence of fixed-size tiles. This architecture consistently outperforms traditional CNNs on large-scale image classification benchmarks and is the foundation of modern computer vision systems in medical imaging, autonomous vehicles, satellite analysis, and quality inspection.

---

## Live Demo

[**Try the app on Hugging Face Spaces**](https://huggingface.co/spaces/vysubs28/image-detect-app)

Upload any image → receive predicted label + confidence score in real time. No setup required.

---

## How It Works

```
User uploads image (web UI)
        ↓
Image preprocessed into fixed-size patches (ViT tokenization)
        ↓
Vision Transformer applies multi-head self-attention across patches
        ↓
Classification head produces label probabilities
        ↓
Top prediction + confidence score displayed
```

**Hardware acceleration:** Automatically uses GPU if available, Apple Silicon MPS if on macOS, or falls back to CPU — no configuration required.

---

## Tech Stack

| Component | Technology |
|---|---|
| Model | Vision Transformer (ViT) via Hugging Face |
| Inference | PyTorch (CPU / GPU / MPS) |
| NLP Library | Hugging Face Transformers |
| Web Interface | Gradio |
| Language | Python 3.11 |

---

## Local Setup

```bash
git clone https://github.com/Vysubs28/AI-Image-Classifier-ViT
cd AI-Image-Classifier-ViT

python -m venv venv
source venv/bin/activate       # macOS/Linux
# venv\Scripts\activate        # Windows

pip install -r requirements.txt
python app.py
```

The Gradio interface opens automatically in your browser.

---

## Dependencies

```
torch
transformers
gradio
```

---

## Future Work

- Fine-tune ViT on domain-specific datasets (medical imaging, satellite imagery)
- Add top-5 predictions with confidence bar chart
- Extend to object detection (DETR) and image segmentation models
- Build API endpoint for integration into production pipelines

---

## License

MIT License

---

## Author

**Vyaas Subramanian**  
[github.com/Vysubs28](https://github.com/Vysubs28) · [LinkedIn](https://linkedin.com/in/vyaas-subramanian-427468237) · [Portfolio](https://vyaasportfolio.netlify.app)
