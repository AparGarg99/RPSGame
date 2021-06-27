# Overview 📚
### ✔️Abstract
A rock-paper-scissors game using live video feed from the camera. Transfer learning was used to fine-tune the SSD_mobilenet_v2 pre-trained object detection model to learn how to classify and localize 3 hand gestures. 
OpenCV library was used for all camera related operations.

### ✔️Dataset
* Custom dataset
* I made my own dataset. Later on try changing the data and re-training the model to see the grave impact data has on a DL model.
![](https://github.com/AparGarg99/RPSGame/blob/master/images/dataset.PNG)

### ✔️Methodology

I used [fastai v1](https://github.com/fastai/fastai) for transforming images and training the DL network.*

1. **Split** - 101000 images were split into train, validation and test set. Train = 60600, Validation = 15150, Test = 25250.
2. **Augmentation** - Fastai has a method called [get_transforms()](https://fastai1.fast.ai/vision.transform.html#get_transforms) for augmenting images. It returns a tuple of two lists of transforms: one for the training set and one for the validation set. The first list of transforms applies default and random transformations with a probability of 75%: crop, horizontal flip, zoom up to 1.1, brightness and contrast, wrap (perspective). The second list of transforms is limited to resizing the pictures since we don't want to modify the images in the validation set.
3. **Preprocessing** - First, the images were resized to 224x224 pixel squares and then they were normalized (using [normalize()](https://fastai1.fast.ai/vision.data.html#ImageDataBunch.normalize) method in fastai).
4. **Model Development** - I performed transfer learning on ResNet34 (Deep CNN network). The model was trained on a GPU in [Google Colab](https://colab.research.google.com
).

Then I created an app using [Streamlit](https://streamlit.io/) to showcase this project. The app allows users to interact with the trained model without any need for coding. Users can enter the image address/URL from the internet or upload their own image and see how the model would classify it. The app outputs the following 3 things: (i) Predicted food class. (ii) Link to the [Wikipedia](https://www.wikipedia.org/) page of the predicted food class. (iii) Link to the [Google Images](https://www.google.com/imghp?hl=EN) page of the predicted food class.

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
