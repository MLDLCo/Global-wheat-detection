
# Global-wheat-detection

Global wheat detection using YOLOv2 in Keras.

This is a Keras implementation of YOLOV2 for Kaggle Competition [https://www.kaggle.com/c/global-wheat-detection/](https://www.kaggle.com/c/global-wheat-detection/)

## Setup
* Run the command to install all required packages
``` pip install -r requirements.txt ```

## Train

### 1. Data preparation

Download the Global-wheat-detection dataset from from  [https://www.kaggle.com/c/global-wheat-detection/](https://www.kaggle.com/c/global-wheat-detection/).

Organize the dataset into 4 folders:

-   train_image_folder <= the folder that contains the train images.
    
-   train_annot_folder <= the folder that contains the train annotations in VOC format.
    
-   valid_image_folder <= the folder that contains the validation images.
    
-   valid_annot_folder <= the folder that contains the validation annotations in VOC format.
    

There is a one-to-one correspondence by file name between images and annotations. If the validation set is empty, the training set will be automatically splitted into the training set and validation set using the ratio of 0.8.

### 2. Convert Bounding box into VOC format for training
Run the jupyter notebook **preproc.ipynb** to create VOC format xml files.

### 3. Download the Yolov2 weights
Download the yolov2 weights from [https://pjreddie.com/darknet/yolov2/](https://pjreddie.com/darknet/yolov2/) and save it in model_weights folder. Here we are using transfer learning to train wheat detection model. 

### 4. Train
Use the **train.ipynb** to train the model.

### 5. Inference
Use the **Inference.ipynb** for prediction on test dataset.

## Refereneces
* [https://github.com/experiencor/keras-yolo2](https://github.com/experiencor/keras-yolo2)
* [https://www.kaggle.com/c/global-wheat-detection/](https://www.kaggle.com/c/global-wheat-detection/)
* [https://pjreddie.com/darknet/yolov2/](https://pjreddie.com/darknet/yolov2/)
