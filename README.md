# Tree Detection Using YOLOv11 🌳🔍

This repository implements tree detection using **YOLOv11**, trained on a **Roboflow dataset** to detect trees in images efficiently. The model is fine-tuned to achieve accurate predictions and is ready for deployment.

## 🚀 Features
- Utilizes **YOLOv11** for real-time tree detection.
- Trained on a high-quality **Roboflow dataset**.
- Supports **batch inference** and **real-time predictions**.
- Outputs **bounding boxes** around detected trees.
- Configurable confidence threshold for predictions.

## 📂 Dataset
The dataset used for training is sourced from **Roboflow**. Please make sure to download the dataset and extract it to the appropriate directory before training or testing.

## 🛠 Installation & Setup
To set up the environment, install the required dependencies:

```bash
pip install ultralytics roboflow opencv-python numpy matplotlib
```

Clone the repository and navigate to the project directory:

```bash
git clone https://github.com/TanvirArefin/Tree-Detection-Using-YOLOv11.git
cd tree-detection-yolov11
```

## 🔧 Model Training
Train the YOLOv11 model using the provided dataset:

```bash
!yolo task=detect mode=train model=yolov11.pt data=dataset.yaml epochs=50 imgsz=640
```

## 🔍 Inference (Prediction)
Use the trained model to detect trees in test images:

```bash
!yolo task=detect mode=predict model={HOME}/runs/detect/train3/weights/best.pt \
     conf=0.25 source={dataset.location}/test/images save=True
```

This command will process images and save results with bounding boxes.

## 📊 Results & Evaluation
- The trained model achieves **high accuracy** on the test dataset.
- Performance metrics like **mAP, precision, and recall** can be visualized.
- Supports **real-time video inference**.

## 📌 Future Improvements
- Fine-tune the model with a **larger dataset** for better accuracy.
- Implement **real-time tree detection on video streams**.
- Optimize inference speed for **edge devices**.

## 📜 License
This project is released under the **MIT License**.

---

🔥 **Contributions are welcome!** Feel free to fork this repository and improve the tree detection pipeline. 🚀

