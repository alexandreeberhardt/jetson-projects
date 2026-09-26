# Jetson Projects

Projects running on an NVIDIA Jetson Orin Nano 8 GB (JetPack 6, L4T R36.4).
Each project lives in its own repository and is included here as a git submodule.

| Project | Description |
|---------|-------------|
| [jetson-yolo-fruit](https://github.com/alexandreeberhardt/jetson-yolo-fruit) | Real-time apple and banana detection from the CSI camera with YOLO11n and TensorRT, signalled by the power LED |
| [jetson-qwen-benchmark](https://github.com/alexandreeberhardt/jetson-qwen-benchmark) | Benchmark of six small Qwen models served by Ollama, and an offline chat assistant built from the best one |

## Clone

```bash
git clone --recursive git@github.com:alexandreeberhardt/jetson-projects.git
```

If the repository was cloned without `--recursive`:

```bash
git submodule update --init
```

## Update the submodules

To point this repository to the latest commit of each project:

```bash
git submodule update --remote
git commit -am "Update submodules"
```
