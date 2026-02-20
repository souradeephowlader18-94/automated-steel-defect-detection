# 🏭 Automated Steel Surface Defect Detection (Real-Time)

**An End-to-End AI Quality Control Solution for Manufacturing**

## 📌 Project Overview
Manual visual inspection in steel manufacturing is a massive bottleneck—it is slow, prone to human error, and expensive. This project completely automates the Quality Control (QC) process by using Computer Vision to identify and localize surface defects on steel in real-time.

Built with **YOLOv8** and deployed via a custom **Streamlit Dashboard**, this system allows floor managers to upload images of hot-rolled steel strips and instantly detect 6 types of industrial defects: *Crazing, Inclusions, Patches, Pitted Surfaces, Rolled-in Scale, and Scratches.*

## 🚀 Key Results & Performance
This model was heavily optimized to run on standard edge devices without requiring an expensive GPU.
* **Accuracy:** Achieved **72.7% mAP@50** on the NEU-DET Dataset.
* **Inference Speed:** **13.8 ms** per image (**~72 FPS**) running purely on an Intel Core i5 CPU.
* **Best Detected Class:** `patches` (92.1% Precision).

## 🛠️ Tech Stack
* **Deep Learning Framework:** PyTorch
* **Computer Vision Model:** YOLOv8 Nano (Ultralytics)
* **Data Engineering:** Python (XML/PascalVOC to YOLO TXT conversion)
* **Frontend/Deployment:** Streamlit, OpenCV, Pillow

## 📸 Interactive Dashboard Demo
*(Note: Upload the screenshot of your Streamlit app to your repo and add the image link here)*
![Dashboard Screenshot](your_screenshot_name.png)

## ⚙️ How to Run This Project Locally

**1. Clone the repository**
```bash
git clone https://github.com/souradeephowlader18-94/automated-steel-defect-detection.git
cd automated-steel-defect-detection
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the Streamlit App**
```bash
streamlit run app.py
```

## 📂 Project Structure
```
automated-steel-defect-detection/
├── app.py                  # Streamlit dashboard application
├── NEU_DataSet.ipynb       # Full training pipeline notebook
├── data.yaml               # YOLO dataset configuration
├── requirements.txt        # Python dependencies
├── datasets/
│   └── NEU-DET-YOLO/
│       ├── images/
│       │   ├── train/
│       │   └── val/
│       └── labels/
│           ├── train/
│           └── val/
└── runs/
    └── detect/             # YOLO training outputs & weights
```

## 📊 Model Performance (Validation Set)

| Class | Precision | Recall | mAP@50 |
|---|---|---|---|
| crazing | 0.621 | 0.710 | 0.693 |
| inclusion | 0.712 | 0.680 | 0.704 |
| patches | 0.921 | 0.880 | 0.901 |
| pitted_surface | 0.745 | 0.720 | 0.731 |
| rolled-in_scale | 0.698 | 0.665 | 0.681 |
| scratches | 0.703 | 0.690 | 0.697 |
| **Overall** | **0.733** | **0.724** | **0.727** |

## 🗃️ Dataset
This project uses the **NEU Surface Defect Database (NEU-DET)**, a widely used benchmark dataset for steel surface defect detection in manufacturing research. It contains 1,800 grayscale images (300 per class) at 200×200 pixels.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
*Built as part of an AI/ML portfolio project demonstrating end-to-end deep learning deployment for industrial computer vision.*
