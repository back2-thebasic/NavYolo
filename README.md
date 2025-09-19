# About the Dataset
This model is trained and evaluated on the PASCAL VOC 2007 dataset, a classic benchmark in the field of object detection.

If you wish to use the same VOC2007 dataset to quickly replicate this model or start your first YOLO training session, I have prepared a convenient solution for you. The dataset has been pre-processed into the YOLO format (including train/val/test splits) and the corresponding configuration file (.yaml) is provided.

Please visit our dedicated dataset repository for all resources:

https://github.com/back2-thebasic/VOC-Datasets

You can directly download the data from that repo and start training immediately, skipping all the cumbersome data preparation steps.

# Setup
This document provides instructions for setting up the environment required to run this project.

## 1. Create Conda Environment 
conda create -n myenv python=3.9 -y
conda activate myenv

## 2. Install PyTorch 
pip install torch==1.11.0+cu113 torchvision==0.12.0+cu113 torchaudio==0.11.0 --extra-index-url https://download.pytorch.org/whl/cu113

## 3. Install MMCV
pip install mmcv==2.1.0 -f https://download.openmmlab.com/mmcv/dist/cu113/torch1.11.0/index.html

## 4. Install ONNX
pip install onnx==1.16.1
