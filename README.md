# <div align="center">xyether anime</div>

<div align="center">

### A fast, high-quality 2× anime super-resolution model

<p>
  <img src="https://img.shields.io/badge/scale-2×-7c3aed?style=for-the-badge" alt="2x scale" />
  <img src="https://img.shields.io/badge/architecture-SRVGG-2563eb?style=for-the-badge" alt="SRVGG architecture" />
  <img src="https://img.shields.io/badge/domain-anime-f97316?style=for-the-badge" alt="Anime model" />
  <img src="https://img.shields.io/badge/focus-real--time-16a34a?style=for-the-badge" alt="Real-time focus" />
</p>

<p>
  <strong>xyether anime</strong> is an SRVGG-based super-resolution model built to deliver a clean 2× upscale with a strong balance between visual quality and real-time speed.
</p>

<p>
  <a href="#-overview">Overview</a> ·
  <a href="#-preview">Preview</a> ·
  <a href="#-features">Features</a> ·
  <a href="#-usage">Usage</a> ·
  <a href="#-model-card">Model card</a>
</p>

</div>

---

## ✨ Overview

Anime artwork needs more than a simple resize. Fine line art, cel-shaded color blocks, hair strands, eyes, and clean silhouettes can easily become soft or oversharpened during upscaling.

**xyether anime** is designed for that kind of content. It targets a practical middle ground:

- **Good visual quality** for anime frames, illustrations, and character art
- **Fast inference** for interactive and real-time-oriented workflows
- **Stable 2× enlargement** without changing the intended composition
- **Compact SRVGG design** suited to users who value speed as well as detail

> The model is intended for 2× super-resolution. Actual throughput depends on image size, tiling, precision, runtime, and hardware.

## 🖼️ Preview

The preview below shows the model's upscaling results. The source image is stored in the repository root as `preview image.jpg`.

<div align="center">
  <img src="preview%20image.jpg" alt="xyether anime 2x upscaling preview" width="100%" />
</div>

## 🚀 Features

| Capability | Description |
| --- | --- |
| **2× super-resolution** | Doubles the width and height of the input image. |
| **Anime-oriented output** | Tuned for illustrated and anime-style visual content. |
| **SRVGG architecture** | A compact architecture chosen with practical inference speed in mind. |
| **Real-time focus** | Designed for responsive workflows where latency matters. |
| **Clean line handling** | Aims to preserve edges, silhouettes, and fine illustrated details. |
| **Simple integration** | Suitable for Python, PyTorch, and SRVGG-compatible inference pipelines. |

## 📦 Model download

> **Release status:** Add the final model URL below when the weights are published.

| File | Scale | Format | Status |
| --- | ---: | --- | --- |
| `xyether_anime_2x.pth` | 2× | PyTorch | Coming soon |

```text
Model weights: <ADD_RELEASE_OR_HUGGINGFACE_LINK_HERE>
SHA-256:       <ADD_CHECKSUM_HERE>
```

## 🛠️ Usage

### Recommended settings

```text
Scale:       2×
Precision:   FP16 when supported, otherwise FP32
Tiling:      Enable for images that exceed available VRAM
Best suited: Anime frames, illustrations, screenshots, and character artwork
```

### Python / PyTorch-style example

The exact constructor depends on the inference wrapper used by your project. The following shows the intended flow:

```python
from PIL import Image
import torch

# Load your SRVGG-compatible xyether anime 2x model here.
# model = load_xyether_anime("xyether_anime_2x.pth")
# model.eval().to(device)

image = Image.open("input.png").convert("RGB")

with torch.inference_mode():
    # output = upscale_with_model(model, image, scale=2)
    pass

# output.save("output_2x.png")
```

### Real-time inference tips

- Use FP16 or an accelerated backend when your hardware supports it.
- Process multiple frames with a persistent model instance instead of reloading weights.
- Use tiling for very large images to control VRAM usage.
- Keep the scale fixed at **2×** for the model's intended behavior.
- Benchmark on your target resolution; speed can change significantly with image dimensions.

## 🧾 Model card

| Field | Value |
| --- | --- |
| **Name** | xyether anime |
| **Task** | Single-image super-resolution |
| **Upscale factor** | 2× |
| **Architecture** | SRVGG |
| **Primary domain** | Anime and illustrated content |
| **Design priority** | Quality / speed balance |
| **Input** | RGB images |
| **Output** | RGB images at 2× spatial resolution |

## ⚠️ Limitations

- Results depend on the quality, compression, and style of the input image.
- The model is not intended to recover genuinely missing photographic detail.
- Extremely noisy, heavily compressed, or already oversharpened images may produce less predictable results.
- Do not compare speed without keeping resolution, precision, backend, and tiling settings consistent.

## 📜 License

Add the model license here before release. Make sure the license covers the weights, code, and any training data or third-party components used by the project.

## 🙌 Credits

Built and released by **xyether**.

If you use `xyether anime` in a project, a link back to this repository is appreciated.

<div align="center">

### Fast enough for the moment. Sharp enough for the details.

</div>
