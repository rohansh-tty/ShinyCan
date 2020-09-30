# S13 Assignment

**Yolo 2 & 3**


Assignment Task: 

    OpenCV Yolo: SOURCE (Links to an external site.)
        Run this above code on your laptop or Colab. 
        Take an image of yourself, holding another object which is there in COCO data set (search for COCO classes to learn). 
        Run this image through the code above. 
        Upload the link to GitHub implementation of this
        Upload the annotated image by YOLO. 
    Training Custom Dataset on Colab for YoloV3
        Refer to this Colab File: LINK (Links to an external site.)
        Refer to this GitHub Repo (Links to an external site.)
        Collect a dataset of 500 images and annotate them. Please select a class for which you can find a YouTube video as well. Steps are explained in the readme.md file on GitHub.
        Once done:
            Download (Links to an external site.) a very small (~10-30sec) video from youtube which shows your class. 
            Use ffmpeg (Links to an external site.) to extract frames from the video. 
            Upload on your drive (alternatively you could be doing all of this on your drive to save upload time)
            Inter on these images using detect.py file. **Modify** detect.py file if your file names do not match the ones mentioned on GitHub. 
            `python detect.py --conf-thres 0.3 --output output_folder_name`
            Use ffmpeg (Links to an external site.) to convert the files in your output folder to video
            Upload the video to YouTube. 
        Share the link to your GitHub project with the steps as mentioned above
        Share the link of your YouTube video
        Share the link of your YouTube video on LinkedIn, Instagram, etc! You have no idea how much you'd love people complimenting you! 

