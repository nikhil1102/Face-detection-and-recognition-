# Face detection and recognition 
# Introduction

Computer vision is a field of informatics, which teaches computers to see. It is a way computers gather and interpret visual information from the surrounding environment. The feature invariant approaches are used for feature detection of eyes, mouth, ears, nose, etc. In recent years, face recognition has attracted much attention and its research has rapidly expanded by not only engineers but also neuroscientists since it has many potential applications in computer vision communication and automatic access control system.

Especially, face detection is an important part of face recognition as the first step of automatic face recognition. However, face detection is not straightforward because it has lots of variations of image appearance, such as pose variations like the front, non-front, occlusion, image orientation, illuminating condition, and facial expression. For example, the template-matching methods are used for face localization and detection by computing the correlation of an input image to a standard face pattern. The feature invariant approaches are used for feature detection of eyes, mouth, ears, nose, etc. This project presents a face detection technique mainly based on color segmentation, image segmentation and template matching methods. The implementation is on the Haar-cascade algorithm to detect the face from the given image dataset loaded by the user.

# Project Discription
For this project, a more sophisticated method is therefore required. One such method would be the detection of objects from images using features or specific structures of the object in question. However, there was a problem. Working with only image intensities, meaning the RGB pixel values in every single pixel in the image, made feature calculation rather computationally expensive and therefore slow on most platforms.

This problem was addressed by the so-called Haar-like features, which is a trained cascade Due to its efficiency, Haar-like rectangle features have become a popular choice as image features in the context off detection. We compare our rectangular features with Haar-like features. Haar-like features are attributes extracted from images used in pattern recognition. Their name comes from their similarity to Haar wavelets. First, the pixel values inside the black area are added together; then the values in the white area are summed, Then the total value of the white area is subtracted from the total value of the black area. This result is used to categorize image sub-regions.

# Face Recognition
Step1: Creating a dataset
 Dataset generator is going to capture few sample faces of one person from the live video frame and assign a ID to it and it will save those samples in a folder which we are going to create now and we will name it dataset
So we create a folder named dataSet in the same location where you have saved your .py script We are going to follow this naming convention for the sample images to make sure they dont mixed up with other person’s image samples

Step2: Training the dataset
 we will are going to create a function which will grab the training images from the dataset folder, and will also get the corresponding Ids from its file name the function “getImagesAndLabels”   need the path of the dataset folder so we will provide the folder path as argument. inside this function we are going to do the following

1. Load the training images from dataset folder
2. capture the faces and Id from the training images
3. Put them In a List of Ids and Face Samples  and return it
4. create a recognizer object using opencv library and load the training data

Step3: Recognize the database
The main loop in the recognition does the following basic steps 
1. Starts capturing frames from the camera object
2. Convert it to Gray Scale
3. Detect and extract faces from the images
4. Use the recognizer to recognize the Id of the user
5. Put predicted Id/Name and Rectangle on detected face
