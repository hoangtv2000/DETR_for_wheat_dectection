# DETR 
Welcome to our Computer Vision project.

**Abstract.** In this work, we introduce the panoptic segmentation problem of image, its evaluation metric, and provide the 2020 SOTA Detection Transformer (DETR) as the optimal solution. Then explain explicitly how does DETR performs object detection: the Transformer architecture, the process of extracted image's feature transformation to Transformer's digestible form, the queries for questioning detected object and the loss computation, also the optimization algorithm. In order to deploy panoptic segmentation, the panoptic head is added to notice each detected object and render the segmentation version of image. Finally, we clarify its powerful properties by implement [COCO-2017](https://cocodataset.org/index.htm#download) pretrained model and apply it to solve [Wheat Head detection problem](https://www.kaggle.com/c/global-wheat-detection).

**Keywords**: detection, segmentation, detr, global-wheat-detection.

:star: For the detail of our report, see [Approaching Object detection and Panoptic segmenation problem by DETR](https://github.com/thoconvuive/DETR/blob/main/DETR.pdf).

:star: Slide of report can be found [here](https://drive.google.com/file/d/1GRagZq1G4-X24gwfjzzKmQBQL7_D4S6S/view?usp=sharing).

:star: We add the code-only version of [Wheat head dataset EDA](https://github.com/hoangtv2000/DETR_for_wheat_dectection/blob/main/wheat_head_EDA.ipynb). You can try yourself by running the script. 


# Notebooks
+ For the implementation of COCO-2017 pretrained model. We install and demonstrate its performance by plotting the prediction (included visualization of attention mechanism). The work can be found at [Implement pretrained DETR for object detection and panoptic segmentation](https://github.com/thoconvuive/DETR/blob/main/Implement%20pretrained%20DETR%20for%20object%20detection%20and%20panoptic%20segmentation.ipynb)  

+ We train the pre-trained DETR model to get a prediction of wheat in Wheat Head dataset. This is a really hard problem, our training model have a acceptable result. See [Implement DETR for Wheat detection](https://github.com/thoconvuive/DETR/blob/main/Implement%20DETR%20for%20Wheat%20detection.ipynb) for full detail.

**Update** : We add [hand-craft annotation](https://github.com/thoconvuive/DETR/blob/main/_annotations.csv) of the test images, build an mAP evaluation metric and test on it.


## Result

**Object detection of wheat in Wheat Head dataset**

<p float="left">
  <img src="https://github.com/hoangtv2000/DETR_for_wheat_dectection/blob/main/results/res1.jpg" />
  <img src="https://github.com/hoangtv2000/DETR_for_wheat_dectection/blob/main/results/res2.jpg" /> 
  <img src="https://github.com/hoangtv2000/DETR_for_wheat_dectection/blob/main/results/res3.jpg" width="273" />
</p>

**Our mAP scores**

|No. image| AP       |No. image| AP   |
|-------- |----------|---------|------|
|1        | 0.3125   |6        |0.1363|
|2        | 0.4195   |7        |0.4545|
|3        | 0.4394   |8        |0.4695|
|4        | 0.5397   |9        |0.5121|
|5        | 0.1735   |10       |0.3123|
|**mAP**  | **0.3769**              |||
