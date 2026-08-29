# <div align="center">xyether anime</div>

<div align="center">

### Fast, clean 2× upscaling for anime artwork

<p>
  <img src="https://img.shields.io/badge/scale-2×-7c3aed?style=for-the-badge" alt="2x scale" />
  <img src="https://img.shields.io/badge/architecture-SRVGG-2563eb?style=for-the-badge" alt="SRVGG architecture" />
  <img src="https://img.shields.io/badge/domain-anime-f97316?style=for-the-badge" alt="Anime model" />
  <img src="https://img.shields.io/badge/focus-fast%20inference-16a34a?style=for-the-badge" alt="Fast inference" />
</p>

<p>
  <strong>xyether anime</strong> is a 2× anime super-resolution model made to keep lines, colors, and character details looking sharp while staying quick to run.
</p>

<p>
  <a href="#-what-it-does">What it does</a> ·
  <a href="#-preview">Preview</a> ·
  <a href="#-model-variants">Model variants</a> ·
  <a href="#-usage">Usage</a>
</p>

</div>

---

## ✨ What it does

Anime images can lose clean line art and small details when enlarged. xyether anime is built to give them a sharper 2× upscale without making the process unnecessarily slow.

- Anime and illustration focused
- 2× enlargement
- SRVGG-based architecture
- Designed with fast, real-time-friendly inference in mind
- Available in formats for different workflows

> Speed depends on your GPU, resolution, precision, runtime, and tiling settings.

## 🖼️ Preview

The preview image is stored in the repository root as `preview image.jpg`.

<div align="center">
  <img src="preview%20image.jpg" alt="xyether anime 2x upscaling preview" width="100%" />
</div>

## 📦 Model variants

Download all versions from the [**models release page**](https://github.com/XYETHER/Xyether-Anime-Upscaler/releases/tag/models).

| Variant | Best for |
| --- | --- |
| **Safetensors** | PyTorch and compatible model tools |
| **ONNX FP16** | Faster ONNX Runtime inference on supported hardware |
| **ONNX FP32** | Wider compatibility and full 32-bit precision |
| **TensorRT FP16** | Fast NVIDIA inference and Google Colab |

The TensorRT Colab engine is named `2x_XyetherAnimeV5.engine`.

All variants are intended for **2× upscaling**.

## 🛠️ Usage

Pick the format that matches your setup:

- Use **Safetensors** with a compatible PyTorch pipeline.
- Use **ONNX FP16** or **ONNX FP32** with ONNX Runtime.
- Use the **TensorRT FP16 engine** with NVIDIA TensorRT, including the Google Colab workflow.

### Recommended settings

```text
Scale:     2×
Precision: FP16 when supported, otherwise FP32
Tiling:    Enable for very large images or limited VRAM
```

### TensorRT / Google Colab

The TensorRT engine can be downloaded directly from the release page or with this URL:

```text
https://github.com/XYETHER/Xyether-Anime-Upscaler/releases/download/models/2x_XyetherAnimeV5.engine
```

For the best speed, keep the model loaded between frames, use FP16, and benchmark at the resolution you actually plan to process.

## 🧾 Quick model card

| Field | Value |
| --- | --- |
| **Name** | xyether anime |
| **Task** | Single-image super-resolution |
| **Scale** | 2× |
| **Architecture** | SRVGG |
| **Focus** | Anime and illustrated content |
| **Input / output** | RGB image → RGB image at 2× resolution |

## ⚠️ Notes

- Results depend on the input quality and art style.
- Very noisy, compressed, or already oversharpened images may look less predictable.
- “Real-time” speed depends on the hardware and runtime being used.
- The TensorRT engine is intended for NVIDIA TensorRT-compatible environments.

## 📜 License

Add your license here before publishing. Also make sure the license covers the model weights, code, preview image, training data, and any third-party components you used.

## 🙌 Credits

Built and released by **xyether**.

If you use xyether anime in a project, linking back to this repository is appreciated.

<div align="center">

### Sharp anime. Fast upscaling.

</div>
