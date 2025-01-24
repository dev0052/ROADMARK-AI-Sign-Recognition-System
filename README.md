
# Traffic Sign Recognition using YOLO

This project implements traffic sign recognition using the YOLO (You Only Look Once) object detection algorithm. The goal is to accurately detect and classify various traffic signs in images or video streams in real-time.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Training](#training)
- [Evaluation](#evaluation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Traffic sign recognition is a critical component of advanced driver-assistance systems (ADAS) and autonomous driving. This project leverages the YOLO algorithm to perform efficient and accurate detection of traffic signs.

## Features

- Real-time detection and classification of traffic signs
- High accuracy with optimized YOLO architecture
- Support for custom datasets

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/dev0052/Traffic_Sign_Recognition-YOLO.git
   cd Traffic_Sign_Recognition-YOLO
   ```

2. **Create a virtual environment (optional but recommended):**

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install the required dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Prepare the dataset:**

   - Ensure your dataset is organized and labeled appropriately. Refer to the Dataset section for more details.

2. **Train the model:**

   - Configure the training parameters as needed.
   - Run the training script:

     ```bash
     python train.py --data data.yaml --cfg cfg/yolov5s.yaml --weights yolov5s.pt --epochs 50
     ```

3. **Evaluate the model:**

   - After training, evaluate the model's performance:

     ```bash
     python val.py --data data.yaml --weights runs/train/exp/weights/best.pt
     ```

4. **Detect traffic signs in new images or videos:**

   - Use the trained model to perform detection:

     ```bash
     python detect.py --weights runs/train/exp/weights/best.pt --source path/to/your/image_or_video
     ```

## Dataset

To train the model, you'll need a dataset of traffic sign images with corresponding annotations. You can use publicly available datasets or create your own. Ensure that the dataset is in a format compatible with YOLO training.

## Training

The training process involves configuring the YOLO model architecture and hyperparameters. Adjust the settings in the configuration files as needed to suit your dataset and requirements.

## Evaluation

Evaluate the trained model using validation datasets to assess its performance. Metrics such as precision, recall, and mean Average Precision (mAP) are commonly used.

## Results

Include visualizations of detection results, performance metrics, and any other relevant findings here.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please fork the repository and submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
