# Vehicle Tracking with Low Light Enhancement and DeepSORT

## Overview
This code implements a vehicle tracking system using YOLOv8 for object detection, DeepSORT for tracking, and includes low light enhancement techniques. The system processes a video, tracks vehicles, and provides vehicle count statistics. 

## Prerequisites
- Python 3
- Required libraries: `torch`, `ultralytics`, `opencv`, `numpy`

## Steps to Reproduce

1. Install the required libraries:
   ```bash
   pip install torch ultralytics opencv-python numpy
### Download YOLOv8 model weights and place them in the model directory. You can obtain the weights from the official YOLOv5 repository: YOLOv5 Releases.

### Download the DeepSORT model checkpoint and place it in the deep_sort/deep/checkpoint directory. You can find the checkpoint on the official DeepSORT repository: DeepSORT Releases.

Set the video_path variable in the code to the path of the video file you want to process.

Run the code:
'bash
Copy code
python your_file_name.py
During video playback, you can press 'q' to exit, 'a' to rewind, and 'd' to fast forward.'

Additional Information

I have used pretrained model for testing purposes, feel free to deploy your customized models.
The system enhances low-light conditions using gamma correction and adjusts contrast.
Vehicles are tracked using the DeepSORT algorithm, which associates bounding boxes over consecutive frames.
The code saves tracking information in a CSV file (tracking_info.csv) with details such as vehicle counts and total person count unit (PCU) every 30 seconds.
Feel free to adjust the confidence threshold (conf), image size (imgsz), and other parameters in the code based on your specific requirements.
