# Underwater Object Detection Using WaterNet and YOLOv7

This repository focuses on **underwater object detection**, leveraging two state-of-the-art methods: **WaterNet** for underwater image enhancement and **YOLOv7** for real-time object detection. The project aims to tackle challenges such as low visibility and color distortions in underwater environments to improve the accuracy of object detection.

## 📌 **Project Highlights**
- **WaterNet**: Enhances underwater images by correcting distortions, improving visibility, and restoring colors, making detection tasks more effective.
- **YOLOv7**: A cutting-edge object detection model offering superior accuracy and speed, tailored for detecting underwater objects in challenging conditions.
- **Dataset Integration**: Utilizes the Roboflow Aquarium Dataset with diverse marine species for training and testing.

## 📁 **Dataset**
The project uses the **Aquarium Dataset** provided by Roboflow, consisting of images and annotations formatted for object detection. The dataset includes images collected from aquariums in the United States, annotated with bounding boxes for seven classes of marine life.

### **Directory Structure**

aquarium_pretrain/ ├── train/ │ ├── images/ │ ├── labels/ ├── valid/ │ ├── images/ │ ├── labels/ ├── test/ ├── images/ ├── labels/


### **Class Labels**
The dataset includes the following **7 classes**:
1. `fish`
2. `jellyfish`
3. `penguin`
4. `puffin`
5. `shark`
6. `starfish`
7. `stingray`

### **Dataset Details**
- Train: Images in `train/images` with annotations in `train/labels`
- Validation: Images in `valid/images` with annotations in `valid/labels`
- Test: Images in `test/images` with annotations in `test/labels`
- Annotations are provided in `.txt` format, matching YOLO's requirements.

The dataset was sourced from the following link:
[Roboflow Aquarium Dataset](https://public.roboflow.ai/object-detection/aquarium)

### Sample Image Name

IMG_8379_jpg.rf.508f381df23405933378196381fd0949.jpg


---

## 🛠️ **Project Features**
1. **Image Preprocessing**:
   - Applies WaterNet to enhance underwater images before detection.
2. **Object Detection**:
   - Trains YOLOv7 on the Aquarium Dataset for real-time detection of marine objects.
3. **Visualization and Analysis**:
   - Tools to visualize results and compare the impact of WaterNet preprocessing on YOLOv7's performance.

## 🚀 **Usage**
1. Clone the repository and install dependencies:
   ```bash
   git clone https://github.com/<your-username>/underwater-object-detection
   cd underwater-object-detection
   pip install -r requirements.txt

Download and organize the dataset under the aquarium_pretrain/ directory.
Train the YOLOv7 model with the dataset:
  ```bash
  python train.py --data data.yaml --weights yolov7.pt
  python detect.py --weights runs/train/exp/weights/best.pt --source aquarium_pretrain/test/images
  ```
📊 Evaluation
Includes scripts to evaluate detection performance using metrics like:

Mean Average Precision (mAP)
Precision
Recall
🌊 Applications
Marine biodiversity monitoring
Underwater vehicle navigation
Marine life conservation
Environmental health assessment
🔗 Resources
Dataset: Roboflow Aquarium Dataset
YOLOv7: GitHub Repository
WaterNet: Research Paper
Feel free to contribute or share your ideas for improving the project! 🌊🐟





