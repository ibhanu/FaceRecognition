# Face Recognition System

A facial recognition system is a technology capable of identifying or verifying a person from a digital image or a video frame from a video source. There are multiple methods in which facial recognition systems work, but in general, they work by comparing selected facial features from the given image with faces within a database. It is also described as a Biometric Artificial Intelligence based application that can uniquely identify a person by analyzing patterns based on the person's facial textures and shape.

## Prerequisites

Install these packages to make sure you can run the program without any errors.

```bash
sudo apt install python3-opencv
pip3 install opencv-contrib-python numpy
```

## How to run the program
1. Clone the repo into your local system and change directory
```bash
git clone https://github.com/ibhanu/FaceRecognition.git
cd FaceRecognition
```
2. Make a folder named as 'train-images' where you will store images to train.
```bash
mkdir train-images
```
3. Make 1 or Multiple folders under train-images folder named 0,1,2 and so on to store the images of different people you want to recognize. 
- For every person's images, different folders will be used. For example for person A, his images will be stored in a folder named as 0
and images of Person B, his images will be stored in the folder named as 1 and so on.

4. Open faceRecognition.py and give the path to haar classifier as I have given in faceDetection function.
### Create your dataset
5. Now open Create_dataset_from_webcam.py to capture images from your webcam if you want to create a dataset for your own images. It will click multiple images from webcam till you end this program. 
Make sure it clicks at least 300 images before you end the program. Do the required configuration as I have mentioned in comments.
```bash
python3 Create_dataset_from_webcam.py
```
- Your images will be stored at train-images/0/ folder
- Now at train-images/1/ folder, you can store images of any other person you want to recognize.

### Train your model using haar cascade classifier
6. Now open train_model.py to train your model to recognize whoever faces you want. Do the required configuration.
- You have to take sample photos and save it in the root folder as 1.jpg just to check if the model is trained.
- In train_model.py, If you want to recognize only one person then write:- name={0:"name"} that's all. Don't write for id number 1.
```bash
python3 train_model.py
```
7. Now your training will get done and trainingData.yml file will be saved.

### Load Model to recognize faces from images and video.
8. open load_model_image.py to recognize a face from an image and open load_model_video.py to recognize a face from a video or webcam. Do the required configurations.
```bash
python3 load_model_image.py
python3 load_model_video.py
```
## That's it.

### If you have any problem regarding the project or queries 
mail me pratap.bhanu3434@gmail.com
or message me on instagram @itsbhanupratap
