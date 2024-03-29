# [DukeMTMC-reID/DukeMTMC4ReID](http://vision.cs.duke.edu/DukeMTMC/)

The DukeMTMC dataset is a large-scale heavily labeled multi-target multi-camera tracking dataset. In total, more than 2700 people were labeled with unique identities in 8 cameras. With the access to all information (full frames, frame level ground truth, calibration information, etc.), this dataset has a lot of protentials. Based on the released train-validation set, two re-id extension datasets are created. The key difference is the way to generate the bounding boxes. DukeMTMC-reID directly uses the manually labeled ground truth whereas DukeMTMC4ReID adopts Doppia as the person detector.

# 简介

原始数据集包含了85分钟的高分辨率视频，采集自8个不同的摄像头。并且提供了人工标注的bounding box 该数据集一共 36,411张图像。其中有1,404个人出现在大于两个摄像头下，有408个人只出现在一个摄像头下。

随机采样了 702 个人作为**训练集**，702个人作为**测试集**。在**测试集中**，我们采样了**每个ID的每个摄像头下的一张照片**作为查询图像（**query**）。剩下的图像加入测试的搜索库（gallery），并且将之前的 408人作为干扰项，也加到 gallery中。最终，**训练集中，**DukeMTMC-reID 包含了 16,522张训练图片（来自702个人），**测试集中**： 2,228个查询图像（来自另外的702个人），以及 17,661 张图像的搜索库（gallery）。并提供切割后的图像供下载。

另外，DukeMTMC-reID还提供了23种属性数据标注 DukeMTMC-attribute供下载。 https://github.com/vana77/DukeMTMC-attribute

## 目录结构

DukeMTMC-reID
　　├── bounding_box_test
　　　　　　　├── 0002_c1_f0044158.jpg
　　　　　　　├── 3761_c6_f0183709.jpg
　　　　　　　├── 7139_c2_f0160815.jpg
　　├── bounding_box_train
　　　　　　　├── 0001_c2_f0046182.jpg
　　　　　　　├── 0008_c3_f0026318.jpg
　　　　　　　├── 7140_c4_f0175988.jpg
　　├── query
　　　　　　　├── 0005_c2_f0046985.jpg
　　　　　　　├── 0023_c4_f0031504.jpg
　　　　　　　├── 7139_c2_f0160575.jpg
　　└── CITATION_DukeMTMC.txt
　　└── CITATION_DukeMTMC-reID.txt
　　└── LICENSE_DukeMTMC.txt
　　└── LICENSE_DukeMTMC-reID.txt
　　└── README.md

## 目录介绍

从视频中每 120 帧采样一张图像，得到了 36,411 张图像。一共有 1,404 个人出现在大于两个摄像头下，有 408 个人 (distractor ID) 只出现在一个摄像头下。

1） “bounding_box_test”——用于测试集的 702 人，包含 17,661 张图像（随机采样，702 ID + 408 distractor ID）

2） “bounding_box_train”——用于训练集的 702 人，包含 16,522 张图像（随机采样）

3） “query”——为测试集中的 702 人在每个摄像头中随机选择一张图像作为 query，共有 2,228 张图像

## 命名规则

以 0001_c2_f0046182.jpg 为例

1） 0001 表示每个人的标签编号；

2） c2 表示来自第二个摄像头(camera2)，共有 8 个摄像头；

3） f0046182 表示来自第二个摄像头的第 46182 帧。

## 数据分布

DukeMTMC-reID训练集的图像分布。我们注意到每个ID的图像中值为20。但有些ID可能包含大量图像，这可能会影响某些算法。(例如，ID 5388包含426个图像。)


#### DukeMTMC-reID

![img](imgs/eg_DukeMTMC-reID.jpg)

> Zheng, Zhedong, Liang Zheng, and Yi Yang. ["Unlabeled samples generated by gan improve the person re-identification baseline in vitro."](https://arxiv.org/pdf/1701.07717.pdf) arXiv preprint arXiv:1701.07717 (2017).

#### DukeMTMC4ReID

![img](imgs/eg_DukeMTMC4ReID.jpg)

> Gou, Mengran and Karanam, Srikrishna and Liu, Wenqian and Camps, Octavia and Radke, Richard J. "[DukeMTMC4ReID: A Large-Scale Multi-Camera Person Re-Identification Dataset](http://robustsystems.coe.neu.edu/sites/robustsystems.coe.neu.edu/files/systems/papers/MengranGou_CVPRW17.pdf)." CVPR Workshops (2017)

