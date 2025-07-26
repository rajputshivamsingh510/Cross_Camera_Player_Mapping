
# YOLOv8 Object Detection Project

This project demonstrates real-time object detection using YOLOv8 from the Ultralytics library. The model is used to detect objects in images and videos with high accuracy and performance.

## Features
- Uses YOLOv8 for object detection
- Real-time detection from images or videos
- Simple interface using Python and OpenCV
- Customizable for different datasets or use cases

## Installation

Make sure Python 3.7+ is installed. Then run:

```bash
pip install ultralytics opencv-python
```

You may also need:

```bash
pip install matplotlib numpy pandas
```

## Usage

### 1. Import and Load YOLOv8 Model

```python
from ultralytics import YOLO

model = YOLO("yolov8n.pt")  # Load pre-trained model
```

### 2. Run Detection on an Image

```python
results = model("path_to_image.jpg", show=True)
```

### 3. Run Detection on a Video

```python
model.predict(source="video.mp4", show=True)
```

### 4. Custom Training (Optional)

To train on a custom dataset:

```bash
yolo task=detect mode=train model=yolov8n.pt data=data.yaml epochs=50
```

## Project Structure

- `Code_Project.ipynb` – Main notebook containing all detection code and steps
- `requirements.txt` – (Optional) List of packages used

## Model Weights

This project uses the default **YOLOv8n** weights provided by Ultralytics. You can change it to `yolov8s.pt`, `yolov8m.pt`, etc., based on your accuracy and speed needs.

## References

- [Ultralytics YOLO Docs](https://docs.ultralytics.com/)
- [YOLOv8 GitHub Repo](https://github.com/ultralytics/ultralytics)
