# Overview 📚
## ✔️Abstract
A rock-paper-scissors game with the computer using a live video feed from the camera. Transfer learning was used to fine-tune SSD_mobilenet_v2, a pre-trained [Tensorflow Object Detection (TFOD)](https://github.com/tensorflow/models/tree/master/research/object_detection) model, to detect the 3 hand gestures. 
[OpenCV](https://opencv.org/) library was used for all camera-related operations.

*Initially I trained the model on fewer images and epochs. Since the results were not good, I tuned the model by adding more variety of images and training on more epochs.*
## ✔️Dataset
I created a [custom dataset](https://github.com/AparGarg99/RPSGame/tree/master/Dataset) for this project. <br>
![](https://github.com/AparGarg99/RPSGame/blob/master/images/dataset.PNG)

## ✔️Methodology
1. **Split** - <br>
![](https://github.com/AparGarg99/RPSGame/blob/master/images/split.PNG) <br>
2. The pipeline.config file contains the pipeline followed.<br>
    2.1. **Preprocessing** - Images were resized to 320x320 pixel squares.<br>
    2.2. **Augmentation** - <br><br>
    ![](https://github.com/AparGarg99/RPSGame/blob/master/images/augment.PNG) <br><br>
    2.3. **Model Development** - Transfer Learning was performed on [ssd_mobilenet_v2_fpnlite_320x320_coco17_tpu-8](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md) model to detect 3 hand gestures. The 3 gestures were: (1) Peace (V) sign - Scissors sign. (2) Fist - Rock sign. (3) Straight hand or Five - Paper sign. <br>

![](https://github.com/AparGarg99/RPSGame/blob/master/images/epochs.PNG)<br>

3. **Game Development** - OpenCV was used for all camera-related operations. The flow for this implementation was simple: (1) Start webcam feed and read each frame. (2) Pass this frame to model for classification ie. predict class. (3) Make a random move by computer. (4) Calculate Score.

## ✔️Results
mAP on Test dataset:
* Base Model - 0.80
* Tuned Model - 0.90

[Know More](https://github.com/AparGarg99/RPSGame/tree/master/images)

## ✔️Future Work
I have several ideas to improve this project:
* Re-train other better-performing TFOD models.
* Design better GUI.
* Add more data in different surroundings with different lightings.
* Add a gesture to terminate the game.
* Take appropriate action if the user shows more than one gesture simultaneously.


# GUI 👨‍💻
![](https://github.com/AparGarg99/RPSGame/blob/master/images/final2.gif)<br>
***Note:*** *The system detects gestures well from both the hands.*

# Installation and Usage 🔌
1. To label images and train the model refer this [tutorial](https://github.com/AparGarg99/Tutorials/tree/master/TFOD).
2. To develop the game use [main.ipynb](https://github.com/AparGarg99/RPSGame/blob/master/main.ipynb)

<br>
<br>

***Don't forget to give a ⭐ if you like this project !!***
