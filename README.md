# 🔍 Depth Estimation Using MiDaS (PyTorch)

This project demonstrates monocular depth estimation using the **MiDaS model** from Intel, a state-of-the-art deep learning model that predicts scene depth from a single RGB image. This implementation is designed for use in **Jupyter notebook**.


## 📸 Example Outputs
| Original Image                          | Depth Map                               |
| --------------------------------------- | --------------------------------------- |
| ![](./datset/mountain_river.jpg)        | ![](./outputs/mountain_river_depth.png) |
| ![](./datset/city.jpg)                  | ![](./outputs/city_depth.png)           |


## 📌 Features

- Load and preprocess custom datasets of RGB images
- Predict per-pixel depth maps using pre-trained MiDaS models (`DPT_Large`, `DPT_Hybrid`, etc.)
- Visualize original images + depth predictions side by side
- Batch prediction and optional saving of results
- Lightweight and Colab-friendly


## 📂 Project Structure
├── dataset/          # Input images
├── outputs/          # Depth map results
├── depth_estimator.py  # Main Python script
└── README.md         # Project documentation


## 📂 Dataset

The project expects a folder named `/dataset` containing 30 input RGB images.


## 🔧 Requirements

This project is designed to run on **Jupyter notebook**, but locally you would need:

- `torch`, `torchvision`
- `opencv-python`
- `matplotlib`
- `tqdm`
- `numpy`

You can install them using:

```bash
pip install torch torchvision tqdm matplotlib opencv-python
```


## 🧠 Model: MiDaS (DPT_Large)

We use the `MiDaS v3` model `DPT_Large` (based on Vision Transformers) for best accuracy, loaded via PyTorch Hub:

- Paper: [MiDaS: Robust Monocular Depth Estimation](https://arxiv.org/abs/1907.01341)
- GitHub: [intel-isl/MiDaS](https://github.com/intel-isl/MiDaS)
- Architecture: DPT (Dense Prediction Transformer)

You can easily switch to lighter variants like `DPT_Hybrid` or `MiDaS_small` for faster inference.


## 📘 Language
- Python


## 📄 License
- MIT License. This project uses MiDaS, which is available under the MIT license from intel-isl/MiDaS.