# ASSIGNMENT A
![Notebook Link](https://github.com/Gilf641/EVA4/blob/master/S13/Assignment-A/S13%20Assignment-A.ipynb)


* **IMPLEMENTATION**
1. Ran the OpenCV-Yolo Colab Notebook
2. Uploaded a couple of images with me holding a some COCO Objects and tested the same


* Sample Image

![](https://github.com/Gilf641/EVA4/blob/master/S13/Assignment-A/Images/OpenCV-Yolo1.png)





# ASSIGNMENT B
![Repo Link](https://github.com/Gilf641/YoloV3)


![Notebook_Link](https://github.com/Gilf641/EVA4/blob/master/S13/Assignment-B/S13%20Assignment-B.ipynb)

---------

* **MOTIVATION**

Waste Segregator Robo, which classifies and seperates Recyclable, Non Recyclable Waste Materials and dump them into respective Bins.
For example I have collected/got dataset from few GitHub repos and planning to build this project.

* **IMPLEMENTATION**
>(Check ![this Colab Notebook](https://github.com/Gilf641/EVA4/blob/master/S13/Assignment-B/S13%20Assignment-B.ipynb) for Step-By-Step Process.)
1. For S13 B, I have Metal Cans as my class. Dataset includes Metal Cans, Caps, Aluminium Foils etc. Collected around 300-400 Images from this repo, rest from the Internet.
2. Used ![this](https://github.com/miki998/YoloV3_Annotation_Tool) for Annotation.
3. Ran for 110 Epochs. 


* **SAMPLES**


**1. Train Data**
![](https://github.com/Gilf641/EVA4/blob/master/S13/Assignment-B/Images/train_batch0.png)

**2. Test Data**
![](https://github.com/Gilf641/EVA4/blob/master/S13/Assignment-B/Images/test_batch0.png)


**RESULTS**

![](https://github.com/Gilf641/EVA4/blob/master/S13/Assignment-B/Images/Output.jpg)


# Model Logs

Model Summary: 225 layers, 6.25733e+07 parameters, 6.25733e+07 gradients
Caching labels (510 found, 0 missing, 0 empty, 0 duplicate, for 510 images): 100% 510/510 [00:00<00:00, 9034.83it/s]
Caching images (0.3GB): 100% 510/510 [00:01<00:00, 464.56it/s]
Caching labels (510 found, 0 missing, 0 empty, 0 duplicate, for 510 images): 100% 510/510 [00:00<00:00, 10415.30it/s]
Caching images (0.3GB): 100% 510/510 [00:01<00:00, 457.72it/s]
Image sizes 512 - 512 train, 512 test
Using 2 dataloader workers
Starting training for 160 epochs...

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
     0/159     9.16G      4.01      3.68         0      7.69        11       512: 100% 43/43 [00:57<00:00,  1.34s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:18<00:00,  2.29it/s]
                 all       510       519         0         0     0.345         0

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
     1/159     9.17G      3.11      1.94         0      5.05        16       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:14<00:00,  3.05it/s]
                 all       510       519      0.29     0.886     0.478     0.437

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
     2/159     9.17G      2.94      1.22         0      4.16        15       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.27it/s]
                 all       510       519      0.34     0.879     0.415      0.49

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
     3/159     9.17G      2.39     0.918         0      3.31        10       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.25it/s]
                 all       510       519     0.284     0.906     0.328     0.433

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
     4/159     9.17G      2.29     0.816         0       3.1        12       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.26it/s]
                 all       510       519     0.828     0.952     0.943     0.886

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
     5/159     9.17G      2.19     0.759         0      2.95        14       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.27it/s]
                 all       510       519    0.0831     0.956     0.135     0.153

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
     6/159     9.17G      1.94     0.772         0      2.71         9       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.25it/s]
                 all       510       519    0.0302     0.884    0.0702    0.0584

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
     7/159     9.17G      1.78     0.727         0      2.51        16       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.27it/s]
                 all       510       519     0.851     0.965     0.971     0.905

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
     8/159     9.17G      1.96     0.713         0      2.67        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.951     0.967     0.977     0.959

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
     9/159     9.17G      1.56     0.726         0      2.29        12       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.941     0.934     0.965     0.938

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    10/159     9.17G      1.79     0.714         0       2.5        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.912     0.919     0.962     0.916

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    11/159     9.17G      1.84     0.678         0      2.52        25       512:  63% 27/43 [00:35<00:21,  1.32s/it]
Model Bias Summary:    layer        regression        objectness    classification
                          89      -0.02+/-0.22      -4.99+/-0.90       4.11+/-0.01 
                         101       0.18+/-0.27      -6.49+/-0.31       4.13+/-0.00 
                         113       0.01+/-0.10      -6.04+/-0.36       4.09+/-0.01 
    11/159     9.17G      1.66     0.683         0      2.35        16       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.901     0.971     0.971     0.935

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    12/159     9.17G      1.33     0.675         0      2.01        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.27it/s]
                 all       510       519      0.84      0.94      0.95     0.887

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    13/159     9.17G      1.51      0.68         0      2.19        15       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.964     0.917      0.96      0.94

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    14/159     9.17G      1.33     0.586         0      1.91        10       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.937     0.828     0.933     0.879

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    15/159     9.17G      1.45     0.619         0      2.07        13       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.937     0.923     0.957      0.93

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    16/159     9.17G      1.42     0.649         0      2.07        17       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519      0.91     0.965     0.976     0.937

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    17/159     9.17G      1.24     0.617         0      1.86        12       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.956     0.969     0.988     0.962

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    18/159     9.17G      1.49     0.621         0      2.11        10       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.974     0.963     0.991     0.968

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    19/159     9.17G      1.16     0.606         0      1.76        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.951     0.967     0.988     0.959

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    20/159     9.17G      1.15     0.627         0      1.78        13       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.963     0.985     0.992     0.974

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    21/159     9.17G      1.08     0.555         0      1.63        12       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.973     0.955     0.983     0.964

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    22/159     9.17G      1.08     0.547         0      1.63        10       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.975     0.982     0.993     0.979

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    23/159     9.17G      1.12     0.556         0      1.67         9       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.969     0.985     0.993     0.977

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    24/159     9.17G      1.25     0.554         0      1.81        10       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.975     0.983     0.993     0.979

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    25/159     9.17G      1.05     0.545         0      1.59        12       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.972     0.985     0.993     0.978

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    26/159     9.17G      1.09     0.574         0      1.67        10       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.968     0.994     0.994     0.981

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    27/159     9.17G      1.01     0.557         0      1.56        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.983     0.988     0.994     0.986

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    28/159     9.17G       1.5     0.546         0      2.05        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.975     0.969     0.992     0.972

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    29/159     9.17G      1.06     0.513         0      1.57        10       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.976     0.954     0.991     0.965

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    30/159     9.17G     0.988     0.539         0      1.53        10       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.975     0.965     0.982      0.97

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    31/159     9.17G         1     0.541         0      1.54         8       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.977     0.972     0.992     0.974

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    32/159     9.17G     0.958     0.533         0      1.49        12       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.26it/s]
                 all       510       519     0.981     0.963      0.99     0.972

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    33/159     9.17G     0.973     0.517         0      1.49         8       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.977     0.985     0.992     0.981

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    34/159     9.17G     0.974     0.536         0      1.51        12       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519      0.98     0.966     0.993     0.973

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    35/159     9.17G     0.926     0.528         0      1.45        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.971     0.974     0.992     0.973

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    36/159     9.17G     0.887     0.519         0      1.41        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.983     0.976     0.994     0.979

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    37/159     9.17G      1.15     0.518         0      1.67        10       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.27it/s]
                 all       510       519     0.986     0.988     0.994     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    38/159     9.17G     0.995     0.521         0      1.52        12       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.983     0.979     0.994     0.981

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    39/159     9.17G      1.05     0.521         0      1.57        14       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.988     0.973     0.991      0.98

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    40/159     9.17G     0.908     0.474         0      1.38        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.27it/s]
                 all       510       519     0.987     0.975     0.991     0.981

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    41/159     9.17G      1.01     0.535         0      1.55        13       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.987     0.985     0.993     0.986

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    42/159     9.17G     0.856     0.479         0      1.34        12       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.26it/s]
                 all       510       519     0.985     0.975     0.991      0.98

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    43/159     9.17G     0.837     0.489         0      1.33        10       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.982      0.97     0.989     0.976

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    44/159     9.17G       1.1     0.469         0      1.57        16       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.988     0.981     0.991     0.985

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    45/159     9.17G     0.927     0.485         0      1.41        12       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.26it/s]
                 all       510       519     0.979     0.978     0.993     0.978

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    46/159     9.17G     0.851       0.5         0      1.35        10       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.983     0.979     0.994     0.981

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    47/159     9.17G      1.01     0.489         0       1.5        14       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.27it/s]
                 all       510       519     0.978     0.988     0.993     0.983

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    48/159     9.17G      1.13     0.503         0      1.64        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.27it/s]
                 all       510       519     0.978     0.994     0.993     0.986

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    49/159     9.17G     0.887     0.456         0      1.34        13       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.25it/s]
                 all       510       519     0.983     0.983     0.993     0.983

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    50/159     9.17G     0.821     0.473         0      1.29        14       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.984     0.975     0.993      0.98

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    51/159     9.17G      1.12     0.483         0       1.6        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.26it/s]
                 all       510       519     0.986     0.985     0.994     0.985

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    52/159     9.17G      1.18      0.46         0      1.64        12       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.27it/s]
                 all       510       519     0.988     0.976     0.994     0.982

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    53/159     9.17G     0.904      0.46         0      1.36        12       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.985     0.967     0.992     0.976

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    54/159     9.17G     0.852     0.477         0      1.33        12       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.984     0.976     0.994      0.98

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    55/159     9.17G     0.805     0.489         0      1.29        15       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.31it/s]
                 all       510       519     0.982     0.975     0.994     0.978

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    56/159     9.17G      1.07     0.513         0      1.59        14       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.989     0.961     0.993     0.975

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    57/159     9.17G     0.843     0.458         0       1.3        13       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.982     0.972     0.994     0.977

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    58/159     9.17G     0.939     0.469         0      1.41        15       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.27it/s]
                 all       510       519     0.983     0.981     0.995     0.982

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    59/159     9.17G     0.826     0.458         0      1.28        15       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519      0.99     0.985     0.994     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    60/159     9.17G     0.924     0.463         0      1.39        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.981     0.987     0.994     0.984

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    61/159     9.17G     0.833     0.444         0      1.28        10       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.979     0.985     0.994     0.982

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    62/159     9.17G     0.835     0.479         0      1.31        13       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.987     0.987     0.993     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    63/159     9.17G     0.838     0.481         0      1.32        14       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.987     0.988     0.994     0.988

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    64/159     9.17G     0.803     0.498         0       1.3        12       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.988     0.983     0.993     0.986

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    65/159     9.17G     0.791     0.451         0      1.24        15       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.989     0.994     0.994     0.991

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    66/159     9.17G     0.896     0.456         0      1.35        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.986     0.992     0.994     0.989

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    67/159     9.17G     0.811     0.466         0      1.28        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.986     0.988     0.994     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    68/159     9.17G     0.682     0.467         0      1.15        13       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.987     0.988     0.994     0.988

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    69/159     9.17G     0.671     0.434         0      1.11        12       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519      0.99     0.983     0.994     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    70/159     9.17G      0.77     0.414         0      1.18        12       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.994     0.977     0.994     0.985

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    71/159     9.17G     0.775     0.433         0      1.21        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519      0.99     0.983     0.994     0.986

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    72/159     9.17G     0.841     0.413         0      1.25        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.988     0.985     0.995     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    73/159     9.17G     0.809     0.418         0      1.23        16       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.988     0.985     0.994     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    74/159     9.17G     0.778     0.416         0      1.19        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519      0.99     0.979     0.994     0.984

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    75/159     9.17G     0.958     0.439         0       1.4        10       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519      0.99     0.986     0.995     0.988

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    76/159     9.17G     0.894     0.442         0      1.34         9       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.992      0.97     0.991     0.981

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    77/159     9.17G     0.613     0.403         0      1.02        10       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.994     0.979     0.985     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    78/159     9.17G     0.757     0.396         0      1.15        10       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.992     0.981     0.994     0.986

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    79/159     9.17G     0.656     0.405         0      1.06        14       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.998     0.987     0.994     0.992

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    80/159     9.17G     0.766      0.42         0      1.19        13       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.996     0.979     0.994     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    81/159     9.17G     0.637     0.424         0      1.06        14       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.995     0.975     0.991     0.985

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    82/159     9.17G     0.629      0.42         0      1.05        13       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.992     0.973     0.984     0.982

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    83/159     9.17G     0.628     0.408         0      1.04        16       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.993     0.975     0.991     0.984

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    84/159     9.17G     0.607     0.388         0     0.996         9       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.993     0.981     0.993     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    85/159     9.17G     0.596     0.379         0     0.974        10       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.998      0.98     0.995     0.989

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    86/159     9.17G     0.643     0.418         0      1.06         8       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519      0.99     0.976     0.993     0.983

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    87/159     9.17G     0.598     0.397         0     0.994        12       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.984     0.979     0.989     0.982

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    88/159     9.17G     0.632     0.397         0      1.03         9       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.986     0.977      0.99     0.982

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    89/159     9.17G     0.629     0.366         0     0.995        13       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519      0.99     0.981     0.994     0.986

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    90/159     9.17G     0.666     0.376         0      1.04        10       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519      0.99     0.983     0.994     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    91/159     9.17G     0.669     0.398         0      1.07        14       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.994      0.98     0.993     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    92/159     9.17G      0.57     0.392         0     0.962         9       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.994     0.985     0.993     0.989

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    93/159     9.17G     0.548     0.362         0      0.91        14       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.992     0.987     0.993     0.989

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    94/159     9.17G     0.547     0.382         0      0.93        13       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.994     0.983     0.994     0.988

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    95/159     9.17G     0.622     0.363         0     0.985        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.996     0.977     0.994     0.986

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    96/159     9.17G     0.659     0.364         0      1.02        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.994     0.971     0.994     0.982

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    97/159     9.17G     0.551     0.377         0     0.928        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.994     0.972     0.994     0.983

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    98/159     9.17G     0.627     0.358         0     0.985        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.995     0.983     0.995     0.989

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
    99/159     9.17G     0.612     0.368         0      0.98        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.992     0.982     0.995     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
   100/159     9.17G     0.696     0.394         0      1.09        13       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.994     0.981     0.992     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
   101/159     9.17G     0.616     0.372         0     0.988         9       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.994     0.983     0.994     0.989

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
   102/159     9.17G      0.59     0.363         0     0.953        11       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.995     0.981     0.994     0.988

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
   103/159     9.17G     0.609     0.362         0     0.971        13       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.993     0.979     0.991     0.986

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
   104/159     9.17G     0.503     0.333         0     0.835        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.995     0.981     0.993     0.988

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
   105/159     9.17G     0.565      0.35         0     0.915         9       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.992      0.98     0.984     0.986

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
   106/159     9.17G     0.651     0.348         0     0.999        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.28it/s]
                 all       510       519     0.992     0.976     0.984     0.984

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
   107/159     9.17G      0.47      0.36         0      0.83        13       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.994     0.979     0.984     0.987

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
   108/159     9.17G     0.517     0.349         0     0.867        12       512: 100% 43/43 [00:56<00:00,  1.31s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519     0.993     0.979     0.984     0.986

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
   109/159     9.17G     0.652     0.344         0     0.995        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.30it/s]
                 all       510       519     0.992     0.979     0.984     0.985

     Epoch   gpu_mem      GIoU       obj       cls     total   targets  img_size
   110/159     9.17G      0.56     0.315         0     0.875        11       512: 100% 43/43 [00:56<00:00,  1.32s/it]
               Class    Images   Targets         P         R   mAP@0.5        F1: 100% 43/43 [00:13<00:00,  3.29it/s]
                 all       510       519      0.99     0.975     0.984     0.983




