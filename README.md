<p align="center">
  <a href="https://github.com/jatindalal">
   __     ______     ______   __     __   __    
  /\ \   /\  __ \   /\__  _\ /\ \   /\ "-.\ \   
 _\_\ \  \ \  __ \  \/_/\ \/ \ \ \  \ \ \-.  \  
/\_____\  \ \_\ \_\    \ \_\  \ \_\  \ \_\\"\_\ 
\/_____/   \/_/\/_/     \/_/   \/_/   \/_/ \/_/ 

  </a>
</p>

<h3 align="center">C++ / Python Integration · ONNX Runtime · Inference Performance</h3>

<p align="center">
  I help computer-vision and ML teams move performance-critical workloads<br/>
  from Python into modern C++, without making deployment painful.
</p>

---

### What I work on

- **Python bindings for C++ libraries**: nanobind/pybind11 extensions, NumPy interoperability, GIL-safe long-running calls, wheels and packaging
- **C++ ONNX Runtime inference pipelines**: provider selection, preprocessing/postprocessing, latency-aware real-time processing
- **CPU/GPU performance optimization**: profiling, multithreading, queue design, CUDA acceleration where it pays for itself
- **Real-time video, sensor, and point-cloud systems**: LiDAR tooling, frame pipelines, visualization
- **Cross-platform CMake builds**: Linux, macOS, Windows; CI and reproducible releases

### Selected experience

- Redesigned a 3D multi object-tracking pipeline to handle **2,000+ concurrent objects**
- Improved tracking throughput **5×** via CUDA acceleration
- Built **Pybind11 and LibTorch bindings** for production C++ inference, sensor, and post-processing components
- Worked hands-on with **LibTorch, CUDA, ONNX Runtime, LiDAR SDKs, FFmpeg, OpenGL**
- Ported real-time C++ systems **between Linux and Windows**

### Featured

> **[`cpp-onnx-python`](https://github.com/jatindalal/cpp-onnx-python)** — `v0.1.0` released: a packaged C++20 + ONNX Runtime inference library exposed to Python through nanobind. Bundles ONNX Runtime, takes NumPy in and returns owned NumPy arrays, validates dtype/rank/shape/device/contiguity before calling ORT, maps native failures to `ValueError` / `FileNotFoundError` / `NotImplementedError` / `RuntimeError`, and releases the GIL around session build and inference. Stable-ABI `cp312-abi3` wheels for **macOS 14+ arm64**, **Linux x86_64** and **Linux aarch64** (`manylinux_2_28`) are [on the Releases page](https://github.com/jatindalal/cpp-onnx-python/releases/latest); a 27-case pytest suite plus a native CTest suite exercise the same C++ core.
>
> Measured on Apple M3 Pro / ONNX Runtime 1.30.0: **1.21–1.24× faster per call than the official `onnxruntime` Python wheel** on the fixed-overhead fixture, and a real-model CoreML benchmark where speedup is model-dependent — **4.1×** for MobileNetV2 (ANE+GPU), **~0.5×** for the YuNet detector, NaN for a super-resolution transformer. No general GPU-speedup claim is made.

### Selected open source

| Project | What it demonstrates |
|---|---|
| [cpp-onnx-python](https://github.com/jatindalal/cpp-onnx-python) | Packaged C++20 + ONNX Runtime inference library with nanobind bindings (`v0.1.0`): bundled ORT runtime, owned NumPy in/out, explicit dtype/shape/contiguity validation, Python exception taxonomy, GIL-released inference, stable-ABI wheels for macOS/Linux, and committed CPU + CoreML benchmarks on real models |
| [OxyRT](https://github.com/jatindalal/OxyRT) | C++20 real-time object detection on ONNX Runtime: session management, preprocessing, output decoding, provider selection, live latency telemetry |
| [anonrt](https://github.com/jatindalal/anonrt) | Modern C++ video pipeline: real-time face anonymization, bounded queues, background processing, MP4 export |
| [visin](https://github.com/jatindalal/visin) | Point-cloud visualization: file-format I/O, GPU-backed rendering (ModernGL), camera math, tested NumPy data handling |
| [human-activity-detection](https://github.com/jatindalal/human-activity-detection) | End-to-end ML product: model inference, async API, webcam capture, frontend |
| [SocketSphere](https://github.com/jatindalal/socket-sphere) | Asynchronous C++ networking with framed protocols |

### Working with me

| Engagement | What you get | Good fit when |
|---|---|---|
| **Performance audit** | Profiling setup, hotspot report, before/after measurements, one prioritized fix implemented | Latency or throughput is off but you don't know where the time goes |
| **Python binding sprint** | Production-ready pybind11/nanobind module: NumPy interop, GIL-safe calls, exception translation, tests, wheels | You have a C++ library your Python team can't use efficiently |
| **ONNX Runtime integration** | C++ inference wrapper, provider setup, pre/post-processing, benchmark report | A Python prototype needs native deployment or real-time performance |

Most engagements start with a short paid audit, you get a concrete measurement of what's slow and what it would cost to fix, whether or not we continue.

📫 **jd.jatindalal@gmail.com** · [LinkedIn](https://linkedin.com/in/jatindalal)

---

### Core stack

<p align="left">
  <img src="https://img.shields.io/badge/C%2B%2B20-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++20" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/pybind11-3670A0?style=for-the-badge" alt="pybind11" />
  <img src="https://img.shields.io/badge/nanobind-3670A0?style=for-the-badge" alt="nanobind" />
  <img src="https://img.shields.io/badge/ONNX_Runtime-005CED?style=for-the-badge" alt="ONNX Runtime" />
  <img src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=black" alt="CUDA" />
  <img src="https://img.shields.io/badge/CMake-064F8C?style=for-the-badge&logo=cmake&logoColor=white" alt="CMake" />
  <img src="https://img.shields.io/badge/Qt-41CD52?style=for-the-badge&logo=qt&logoColor=white" alt="Qt" />
  <img src="https://img.shields.io/badge/FFmpeg-007808?style=for-the-badge&logo=ffmpeg&logoColor=white" alt="FFmpeg" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
</p>

<p align="center">
  <img height="150" src="https://github-readme-stats-five-sigma-99.vercel.app/api/top-langs/?username=jatindalal&layout=compact&theme=tokyonight&title_color=2ea043&icon_color=2ea043&hide_border=true&bg_color=00000000&langs_count=6" alt="top langs" />
</p>
