# Overview 📚
## ✔️Abstract
A rock-paper-scissors game using live video feed from the camera. Transfer learning was used to fine-tune SSD_mobilenet_v2, a pre-trained Tensorflow Object Detection (TFOD) model, to detect 3 hand gestures. 
OpenCV library was used for all camera related operations.

*Initially I trained the model on less images and epochs. Since the results were not good, I tuned the model by adding more variety of images and training on more epochs.*
## ✔️Dataset
* I created a custom dataset for this project. <br>
![](https://github.com/AparGarg99/RPSGame/blob/master/images/dataset.PNG)

## ✔️Methodology
1. **Split** - <br>
![](https://github.com/AparGarg99/RPSGame/blob/master/images/split.PNG) <br>
2. The pipeline.config file contains the pipeline followed.<br>
&nbsp; 2.1. **Preprocessing** - Images were resized to 320x320 pixel squares.<br>
&nbsp; 2.2. **Augmentation** - <br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![](https://github.com/AparGarg99/RPSGame/blob/master/images/augment.PNG) <br>
&nbsp; 2.3. **Model Development** - Transfer Learning was performed on [ssd_mobilenet_v2_fpnlite_320x320_coco17_tpu-8]() model.
3. **Deployment using OpenCV** - The flow for this implementation is simple: (1) Start webcam feed and read each frame. (2) Pass this frame to model for classification ie. predict class. (3) Make a random move by computer. (4) Calculate Score.

## ✔️Results
![](https://github.com/AparGarg99/RPSGame/blob/master/images/epochs.PNG)

### Base Model
![](https://github.com/AparGarg99/RPSGame/blob/master/images/v1_1.PNG)
![](https://github.com/AparGarg99/RPSGame/blob/master/images/v1_2.PNG)
<br>
### Tuned Model
![](https://github.com/AparGarg99/RPSGame/blob/master/images/v2_1.PNG)
![](https://github.com/AparGarg99/RPSGame/blob/master/images/v2_2.PNG)


## ✔️Future Work
I have several ideas to improve this project:
* Train other better performing TFOD models.
* Design better GUI.
* Add more data in different surroundings with different lightings.
* Add a gesture to terminate the game.
* Take appropriate action if user shows more than one gestures simultaneously.


# GUI 👨‍💻
![trim](https://user-images.githubusercontent.com/54896849/119932196-6e3b8880-bfa0-11eb-8c26-1c0f32bd98ce.gif)


# Installation and Usage 🔌
[Click Here](https://github.com/AparGarg99/Tutorials/blob/master/streamlit_frontend_tutorial/README.md#installation-and-usage) for reference.

<br>
<br>

***Dont forget to give a ⭐ if you like this project !!***
