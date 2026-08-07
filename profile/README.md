# ARBO-TEAM

**arboOCR** is a fast, self-contained OCR engine (PP-OCRv6 ONNX weights via
ONNXRuntime, CPU/GPU/TensorRT) with a single prebuilt binary
(`arboocr_demo`) that every wrapper below drives via subprocess — no C++
build required to use any of them.

### ⚙ Core engine

|🧑‍💻Language|🏗️Project|⭐️Stars|📝Description|
|:---:|:---|:---|:---|
|C++|[🔥ArboOCR](https://github.com/wafik/ArboOCR)|![GitHub Repo stars](https://img.shields.io/github/stars/wafik/ArboOCR?style=flat-square)|The simplest OCR library for C++, with support for TensorRT, Nvidia GPU and CPU.|

### 📦 Language wrappers

|🧑‍💻Language|🏗️Project|⭐️Stars|📝Description|
|:---:|:---|:---|:---|
|PHP|[ArboOcrPhp](https://github.com/ARBO-TEAM/ArboOcrPhp)|![GitHub Repo stars](https://img.shields.io/github/stars/ARBO-TEAM/ArboOcrPhp?style=flat-square)|Simplest PHP OCR, with sub process cpp.|
|Go|[arbo-ocr-go](https://github.com/ARBO-TEAM/arbo-ocr-go)|![GitHub Repo stars](https://img.shields.io/github/stars/ARBO-TEAM/arbo-ocr-go?style=flat-square)|Simplest Go OCR, with sub process cpp.|
|Rust|[arbo-ocr-rust](https://github.com/ARBO-TEAM/arbo-ocr-rust)|![GitHub Repo stars](https://img.shields.io/github/stars/ARBO-TEAM/arbo-ocr-rust?style=flat-square)|Simplest Rust OCR, with sub process cpp.|
|Python|[arbo-ocr-python](https://github.com/ARBO-TEAM/arbo-ocr-python)|![GitHub Repo stars](https://img.shields.io/github/stars/ARBO-TEAM/arbo-ocr-python?style=flat-square)|Python wrapper for arboOCR — runs the prebuilt `arboocr_demo` binary via subprocess, no C++ build required.|

Every wrapper spawns the same `arboocr_demo` release binary per call and
parses its `--json` output — so accuracy is identical across all four;
what differs is each language's own process-spawn/interpreter overhead.
Benchmarked head-to-head against each other and against RapidOCR /
RapidOcrOnnx on a 40-image SROIE sample; Go and Rust add the least
overhead (near-zero on top of raw process-spawn), PHP and Python pay
their interpreter's own startup cost on top.

<a href="https://github.com/orgs/ARBO-TEAM/repositories"><img alt="All Repositories" title="All Repositories" src="https://custom-icon-badges.demolab.com/badge/-Click%20Here%20For%20All%20Repos-1F222E?style=for-the-badge&logoColor=white&logo=repo"/></a>
