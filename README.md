# Overview 📚
### ✔️Abstract
A rock-paper-scissors game using live video feed from the camera. Transfer learning was used to fine-tune the SSD_mobilenet_v2 pre-trained object detection model to learn how to classify and localize 3 hand gestures. 
OpenCV library was used for all camera related operations.

### ✔️Dataset
* Custom dataset
* I made my own dataset. Later on try changing the data and re-training the model to see the grave impact data has on a DL model.
![](https://github.com/AparGarg99/RPSGame/blob/master/images/dataset.PNG)

### ✔️Methodology


1. **Split** - 
![](https://github.com/AparGarg99/RPSGame/blob/master/images/split.PNG)
2. The pipeline.config file cotains the pipeline followed.<br>
&nbsp;2.1. **Augmentation** - 
![](https://github.com/AparGarg99/RPSGame/blob/master/images/augment.PNG)
<br>
&nbsp;2.2. **Preprocessing** - Images were resized to 320x320 pixel squares.<br>
&nbsp;2.3. **Model Development** - Transfer Learning was performed on [ssd_mobilenet_v2_fpnlite_320x320_coco17_tpu-8]() model


### ✔️Results
After training the model for 20 epochs, final training and validation set losses were 1.19 and 1.16 respectively.

***Note:***
* *The training stopped pre-maturely and may have improved with more epochs. But due to memory limitation in Google Colab, epochs were set to 20.*
* *I did not perform testing on the test set because of huge time and memory complexity. Instead, I performed inference on random test images.*

### ✔️Future Work
I have several ideas to improve this project:
* Train other popular CNN networks like VGG and Inception --> Present a real-time comparison-based study on the app when a user gives an image.
* Check predicted confidence --> Say something about not being sure about the prediction if it is under some threshold.
* Add functionality of performing image processing in the app using OpenCV (check out my [project](https://github.com/AparGarg99/Tutorials/tree/master/streamlit_frontend_tutorial/app7_opencv_tutorial)) --> Users can analyze in real-time how transforming an image affects the prediction.
---
---

# GUI 👨‍💻
![trim](https://user-images.githubusercontent.com/54896849/119932196-6e3b8880-bfa0-11eb-8c26-1c0f32bd98ce.gif)

---
---
# Installation and Usage 🔌
[Click Here](https://github.com/AparGarg99/Tutorials/blob/master/streamlit_frontend_tutorial/README.md#installation-and-usage) for reference.

<br>
<br>

***Dont forget to give a ⭐ if you like this project !!***
