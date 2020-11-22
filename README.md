# Fashion-Detection-Brainhack2020
Object Detection of Fashion Items for BrainHack 2020 Qualifier Stage by DSTA
This was WASD++'s attempt for the finals of the [DSTA BrainHack 2020](https://www.dsta.gov.sg/brainhack)

Contributors: Daryl Lee, Ming Chong, Alvin, Wei Xiong, Kang Liang and Si Yu (me!)

## Objective
We were given images of people wearing certain types of fashion items (tops, trousers, outerwear, dresses and skirts) as well as bounding boxes for the different categories. We needed to train an object detection model for this.
## Methodology
### Data Preprocessing
We used the typical image preprocessing techniques such as shearing, brightness, horizontal flipping, etc.
Something interesting that I tried using was the [albumentations](https://github.com/albumentations-team/albumentations) library. 

### Model Training
We trained a couple of object detection models, mainly:
1. [EfficientDet Pytorch Implementation](efficientdet_pytorch.ipynb)
2. [EfficientDet Tensorflow Implementation](efficientdet.ipynb)
3. [RetinaNet](Retinanet.ipynb)
4. [Yolov4](yolov4.ipynb)
5. [Yolov5](yolov5.ipynb)
We made some edits on top of those forked repositories to fit to our use case.

### Ensemble
We used a novel method to ensemble the models by doing weight fusion on the bounding boxes that each of the models outputted. This method was from this research paper. https://arxiv.org/pdf/1910.13302.pdf
