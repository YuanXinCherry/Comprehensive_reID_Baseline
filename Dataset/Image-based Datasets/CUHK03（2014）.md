# [CUHK03](http://www.ee.cuhk.edu.hk/~xgwang/CUHK_identification.html)

CUHK03 is the first person re-identification dataset that is large enough for deep learning. It provides the bounding boxes detected from deformable part models (DPM) and manually labeling. Person detection quality is relatively good for this dataset.

# 简介

CUHK03是第一个足以进行深度学习的重新识别数据集。它提供从 Deformable Part Model （DPM）检测到的边界框和手动标记。对于该数据集，人物检测质量相对较好。

1467 个身份，13164个图像，手动裁剪+自动检测

## 目录结构

CUHK-03
　　├── “detected”── 5 x 1 cell
　　　　　　　├── 843x10 cell
　　　　　　　├── 440x10 cell
　　　　　　　├── 77x10 cell
　　　　　　　├── 58x10 cell
　　　　　　　├── 49x10 cell
　　├── “labeled”── 5 x 1 cell
　　　　　　　├── 843x10 cell
　　　　　　　├── 440x10 cell
　　　　　　　├── 77x10 cell
　　　　　　　├── 58x10 cell
　　　　　　　├── 49x10 cell
　　├── “testsets”── 20 x 1 cell
　　　　　　　├── 100 x 2 double matrix

## 目录介绍

（1）”detected”—— 5 x 1 cells，由机器标注，每个 cell 中包含一对摄像头组采集的照片，如下所示：
　　每个摄像头组由 M x 10 cells 组成，M 为行人索引，前 5 列和后 5 列分别来自同一组的不同摄像头。
　　cell 内每个元素为一幅 H x W x 3 的行人框图像(uint8 数据类型)，个别图像可能空缺，为空集。

843x10 cell ——> 摄像头组pair 1。
440x10 cell ——> 摄像头组pair 2。
77x10 cell ——> 摄像头组pair 3。
58x10 cell ——> 摄像头组pair 4。
49x10 cell ——> 摄像头组pair 5。
（2）”labeled”—— 5 x 1 cells，行人框由人工标注，格式和内容和”detected”相同。

（3）”testsets”—— 20 x 1 cells，测试协议，由 20 个 100 x 2 double 类型矩阵组成 (重复二十次)。
　　100 x 2 double，100 行代表 100 个测试样本，第 1 列为摄像头 pair 索引，第 2 列为行人索引。

## 测试协议

CUHK-03的测试协议有两种。

　　第一种为旧的版本(参考文献 [1], 即数据集的出处)，参见数据集中的’testsets’测试协议。具体地说，即随机选出100个行人作为测试集，1160 个行人作为训练集，100 个行人作为验证集（这里总共 1360 个行人而不是 1467 个，这是因为实验中没有用到摄像头组pair 4 和 5 的数据），重复二十次。这种测试协议是 single-shot setting.

　　第二种测试协议(参考文献 [2])类似于 Market-1501 ，它将数据集分为包含 767 个行人的训练集和包含 700 个行人的测试集。在测试阶段，我们随机选择一张图像作为 query，剩下的作为 gallery，这样的话，对于每个行人，有多个 ground truth 在 gallery 中。

Download：[链接](https://pan.baidu.com/s/11tZoxusQsOU629iTWXQ8BA)   提取码：tegi

![img](imgs/eg_CUHK03_label.png) ![img](imgs/eg_CUHK03_detected.png)

> Li, W., Zhao, R., Xiao, T., & Wang, X. (2014). Deepreid: [Deep filter pairing neural network for person re-identification](https://www.cv-foundation.org/openaccess/content_cvpr_2014/papers/Li_DeepReID_Deep_Filter_2014_CVPR_paper.pdf). In Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (pp. 152-159).

