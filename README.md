<div align="center">

# xyether anime

### Fast 2× anime image upscaling

[![Scale](https://img.shields.io/badge/scale-2%C3%97-7c3aed?style=for-the-badge)](https://github.com/XYETHER/Xyether-Anime-Upscaler)
[![Architecture](https://img.shields.io/badge/architecture-SRVGG-2563eb?style=for-the-badge)](https://github.com/XYETHER/Xyether-Anime-Upscaler)
[![Domain](https://img.shields.io/badge/domain-anime-f97316?style=for-the-badge)](https://github.com/XYETHER/Xyether-Anime-Upscaler)

**xyether anime** is a fast SRVGG-based model for clean 2× upscaling of anime artwork and illustrations.

[Preview](#-preview) · [Models](#-model-variants) · [Google Colab](#-google-colab)

</div>

---

## ✨ What it does

- Clean 2× enlargement for anime and illustrated images
- Preserves line art, colors, and character detail
- SRVGG architecture with fast inference
- Safetensors, ONNX, and TensorRT variants available

## 🖼️ Preview

<img src="preview%20image.jpg" alt="xyether anime 2x upscaling preview" width="100%" />

## 📦 Model variants

Download models from the [release page](https://github.com/XYETHER/Xyether-Anime-Upscaler/releases/tag/models).

| Variant | Best for |
| --- | --- |
| **Safetensors** | PyTorch workflows |
| **ONNX FP16** | Fast ONNX Runtime inference |
| **ONNX FP32** | Maximum compatibility |
| **TensorRT FP16** | Fast NVIDIA and Colab inference |

All variants upscale images by **2×**.

## 🚀 Google Colab

Run the TensorRT version directly in Google Colab:

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/XYETHER/Xyether-Anime-Upscaler/blob/main/Xyether_Anime_Upscaler.ipynb)

Select a **T4 GPU** and run the single upscaling cell. It includes setup and uses the FP16 `2x_XyetherAnimeV5_T4_TRT10.16.1.11.engine` with **TensorRT 10.16.1.11**. Leave `video_path` empty to upload an image or video, or provide a file/folder path.

## 🧾 Model card

| Field | Value |
| --- | --- |
| **Task** | Single-image super-resolution |
| **Scale** | 2× |
| **Architecture** | SRVGG |
| **Focus** | Anime and illustrated content |
| **Input / output** | RGB image → RGB image at 2× resolution |

## 📜 License

This project is licensed under the [MIT License](LICENSE).

## 🙌 Credits

Built and released by **xyether**.

<div align="center">

### Sharp anime. Fast upscaling.

</div>
