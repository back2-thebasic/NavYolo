# Setup
This document provides instructions for setting up the environment required to run this project.

1. Create Conda Environment 
```
conda create -n myenv python=3.9 -y
conda activate myenv
```

2. Install PyTorch 
```
pip install torch==1.11.0+cu113 torchvision==0.12.0+cu113 torchaudio==0.11.0 --extra-index-url https://download.pytorch.org/whl/cu113
```

3. Install MMCV
```
pip install mmcv==2.1.0 -f https://download.openmmlab.com/mmcv/dist/cu113/torch1.11.0/index.html
```
4. Install ONNX
```
pip install onnx==1.16.1
```

# About the Dataset
This model is trained and evaluated on the PASCAL VOC 2007 dataset, a classic benchmark in the field of object detection.

If you wish to use the same VOC2007 dataset to quickly replicate this model or start your first YOLO training session, I have prepared a convenient solution for you. The dataset has been pre-processed into the YOLO format (including train/val/test splits) and the corresponding configuration file (.yaml) is provided.

Please visit our dedicated dataset repository for all resources:

https://github.com/back2-thebasic/VOC-Datasets

You can directly download the data from that repo and start training immediately, skipping all the cumbersome data preparation steps.

# Model Performance Comparison
**VOC2007 Dataset Results**
| Model       | Precision (%) | Recall (%) | F1 (%) | mAP50 (%) | Model Size (MB) | FLOPs (G) |
|-------------|---------------|------------|--------|-----------|-----------------|-----------|
| YOLOv3-tiny | 57.53         | 49.97      | 53.53  | 50.76     | 23.2            | 19.1      |
| YOLOv5      | 58.19         | 43.71      | 49.84  | 47.88     | 8.02            | 11.9      |
| YOLOv6      | 61.69         | 46.23      | 52.86  | 50.85     | 5.03            | 7.2       |
| YOLOv8n     | 60.06         | 47.78      | 53.23  | 52.18     | 5.95            | 8.2       |
| Nav-YOLO    | **75.09**     | **58.40**  | **65.71** | **62.52** | 6.02            | 6.9       |


**VOC2010 Dataset Results**
| Model       | Precision (%) | Recall (%) | F1 (%) | mAP50 (%) | Model Size (MB) | FLOPs (G) |
|-------------|---------------|------------|--------|-----------|-----------------|-----------|
| YOLOv3-tiny | 61.49         | 51.32      | 55.95  | 53.72     | 23.2            | 19.1      |
| YOLOv5      | 62.46         | 51.27      | 56.36  | 55.09     | 5.02            | 7.2       |
| YOLOv6      | 64.00         | 53.25      | 58.21  | 57.19     | 8.28            | 11.9      |
| YOLOv8n     | 64.73         | 53.63      | 58.68  | 58.46     | 6.22            | 8.2       |
| Nav-YOLO    | **70.97**     | **57.42**  | **63.51** | **63.43** | 6.02            | 7.8       |

