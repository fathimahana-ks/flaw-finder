# FlawFinder – Real-Time Weld Defect Detection

YOLOv8 | Python | OpenCV

---

## 🔍 Overview

A computer vision system to identify defects in welded metal joints using X-ray images.
FlawFinder leverages the power of deep learning and real-time image processing to detect weld flaws accurately and efficiently using:

* YOLOv8 object detection model
* Custom-labeled dataset of 1,000+ weld images
* OpenCV-powered visualization
* PyTorch for model training and inference

---

## 🧠 Key Features

🔎 Real-time weld defect detection using YOLOv8
📸 Custom training on over 1,000 X-ray weld images
📈 Achieved 91% detection accuracy across various test scenarios
🔧 Supports integration with industrial inspection pipelines
🧠 Modular code for retraining and fine-tuning

---

## 📁 Project Structure

```
flawfinder/
│
├── models/
│   └── yolov8_custom.pt
│
├── data/
│   ├── images/
│   ├── labels/
│   └── data.yaml
│
├── scripts/
│   ├── train.py
│   └── detect.py
│
├── results/
│   └── sample_detections.png
│
├── requirements.txt
└── README.md
```

---

## 🛠️ Technologies Used

* Python
* YOLOv8 (Ultralytics)
* OpenCV
* PyTorch
* Roboflow (optional for dataset export)

---

## 📊 Evaluation Metrics

| Metric    | Value |
| --------- | ----- |
| Accuracy  | 91%   |
| Precision | 89%   |
| Recall    | 93%   |
| F1-Score  | 91%   |

📌 Confusion matrix and example outputs are included in the `results/` folder.

---

## 🚀 How to Run

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/flawfinder.git
cd flawfinder
```

2. **Install required packages**

```bash
pip install -r requirements.txt
```

3. **Run detection**

```bash
python scripts/detect.py --source data/images --weights models/yolov8_custom.pt
```

4. **To retrain the model**

```bash
yolo detect train data=data/data.yaml model=yolov8n.pt epochs=100 imgsz=640
```

---

## 📦 Model Deployment

Use the trained model to detect defects on new images:

```python
from ultralytics import YOLO

model = YOLO('models/yolov8_custom.pt')
results = model('path/to/new_image.jpg')
results.show()
```

---

## 📌 Notes

* Dataset includes labeled X-ray images of real-world weld defects
* YOLOv8 config and hyperparameters are fully customizable
* You can enhance performance by using larger YOLO models (e.g., `yolov8m`, `yolov8l`)

---

## 📬 Contact

**Fathima Hana**  
📧 [fathimahanaks@gmail.com](mailto:fathimahanaks@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/fathimahana/) 

Feel free to reach out for collaborations or questions!
