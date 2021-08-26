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

