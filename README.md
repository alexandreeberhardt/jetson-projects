# Jetson Projects

Two projects running on an NVIDIA Jetson Orin Nano 8 GB (JetPack 6). Each one lives in its own repository and is included here as a git submodule.

| Project | What it does | Measured on the board |
|---|---|---|
| [jetson-yolo-fruit](https://github.com/alexandreeberhardt/jetson-yolo-fruit) | Detects apples and bananas from the CSI camera with YOLO11n on TensorRT FP16, and signals them with the power LED | 30 fps live, about 16 ms of GPU inference per frame |
| [jetson-qwen-benchmark](https://github.com/alexandreeberhardt/jetson-qwen-benchmark) | Benchmarks six small Qwen models served by Ollama, then turns the best one into an offline chat assistant | Qwen3 4B Instruct: 7/8 on the diagnostic, 16.8 tokens/s at about 18 W, fully on the GPU |

With Ollama's default settings, the 4B model ran out of memory on the board's 8 GB of shared CPU/GPU memory. A quantized KV cache and smaller batches made it fit.

## Clone

```bash
git clone --recursive git@github.com:alexandreeberhardt/jetson-projects.git
```

If the repository was cloned without `--recursive`, run `git submodule update --init`.
