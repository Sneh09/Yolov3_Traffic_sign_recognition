# Yolov3_Traffic_sign_recognition

This is a YOLOv3 model that can detect 200 traffic sign categories using DFG dataset trained on Google Colab.

## DFG Dataset:

* 5254 training images and 1703 testing images
* 6758 images with 1920x1080 resolution
* 199 images with 720x576 resolution
* The images have been anonymized by blurring the faces and vehicle license plates to comply with the EU GDPR legislation.
* 13239 tightly annotated (polygon) traffic sign instances larger than 30 px.
* 4359 loosely annotated (bounding box) traffic sign instances smaller than 30 px marked as ignore.
* 200 traffic sign categories with at least 20 instances per category.
* roughly 70% of categories with a low appearance changes and 30% with a large appearance variability.
* Annotation format:  COCO json format

## Reference from :
* Dataset Link : https://www.vicos.si/resources/dfg/

## Steps to build :

1. Download the dataset and unzip the images.
2. Change the annotation format from COCO json to YOLO txt format using the coco2yolo.py.
3. Create a new folder Yolo_custom_model_training on Google drive and custom_data folder inside and unzip all the images and annotation files.
4. In custom data add classes.names and classes.txt files.
5. Refer github.com/qqwweee/keras-yolo3 to generate anchor boxes for custom_data on Anaconda.
6. Clone the Yolov3 darknet repository. Configure the Makefile to enable training on GPU.
7. Change the yolov3 config file after cloning the darknet. (Make changes in anchor boxes as well if generated using step 4.)
8. Start the training process.
9. To get mAP in the chart.png along with loss use -map tag.

## Test the model performance :
1. Once the training is done predict the results. (images or video file as per your choice)
2. You can even calculate the FPS using -benchmark flag.
3. To train and test the code directly using Google Colab refer yolov3_tsr.ipynb.

## Final Output :

![predictions (1)](https://user-images.githubusercontent.com/87853074/131008508-58949c3b-a0cc-471f-b185-fd695ec73ba3.jpg)
