# Comprehensive_reID_Baseline
This is a repository for organizing codes related to re-identification (especially state-of-the-art reid methods). 

[[git bash连接github远端仓库使用说明](https://github.com/YuanXinCherry/Comprehensive_reID_Baseline/blob/master/git%E8%BF%9E%E6%8E%A5github%E9%A1%B9%E7%9B%AE%E5%85%A5%E9%97%A8.md)]

行人重识别入门资料：[[知乎](https://zhuanlan.zhihu.com/p/336753215)] 

论文排版Latex软件安装教程：[[知乎](https://zhuanlan.zhihu.com/p/338929182)]

CVPR 2021【行人/车辆重识别】相关论文和代码（基本更新完毕）：[[知乎](https://zhuanlan.zhihu.com/p/376350735)]





---
更新：袁鑫

category: deep_learning

title: Re-ID

date: 2021-06-17
---

# Leaderboard

## ReID

|                   Method                   |  backbone  | test size |  Market1501   |   CUHK03 (detected)   | CUHK03 (detected/new) | CUHK03 (labeled/new) |  CUHK-SYSU  | DukeMTMC-reID |     MARS      |
| :----------------------------------------: | :--------: | :-------: | :-----------: | :-------------------: | :-------------------: | :------------------: | :---------: | :-----------: | :-----------: |
|                                            |            |           |  rank1 / mAP  |  rank1/rank5/rank10   |      rank1 / mAP      |     rank1 / mAP      | rank1 / mAP |               |  rank1 / mAP  |
| [DG-Net](https://github.com/NVlabs/DG-Net) | ResNet-50  |  256×128  |  94.8/ 86.0   |                       |       65.6/61.1       |                      |             |   86.6/74.8   |               |
|                AlignedReID                 | ResNet50-X |           |  92.6 / 82.3  |  91.9 / 98.7 / 99.4   |                       |     86.8 / 79.1      |             |               |  95.3 / 93.7  |
|                Deep-Person                 | ResNet-50  |  256×128  | 92.31 / 79.58 |  89.4 / 98.2 / 99.1   |                       |                      |             |               | 80.90 / 64.80 |
|                    PCB                     | ResNet-50  |  384x128  |  92.4 / 77.3  |                       |      61.3 / 54.2      |                      |             |  81.9 / 65.3  |               |
|                  PCB+RPP                   | ResNet-50  |  384x128  |  93.8 / 81.6  |                       |      63.7 / 57.5      |                      |             |  83.3 / 69.2  |               |
|                   PN-GAN                   | ResNet-50  |           | 89.43 / 72.58 | 79.76 / 96.24 / 98.56 |                       |                      |             | 73.58 / 53.20 |               |
|                    MGN                     | ResNet-50  |           | 95.7 /  86.9  |                       |      66.8 / 66.0      |     68.0 / 67.4      |             |  88.7 / 78.4  |               |
|                    HPM                     | ResNet-50  |  384x128  | 94.2 /  82.7  |                       |      63.1 / 57.5      |                      |             |  86.6 / 74.3  |               |
|                  HPM+HRE                   | ResNet-50  |  384x128  | 93.9 /  83.1  |                       |      63.2 / 59.7      |                      |             |  86.3 / 74.5  |               |
|                 SphereReID                 | ResNet-50  |  288×144  | 94.4 /  83.6  |  93.1 / 98.7 / 99.4   |      63.2 / 59.7      |                      | 95.4 / 93.9 |  83.9 / 68.5  |               |
|                 Auto-ReID                  |            |  384x128  | 94.5 /  85.1  |                       |      73.3 / 69.3      |     77.9 / 73.0      |             |  88.5 / 75.1  |               |

## PersonSearch

|                            Method                            | backbone  |   CUHK-SYSU   |     PRW      |  PRW-mini   |
| :----------------------------------------------------------: | :-------: | :-----------: | :----------: | :---------: |
|                                                              |           |  top1 / mAP   |  top1 / mAP  | top1 / mAP  |
| [Joint Detection and Identification Feature Learning for Person Search](https://arxiv.org/abs/1604.01850) | ResNet-50 |  78.7 / 75.5  |   -- / --    |   -- / --   |
| [Learning Context Graph for Person Search](https://arxiv.org/abs/1904.01830) | ResNet-50 |  86.5 / 84.1  | 73.6 / 33.4  |   -- / --   |
| [Knowledge Distillation for End-to-End Person Search](https://arxiv.org/abs/1909.01058) | ResNet-50 |  88.5 / 87.2  |   -- / --    | 70.0 / 33.1 |
| [Query-guided End-to-End Person Search](https://arxiv.org/abs/1905.01203) | ResNet-50 |  89.1 / 88.9  | 76.7 / 37.1  | 80.0 / 39.1 |
| [Fast Person Search Pipeline](https://ieeexplore.ieee.org/abstract/document/8784982/) | ResNet-50 | 89.87 / 86.99 | 70.58/ 44.45 |   -- / --   |
|    End-to-End Thorough Body Perception for Person Search     | ResNet-50 |  90.5 / 88.4  | 68.9 / 42.9  |   -- / --   |
| [Re-ID Driven Localization Refinement for Person Search](https://arxiv.org/abs/1909.08580) | ResNet-50 |  94.2 / 93.0  | 70.2 / 42.9  |   -- / --   |

# Papers

**Uncertainty-Aware Multi-Shot Knowledge Distillation for Image-Based Object Re-Identification**

- intro: AAAI 2020
- arxiv: [https://arxiv.org/abs/2001.05197](https://arxiv.org/abs/2001.05197)

**Robust Re-Identification by Multiple Views Knowledge Distillation**

- intro: ECCV 2020
- intro: University of Modena and Reggio Emilia
- arxiv: [https://arxiv.org/abs/2007.04174](https://arxiv.org/abs/2007.04174)
- github: [https://github.com/aimagelab/VKD](https://github.com/aimagelab/VKD)

**Self-paced Contrastive Learning with Hybrid Memory for Domain Adaptive Object Re-ID**

- intro: NeurIPS 2020
- intro: CUHK
- project apge: [https://geyixiao.com/projects/spcl.html](https://geyixiao.com/projects/spcl.html)
- arxiv: [https://arxiv.org/abs/2006.02713](https://arxiv.org/abs/2006.02713)
- github: [https://github.com/yxgeee/SpCL](https://github.com/yxgeee/SpCL)
- github: [https://github.com/open-mmlab/OpenUnReID](https://github.com/open-mmlab/OpenUnReID)

**Context-Aware Graph Convolution Network for Target Re-identification**

- intro: AAAI 2021
- intro: SenseTime Research & Xidian University & Peking University
- arxiv: [https://arxiv.org/abs/2012.04298](https://arxiv.org/abs/2012.04298)

# Person Re-identification / Person Retrieval

**DeepReID: Deep Filter Pairing Neural Network for Person Re-Identification**

- intro: CVPR 2014
- paper: [http://www.cv-foundation.org/openaccess/content_cvpr_2014/papers/Li_DeepReID_Deep_Filter_2014_CVPR_paper.pdf](http://www.cv-foundation.org/openaccess/content_cvpr_2014/papers/Li_DeepReID_Deep_Filter_2014_CVPR_paper.pdf)

**An Improved Deep Learning Architecture for Person Re-Identification**

- intro: CVPR 2015
- paper: [http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Ahmed_An_Improved_Deep_2015_CVPR_paper.pdf](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Ahmed_An_Improved_Deep_2015_CVPR_paper.pdf)
- github: [https://github.com/Ning-Ding/Implementation-CVPR2015-CNN-for-ReID](https://github.com/Ning-Ding/Implementation-CVPR2015-CNN-for-ReID)

**Deep Ranking for Person Re-identification via Joint Representation Learning**

- intro: IEEE Transactions on Image Processing (TIP), 2016
- arxiv: [https://arxiv.org/abs/1505.06821](https://arxiv.org/abs/1505.06821)

**PersonNet: Person Re-identification with Deep Convolutional Neural Networks**

- arxiv: [http://arxiv.org/abs/1601.07255](http://arxiv.org/abs/1601.07255)

**Learning Deep Feature Representations with Domain Guided Dropout for Person Re-identification**

- intro: CVPR 2016
- arxiv: [https://arxiv.org/abs/1604.07528](https://arxiv.org/abs/1604.07528)
- github: [https://github.com/Cysu/dgd_person_reid](https://github.com/Cysu/dgd_person_reid)

**Person Re-Identification by Multi-Channel Parts-Based CNN with Improved Triplet Loss Function**

- intro: CVPR 2016
- paper: [http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Cheng_Person_Re-Identification_by_CVPR_2016_paper.pdf](http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Cheng_Person_Re-Identification_by_CVPR_2016_paper.pdf)

**Joint Learning of Single-image and Cross-image Representations for Person Re-identification**

- intro: CVPR 2016
- paper: [http://openaccess.thecvf.com/content_cvpr_2016/papers/Wang_Joint_Learning_of_CVPR_2016_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2016/papers/Wang_Joint_Learning_of_CVPR_2016_paper.pdf)

**End-to-End Comparative Attention Networks for Person Re-identification**

[https://arxiv.org/abs/1606.04404](https://arxiv.org/abs/1606.04404)

**A Multi-task Deep Network for Person Re-identification**

- intro: AAAI 2017
- arxiv: [http://arxiv.org/abs/1607.05369](http://arxiv.org/abs/1607.05369)

**A Siamese Long Short-Term Memory Architecture for Human Re-Identification**

- arxiv: [http://arxiv.org/abs/1607.08381](http://arxiv.org/abs/1607.08381)

**Gated Siamese Convolutional Neural Network Architecture for Human Re-Identification**

- intro: ECCV 2016
- keywords: Market1501 rank1 = 65.9%
- arxiv: [https://arxiv.org/abs/1607.08378](https://arxiv.org/abs/1607.08378)

**Deep Neural Networks with Inexact Matching for Person Re-Identification**

- intro: NIPS 2016
- keywords: Normalized correlation layer, CUHK03/CUHK01/QMULGRID
- paper: [https://papers.nips.cc/paper/6367-deep-neural-networks-with-inexact-matching-for-person-re-identification](https://papers.nips.cc/paper/6367-deep-neural-networks-with-inexact-matching-for-person-re-identification)
- github: [https://github.com/InnovArul/personreid_normxcorr](https://github.com/InnovArul/personreid_normxcorr)

**Person Re-identification: Past, Present and Future**

[https://arxiv.org/abs/1610.02984](https://arxiv.org/abs/1610.02984)

**Deep Learning Prototype Domains for Person Re-Identification**

- arxiv: [https://arxiv.org/abs/1610.05047](https://arxiv.org/abs/1610.05047)

**Deep Transfer Learning for Person Re-identification**

- arxiv: [https://arxiv.org/abs/1611.05244](https://arxiv.org/abs/1611.05244)

**A Discriminatively Learned CNN Embedding for Person Re-identification**

- intro: TOMM 2017
- arxiv: [https://arxiv.org/abs/1611.05666](https://arxiv.org/abs/1611.05666)
- github(official, MatConvnet): [https://github.com/layumi/2016_person_re-ID](https://github.com/layumi/2016_person_re-ID)
- github: [https://github.com/D-X-Y/caffe-reid](https://github.com/D-X-Y/caffe-reid)

**Person Re-Identification via Recurrent Feature Aggregation**

- intro: ECCV 2016
- keywords: recurrent feature aggregation network (RFA-Net)
- arxiv: [https://arxiv.org/abs/1701.06351](https://arxiv.org/abs/1701.06351)
- code: [https://sites.google.com/site/yanyichao91sjtu/](https://sites.google.com/site/yanyichao91sjtu/)
- github(official): [https://github.com/daodaofr/caffe-re-id](https://github.com/daodaofr/caffe-re-id)

**Structured Deep Hashing with Convolutional Neural Networks for Fast Person Re-identification**

- arxiv: [https://arxiv.org/abs/1702.04179](https://arxiv.org/abs/1702.04179)

**SVDNet for Pedestrian Retrieval**

- intro: ICCV 2017 spotlight
- intro: On the Market-1501 dataset, rank-1 accuracy is improved from 55.2% to 80.5% for CaffeNet, 
and from 73.8% to 83.1% for ResNet-50
- arxiv: [https://arxiv.org/abs/1703.05693](https://arxiv.org/abs/1703.05693)
- github: [https://github.com/syfafterzy/SVDNet-for-Pedestrian-Retrieval](https://github.com/syfafterzy/SVDNet-for-Pedestrian-Retrieval)

**In Defense of the Triplet Loss for Person Re-Identification**

- arxiv: [https://arxiv.org/abs/1703.07737](https://arxiv.org/abs/1703.07737)
- github(official, Theano): [https://github.com/VisualComputingInstitute/triplet-reid](https://github.com/VisualComputingInstitute/triplet-reid)

**Beyond triplet loss: a deep quadruplet network for person re-identification**

- intro: CVPR 2017
- arxiv: [https://arxiv.org/abs/1704.01719](https://arxiv.org/abs/1704.01719)
- ppaper: [http://cvip.computing.dundee.ac.uk/papers/Chen_CVPR_2017_paper.pdf](http://cvip.computing.dundee.ac.uk/papers/Chen_CVPR_2017_paper.pdf)

**Quality Aware Network for Set to Set Recognition**

- intro: CVPR 2017
- arxiv: [https://arxiv.org/abs/1704.03373](https://arxiv.org/abs/1704.03373)
- github: [https://github.com/sciencefans/Quality-Aware-Network](https://github.com/sciencefans/Quality-Aware-Network)

**Learning Deep Context-aware Features over Body and Latent Parts for Person Re-identification**

- intro: CVPR 2017. CASIA
- keywords: Multi-Scale Context-Aware Network (MSCAN)
- arxiv: [https://arxiv.org/abs/1710.06555](https://arxiv.org/abs/1710.06555)
- supplemental: [http://openaccess.thecvf.com/content_cvpr_2017/supplemental/Li_Learning_Deep_Context-Aware_2017_CVPR_supplemental.pdf](http://openaccess.thecvf.com/content_cvpr_2017/supplemental/Li_Learning_Deep_Context-Aware_2017_CVPR_supplemental.pdf)

**Point to Set Similarity Based Deep Feature Learning for Person Re-identification**

- intro: CVPR 2017
- paper: [http://openaccess.thecvf.com/content_cvpr_2017/papers/Zhou_Point_to_Set_CVPR_2017_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2017/papers/Zhou_Point_to_Set_CVPR_2017_paper.pdf)
- github(stay tuned): [https://github.com/samaonline/Point-to-Set-Similarity-Based-Deep-Feature-Learning-for-Person-Re-identification](https://github.com/samaonline/Point-to-Set-Similarity-Based-Deep-Feature-Learning-for-Person-Re-identification)

**Scalable Person Re-identification on Supervised Smoothed Manifold**

- intro: CVPR 2017 spotlight
- arxiv: [https://arxiv.org/abs/1703.08359](https://arxiv.org/abs/1703.08359)
- youtube: [https://www.youtube.com/watch?v=bESdJgalQrg](https://www.youtube.com/watch?v=bESdJgalQrg)

**Attention-based Natural Language Person Retrieval**

- intro: CVPR 2017 Workshop (vision meets cognition)
- keywords: Bidirectional Long Short- Term Memory (BLSTM)
- arxiv: [https://arxiv.org/abs/1705.08923](https://arxiv.org/abs/1705.08923)

**Part-based Deep Hashing for Large-scale Person Re-identification**

- intro: IEEE Transactions on Image Processing, 2017
- arxiv: [https://arxiv.org/abs/1705.02145](https://arxiv.org/abs/1705.02145)

**Deep Person Re-Identification with Improved Embedding**

**Deep Person Re-Identification with Improved Embedding and Efficient Training**

- intro: IJCB 2017
- arxiv: [https://arxiv.org/abs/1705.03332](https://arxiv.org/abs/1705.03332)

**Towards a Principled Integration of Multi-Camera Re-Identification and Tracking through Optimal Bayes Filters**

- arxiv: [https://arxiv.org/abs/1705.04608](https://arxiv.org/abs/1705.04608)
- github: [https://github.com/VisualComputingInstitute/towards-reid-tracking](https://github.com/VisualComputingInstitute/towards-reid-tracking)

**Person Re-Identification by Deep Joint Learning of Multi-Loss Classification**

- intro: IJCAI 2017
- arxiv: [https://arxiv.org/abs/1705.04724](https://arxiv.org/abs/1705.04724)

**Deep Representation Learning with Part Loss for Person Re-Identification**

- keywords: Part Loss Networks
- arxiv: [https://arxiv.org/abs/1707.00798](https://arxiv.org/abs/1707.00798)

**Pedestrian Alignment Network for Large-scale Person Re-identification**

- arxiv: [https://arxiv.org/abs/1707.00408](https://arxiv.org/abs/1707.00408)
- github: [https://github.com/layumi/Pedestrian_Alignment](https://github.com/layumi/Pedestrian_Alignment)

**Learning Efficient Image Representation for Person Re-Identification**

[https://arxiv.org/abs/1707.02319](https://arxiv.org/abs/1707.02319)

**Person Re-identification Using Visual Attention**

- intro: ICIP 2017
- arxiv: [https://arxiv.org/abs/1707.07336](https://arxiv.org/abs/1707.07336)

**What-and-Where to Match: Deep Spatially Multiplicative Integration Networks for Person Re-identification**

[https://arxiv.org/abs/1707.07074](https://arxiv.org/abs/1707.07074)

**Deep Feature Learning via Structured Graph Laplacian Embedding for Person Re-Identification**

[https://arxiv.org/abs/1707.07791](https://arxiv.org/abs/1707.07791)

**Large Margin Learning in Set to Set Similarity Comparison for Person Re-identification**

- intro: IEEE Transactions on Multimedia
- arxiv: [https://arxiv.org/abs/1708.05512](https://arxiv.org/abs/1708.05512)

**Multi-scale Deep Learning Architectures for Person Re-identification**

- intro: ICCV 2017
- arxiv: [https://arxiv.org/abs/1709.05165](https://arxiv.org/abs/1709.05165)

**Person Re-Identification by Deep Learning Multi-Scale Representations**

- intro: ICCV 2017
- keywords: Deep Pyramid Feature Learning (DPFL)
- paper: [http://openaccess.thecvf.com/content_ICCV_2017_workshops/papers/w37/Chen_Person_Re-Identification_by_ICCV_2017_paper.pdf](http://openaccess.thecvf.com/content_ICCV_2017_workshops/papers/w37/Chen_Person_Re-Identification_by_ICCV_2017_paper.pdf)
- paper: [http://www.eecs.qmul.ac.uk/~sgg/papers/ChenEtAl_ICCV2017WK_CHI.pdf](http://www.eecs.qmul.ac.uk/~sgg/papers/ChenEtAl_ICCV2017WK_CHI.pdf)

**Person Re-Identification with Vision and Language**

[https://arxiv.org/abs/1710.01202](https://arxiv.org/abs/1710.01202)

**Margin Sample Mining Loss: A Deep Learning Based Method for Person Re-identification**

[https://arxiv.org/abs/1710.00478](https://arxiv.org/abs/1710.00478)

**Pseudo-positive regularization for deep person re-identification**

[https://arxiv.org/abs/1711.06500](https://arxiv.org/abs/1711.06500)

**Let Features Decide for Themselves: Feature Mask Network for Person Re-identification**

- keywords: Feature Mask Network (FMN)
- arxiv: [https://arxiv.org/abs/1711.07155](https://arxiv.org/abs/1711.07155)

**AlignedReID: Surpassing Human-Level Performance in Person Re-Identification**

- intro: Megvii Inc & Zhejiang University
- arxiv: [https://arxiv.org/abs/1711.08184](https://arxiv.org/abs/1711.08184)
- evaluation website: (Market1501): [http://reid-challenge.megvii.com/](http://reid-challenge.megvii.com/)
- evaluation website: (CUHK03): [http://reid-challenge.megvii.com/cuhk03](http://reid-challenge.megvii.com/cuhk03)
- github: [https://github.com/huanghoujing/AlignedReID-Re-Production-Pytorch](https://github.com/huanghoujing/AlignedReID-Re-Production-Pytorch)

**Deep Cosine Metric Learning for Person Re-Identification**

- intro: WACV 2018
- paper: [https://elib.dlr.de/116408/1/WACV2018.pdf](https://elib.dlr.de/116408/1/WACV2018.pdf)
- github: [https://github.com/nwojke/cosine_metric_learning](https://github.com/nwojke/cosine_metric_learning)

**Region-based Quality Estimation Network for Large-scale Person Re-identification**

- intro: AAAI 2018
- arxiv: [https://arxiv.org/abs/1711.08766](https://arxiv.org/abs/1711.08766)

**Beyond Part Models: Person Retrieval with Refined Part Pooling**

- intro: ECCV 2018
- keywords: Part-based Convolutional Baseline (PCB), Refined Part Pooling (RPP)
- arxiv: [https://arxiv.org/abs/1711.09349](https://arxiv.org/abs/1711.09349)
- github: [https://github.com/syfafterzy/PCB_RPP_for_reID](https://github.com/syfafterzy/PCB_RPP_for_reID)

**Deep-Person: Learning Discriminative Deep Features for Person Re-Identification**

[https://arxiv.org/abs/1711.10658](https://arxiv.org/abs/1711.10658)

**Hierarchical Cross Network for Person Re-identification**

[https://arxiv.org/abs/1712.06820](https://arxiv.org/abs/1712.06820)

**Re-ID done right: towards good practices for person re-identification**

[https://arxiv.org/abs/1801.05339](https://arxiv.org/abs/1801.05339)

**Triplet-based Deep Similarity Learning for Person Re-Identification**

- intro: ICCV Workshops 2017
- arxiv: [https://arxiv.org/abs/1802.03254](https://arxiv.org/abs/1802.03254)

**Group Consistent Similarity Learning via Deep CRFs for Person Re-Identification**

- intro: CVPR 2018 oral
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Chen_Group_Consistent_Similarity_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Chen_Group_Consistent_Similarity_CVPR_2018_paper.pdf)
- github(official, PyTorch): [https://github.com/dapengchen123/crf_affinity](https://github.com/dapengchen123/crf_affinity)

**Image-Image Domain Adaptation with Preserved Self-Similarity and Domain-Dissimilarity for Person Re-identification**

- intro: CVPR 2018
- keywords: similarity preserving generative adversarial network (SPGAN), Siamese network, CycleGAN, domain adaptation
- arxiv: [https://arxiv.org/abs/1711.07027](https://arxiv.org/abs/1711.07027)

**Similarity-preserving Image-image Domain Adaptation for Person Re-identification**

[https://arxiv.org/abs/1811.10551](https://arxiv.org/abs/1811.10551)

**Harmonious Attention Network for Person Re-Identification**

- intro: CVPR 2018
- keywords: Harmonious Attention CNN (HA-CNN)
- arxiv: [https://arxiv.org/abs/1802.08122](https://arxiv.org/abs/1802.08122)

**Camera Style Adaptation for Person Re-identfication**

- intro: CVPR 2018
- arxiv: [https://arxiv.org/abs/1711.10295](https://arxiv.org/abs/1711.10295)
- github: [https://github.com/zhunzhong07/CamStyle](https://github.com/zhunzhong07/CamStyle)

**Image-Image Domain Adaptation with Preserved Self-Similarity and Domain-Dissimilarity for Person Re-identification**

- intro: CVPR 2018
- arxiv: [https://arxiv.org/abs/1711.07027](https://arxiv.org/abs/1711.07027)

**Dual Attention Matching Network for Context-Aware Feature Sequence based Person Re-Identification**

- intro: CVPR 2018
- arxiv: [https://arxiv.org/abs/1803.09937](https://arxiv.org/abs/1803.09937)

**Multi-Level Factorisation Net for Person Re-Identification**

- intro: CVPR 2018
- keywords: Multi-Level Factorisation Net (MLFN)
- arxiv: [https://arxiv.org/abs/1803.09132](https://arxiv.org/abs/1803.09132)

**Features for Multi-Target Multi-Camera Tracking and Re-Identification**

**Good Appearance Features for Multi-Target Multi-Camera Tracking**

- intro: CVPR 2018 spotlight
- intro: Duke University
- keywords: adaptive weighted triplet loss, hard-identity mining
- project page: [http://vision.cs.duke.edu/DukeMTMC/](http://vision.cs.duke.edu/DukeMTMC/)
- arxiv: [https://arxiv.org/abs/1803.10859](https://arxiv.org/abs/1803.10859)

**Mask-guided Contrastive Attention Model for Person Re-Identification**

- intro: CVPR 2018
- keywords: MGCAM
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Song_Mask-Guided_Contrastive_Attention_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Song_Mask-Guided_Contrastive_Attention_CVPR_2018_paper.pdf)
- github: [https://github.com/developfeng/MGCAM](https://github.com/developfeng/MGCAM)

**Efficient and Deep Person Re-Identification using Multi-Level Similarity**

- intro: CVPR 2018
- arxiv: [https://arxiv.org/abs/1803.11353](https://arxiv.org/abs/1803.11353)

**Person Re-identification with Cascaded Pairwise Convolutions**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_Person_Re-Identification_With_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_Person_Re-Identification_With_CVPR_2018_paper.pdf)

**Attention-Aware Compositional Network for Person Re-identification**

- intro: CVPR 2018
- intro: Sensets Technology Limited & University of Sydney
- keywords: Attention-Aware Compositional Network (AACN), Pose-guided Part Attention (PPA), Attention-aware Feature Composition (AFC)
- arxiv: [https://arxiv.org/abs/1805.03344](https://arxiv.org/abs/1805.03344)

**Deep Group-shuffling Random Walk for Person Re-identification**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Shen_Deep_Group-Shuffling_Random_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Shen_Deep_Group-Shuffling_Random_CVPR_2018_paper.pdf)
- github: [https://github.com/YantaoShen/kpm_rw_person_reid](https://github.com/YantaoShen/kpm_rw_person_reid)

**Adversarially Occluded Samples for Person Re-identification**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Huang_Adversarially_Occluded_Samples_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Huang_Adversarially_Occluded_Samples_CVPR_2018_paper.pdf)
- github: [https://github.com/huanghoujing/AOS4ReID](https://github.com/huanghoujing/AOS4ReID)

**Easy Identification from Better Constraints: Multi-Shot Person Re-Identification from Reference Constraints**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Zhou_Easy_Identification_From_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Zhou_Easy_Identification_From_CVPR_2018_paper.pdf)

**Eliminating Background-bias for Robust Person Re-identification**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Tian_Eliminating_Background-Bias_for_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Tian_Eliminating_Background-Bias_for_CVPR_2018_paper.pdf)

**End-to-End Deep Kronecker-Product Matching for Person Re-identification**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Shen_End-to-End_Deep_Kronecker-Product_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Shen_End-to-End_Deep_Kronecker-Product_CVPR_2018_paper.pdf)
- github: [https://github.com/YantaoShen/kpm_rw_person_reid](https://github.com/YantaoShen/kpm_rw_person_reid)

**Exploiting Transitivity for Learning Person Re-identification Models on a Budget**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Roy_Exploiting_Transitivity_for_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Roy_Exploiting_Transitivity_for_CVPR_2018_paper.pdf)

**Resource Aware Person Re-identification across Multiple Resolutions**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_Resource_Aware_Person_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_Resource_Aware_Person_CVPR_2018_paper.pdf)
- arxiv: [https://arxiv.org/abs/1805.08805](https://arxiv.org/abs/1805.08805)

**Multi-Channel Pyramid Person Matching Network for Person Re-Identification**

- intro: 32nd AAAI Conference on Artificial Intelligence
- keywords: Multi-Channel deep convolutional Pyramid Person Matching Network (MC-PPMN)
- arxiv: [https://arxiv.org/abs/1803.02558](https://arxiv.org/abs/1803.02558)

**Pyramid Person Matching Network for Person Re-identification**

- intro: 9th Asian Conference on Machine Learning (ACML2017) JMLR Workshop and Conference Proceedings
- arxiv: [https://arxiv.org/abs/1803.02547](https://arxiv.org/abs/1803.02547)

**Virtual CNN Branching: Efficient Feature Ensemble for Person Re-Identification**

[https://arxiv.org/abs/1803.05872](https://arxiv.org/abs/1803.05872)

**Weighted Bilinear Coding over Salient Body Parts for Person Re-identification**

[https://arxiv.org/abs/1803.08580](https://arxiv.org/abs/1803.08580)

**Adversarial Binary Coding for Efficient Person Re-identification**

[https://arxiv.org/abs/1803.10914](https://arxiv.org/abs/1803.10914)

**Learning View-Specific Deep Networks for Person Re-Identification**

- intro: IEEE Transactions on image processing. Sun Yat-Sen University
- keywords: cross-view Euclidean constraint (CV-EC), cross-view center loss (CV-CL)
- arxiv: [https://arxiv.org/abs/1803.11333](https://arxiv.org/abs/1803.11333)

**Learning Discriminative Features with Multiple Granularities for Person Re-Identification**

- intro: ACM Multimedia 2018
- intro: Shanghai Jiao Tong University & CloudWalk
- keywords: Multiple Granularity Network (MGN)
- arxiv: [https://arxiv.org/abs/1804.01438](https://arxiv.org/abs/1804.01438)
- video: [https://edu.csdn.net/course/play/8426](https://edu.csdn.net/course/play/8426)

**Recurrent Neural Networks for Person Re-identification Revisited**

- intro: Stanford University & Google AI
- arxiv: [https://arxiv.org/abs/1804.03281](https://arxiv.org/abs/1804.03281)

**MaskReID: A Mask Based Deep Ranking Neural Network for Person Re-identification**

[https://arxiv.org/abs/1804.03864](https://arxiv.org/abs/1804.03864)

**Horizontal Pyramid Matching for Person Re-identification**

- intro: AAAI 2019
- intro: UIUC & IBM Research & Cornell University & Stevens Institute of Technology & CloudWalk Technology
- keywords: Horizontal Pyramid Matching (HPM), Horizontal Pyramid Pooling (HPP), horizontal random erasing (HRE)
- arxiv: [https://arxiv.org/abs/1804.05275](https://arxiv.org/abs/1804.05275)
- github: [https://github.com/OasisYang/HPM](https://github.com/OasisYang/HPM)

**Deep Co-attention based Comparators For Relative Representation Learning in Person Re-identification**

[https://arxiv.org/abs/1804.11027](https://arxiv.org/abs/1804.11027)

**Feature Affinity based Pseudo Labeling for Semi-supervised Person Re-identification**

[https://arxiv.org/abs/1805.06118](https://arxiv.org/abs/1805.06118)

**Semantically Selective Augmentation for Deep Compact Person Re-Identification**

[https://arxiv.org/abs/1806.04074](https://arxiv.org/abs/1806.04074)

**SphereReID: Deep Hypersphere Manifold Embedding for Person Re-Identification**

- keywords: Sphere Loss, feature normalization, weight normalization, balanced sampling
- arxiv: [https://arxiv.org/abs/1807.00537](https://arxiv.org/abs/1807.00537)

**Multi-task Mid-level Feature Alignment Network for Unsupervised Cross-Dataset Person Re-Identification**

- intro: BMVC 2018
- intro: University of Warwick & Nanyang Technological University & Charles Sturt University
- arxiv: [https://arxiv.org/abs/1807.01440](https://arxiv.org/abs/1807.01440)

**Discriminative Feature Learning with Foreground Attention for Person Re-Identification**

[https://arxiv.org/abs/1807.01455](https://arxiv.org/abs/1807.01455)

**Part-Aligned Bilinear Representations for Person Re-identification**

- intro: ECCV 2018
- intro: Seoul National University & Microsoft Research & Max Planck Institute & University of Tubingen & JD.COM
- arxiv: [https://arxiv.org/abs/1804.07094](https://arxiv.org/abs/1804.07094)
- github: [https://github.com/yuminsuh/part_bilinear_reid](https://github.com/yuminsuh/part_bilinear_reid)

**Mancs: A Multi-task Attentional Network with Curriculum Sampling for Person Re-identification**

- intro: ECCV 2018. Huazhong University of Science and Technology & Horizon Robotics Inc.

**Improving Deep Visual Representation for Person Re-identification by Global and Local Image-language Association**

- intro: ECCV 2018
- arxiv: [https://arxiv.org/abs/1808.01571](https://arxiv.org/abs/1808.01571)

**Deep Sequential Multi-camera Feature Fusion for Person Re-identification**

[https://arxiv.org/abs/1807.07295](https://arxiv.org/abs/1807.07295)

**Improving Deep Models of Person Re-identification for Cross-Dataset Usage**

- intro: AIAI 2018 (14th International Conference on Artificial Intelligence Applications and Innovations) proceeding
- arxiv: [https://arxiv.org/abs/1807.08526](https://arxiv.org/abs/1807.08526)

**Measuring the Temporal Behavior of Real-World Person Re-Identification**

[https://arxiv.org/abs/1808.05499](https://arxiv.org/abs/1808.05499)

**Alignedreid＋+: Dynamically Matching Local Information for Person Re-Identification**

[https://github.com/michuanhaohao/AlignedReID](https://github.com/michuanhaohao/AlignedReID)

**Sparse Label Smoothing for Semi-supervised Person Re-Identification**

- arxiv: [https://arxiv.org/abs/1809.04976](https://arxiv.org/abs/1809.04976)
- github: [https://github.com/jpainam/SLS_ReID](https://github.com/jpainam/SLS_ReID)

**In Defense of the Classification Loss for Person Re-Identification**

- intro: University of Science and Technology of China & Microsoft Research Asia
- arxiv: [https://arxiv.org/abs/1809.05864](https://arxiv.org/abs/1809.05864)

**FD-GAN: Pose-guided Feature Distilling GAN for Robust Person Re-identification**

- intro: NIPS 2018
- arxiv: [https://arxiv.org/abs/1810.02936](https://arxiv.org/abs/1810.02936)
- github(Pytorch, official): [https://github.com/yxgeee/FD-GAN](https://github.com/yxgeee/FD-GAN)

**Image-to-Video Person Re-Identification by Reusing Cross-modal Embeddings**

[https://arxiv.org/abs/1810.03989](https://arxiv.org/abs/1810.03989)

**Attention Driven Person Re-identification**

- intro: Pattern Recognition (PR)
- arxiv: [https://arxiv.org/abs/1810.05866](https://arxiv.org/abs/1810.05866)

**A Coarse-to-fine Pyramidal Model for Person Re-identification via Multi-Loss Dynamic Training**

- intro: YouTu Lab, Tencent
- arxiv: [https://arxiv.org/abs/1810.12193](https://arxiv.org/abs/1810.12193)

**M2M-GAN: Many-to-Many Generative Adversarial Transfer Learning for Person Re-Identification**

[https://arxiv.org/abs/1811.03768](https://arxiv.org/abs/1811.03768)

**Batch Feature Erasing for Person Re-identification and Beyond**

- arxiv: [https://arxiv.org/abs/1811.07130](https://arxiv.org/abs/1811.07130)
- github(official, Pytorch): [https://github.com/daizuozhuo/batch-feature-erasing-network](https://github.com/daizuozhuo/batch-feature-erasing-network)

**Re-Identification with Consistent Attentive Siamese Networks**

[https://arxiv.org/abs/1811.07487](https://arxiv.org/abs/1811.07487)

**One Shot Domain Adaptation for Person Re-Identification**

[https://arxiv.org/abs/1811.10144](https://arxiv.org/abs/1811.10144)

**Parameter-Free Spatial Attention Network for Person Re-Identification**

- arxiv: [https://arxiv.org/abs/1811.12150](https://arxiv.org/abs/1811.12150)
- github: [https://github.com/HRanWang/Spatial-Attention](https://github.com/HRanWang/Spatial-Attention)

**Spectral Feature Transformation for Person Re-identification**

- intro: University of Chinese Academy of Sciences & TuSimple
- arxiv: [https://arxiv.org/abs/1811.11405](https://arxiv.org/abs/1811.11405)

**Identity Preserving Generative Adversarial Network for Cross-Domain Person Re-identification**

[https://arxiv.org/abs/1811.11510](https://arxiv.org/abs/1811.11510)

**Dissecting Person Re-identification from the Viewpoint of Viewpoint**

[https://arxiv.org/abs/1812.02162](https://arxiv.org/abs/1812.02162)

**Fast and Accurate Person Re-Identification with RMNet**

- intro: IOTG Computer Vision (ICV), Intel
- arxiv: [https://arxiv.org/abs/1812.02465](https://arxiv.org/abs/1812.02465)

**Spatial-Temporal Person Re-identification**

- intro: AAAI 2019
- intro: Sun Yat-sen University
- arxiv: [https://arxiv.org/abs/1812.03282](https://arxiv.org/abs/1812.03282)
- github: [https://github.com/Wanggcong/Spatial-Temporal-Re-identification](https://github.com/Wanggcong/Spatial-Temporal-Re-identification)

**Omni-directional Feature Learning for Person Re-identification**

- intro: Tongji University
- keywords: OIM loss
- arxiv: [https://arxiv.org/abs/1812.05319](https://arxiv.org/abs/1812.05319)

**Learning Incremental Triplet Margin for Person Re-identification**

- intro: AAAI 2019 spotlight
- intro: Hikvision Research Institute
- arxiv: [https://arxiv.org/abs/1812.06576](https://arxiv.org/abs/1812.06576)

**Densely Semantically Aligned Person Re-Identification**

- intro: USTC & MSRA
- arxiv: [https://arxiv.org/abs/1812.08967](https://arxiv.org/abs/1812.08967)

**EANet: Enhancing Alignment for Cross-Domain Person Re-identification**

- intro: CRISE & CASIA & Horizon Robotics
- arxiv: [https://arxiv.org/abs/1812.11369](https://arxiv.org/abs/1812.11369)
- github(official, Pytorch): [https://github.com/huanghoujing/EANet](https://github.com/huanghoujing/EANet)
- blog: [https://zhuanlan.zhihu.com/p/53660395](https://zhuanlan.zhihu.com/p/53660395)

**Backbone Can Not be Trained at Once: Rolling Back to Pre-trained Network for Person Re-Identification**

- intro: AAAI 2019
- intro: Seoul National University & Samsung SDS
- arxiv: [https://arxiv.org/abs/1901.06140](https://arxiv.org/abs/1901.06140)

**Ensemble Feature for Person Re-Identification**

- keywords: EnsembleNet
- arxiv: [https://arxiv.org/abs/1901.05798](https://arxiv.org/abs/1901.05798)

**Adversarial Metric Attack for Person Re-identification**

- intro: University of Oxford & Johns Hopkins University
- arxiv: [https://arxiv.org/abs/1901.10650](https://arxiv.org/abs/1901.10650)

**Discovering Underlying Person Structure Pattern with Relative Local Distance for Person Re-identification**

- intro: SYSU
- arxiv: [https://arxiv.org/abs/1901.10100](https://arxiv.org/abs/1901.10100)
- github: [https://github.com/Wanggcong/RLD_codes](https://github.com/Wanggcong/RLD_codes)

**Attributes-aided Part Detection and Refinement for Person Re-identification**

[https://arxiv.org/abs/1902.10528](https://arxiv.org/abs/1902.10528)

B**ags of Tricks and A Strong Baseline for Deep Person Re-identification**

- intro: CVPR 2019 Workshop
- arxiv: [https://arxiv.org/abs/1903.07071](https://arxiv.org/abs/1903.07071)
- paper: [http://openaccess.thecvf.com/content_CVPRW_2019/papers/TRMTMCT/Luo_Bag_of_Tricks_and_a_Strong_Baseline_for_Deep_Person_CVPRW_2019_paper.pdf](http://openaccess.thecvf.com/content_CVPRW_2019/papers/TRMTMCT/Luo_Bag_of_Tricks_and_a_Strong_Baseline_for_Deep_Person_CVPRW_2019_paper.pdf)
- slides: [https://drive.google.com/file/d/1h9SgdJenvfoNp9PTUxPiz5_K5HFCho-V/view](https://drive.google.com/file/d/1h9SgdJenvfoNp9PTUxPiz5_K5HFCho-V/view)
- github: [https://github.com/michuanhaohao/reid-strong-baseline](https://github.com/michuanhaohao/reid-strong-baseline)

**Auto-ReID: Searching for a Part-aware ConvNet for Person Re-Identification**

- keywords: NAS
- arxiv: [https://arxiv.org/abs/1903.09776](https://arxiv.org/abs/1903.09776)
- github(official): [https://github.com/D-X-Y/Auto-ReID-and-Others](https://github.com/D-X-Y/Auto-ReID-and-Others)

**Perceive Where to Focus: Learning Visibility-aware Part-level Features for Partial Person Re-identification**

- intro: CVPR 2019
- intro: Tsinghua University & Megvii Technology
- keywords: Visibility-aware Part Model (VPM)
- arxiv: [https://arxiv.org/abs/1904.00537](https://arxiv.org/abs/1904.00537)

**Pedestrian re-identification based on Tree branch network with local and global learning**

- intro: ICME 2019 oral
- arxiv: [https://arxiv.org/abs/1904.00355](https://arxiv.org/abs/1904.00355)

**Invariance Matters: Exemplar Memory for Domain Adaptive Person Re-identification**

- intro: CVPR 2019
- arxiv: [https://arxiv.org/abs/1904.01990](https://arxiv.org/abs/1904.01990)
- github: [https://github.com/zhunzhong07/ECN](https://github.com/zhunzhong07/ECN)

**Person Re-identification with Bias-controlled Adversarial Training**

[https://arxiv.org/abs/1904.00244](https://arxiv.org/abs/1904.00244)

**Relation-Aware Global Attention for Person Re-identification**

- intro: CVPR 2020
- intro: University of Science and Technology of China & Microsoft Research Asia
- arxiv: [https://arxiv.org/abs/1904.02998](https://arxiv.org/abs/1904.02998)
- github: [https://github.com/microsoft/Relation-Aware-Global-Attention-Networks](https://github.com/microsoft/Relation-Aware-Global-Attention-Networks)

**Person Re-identification with Metric Learning using Privileged Information**

- intro: IEEE TIP
- arxiv: [https://arxiv.org/abs/1904.05005](https://arxiv.org/abs/1904.05005)

**Multi-Scale Body-Part Mask Guided Attention for Person Re-identification**

- intro: Suning R&D Center USA
- arxiv: [https://arxiv.org/abs/1904.11041](https://arxiv.org/abs/1904.11041)

**Deep Constrained Dominant Sets for Person Re-identification**

[https://arxiv.org/abs/1904.11397](https://arxiv.org/abs/1904.11397)

**Illumination-Adaptive Person Re-identification**

- intro: 1The University of Tokyo & National Taiwan University & National Institute of Informatics
- arxiv: [https://arxiv.org/abs/1905.04525](https://arxiv.org/abs/1905.04525)

**Domain Adaptive Person Re-Identification via Camera Style Generation and Label Propagation**

- intro: Sun Yat-Sen University & Chinese Academy of Sciences
- arxiv: [https://arxiv.org/abs/1905.05382](https://arxiv.org/abs/1905.05382)

**Beyond Intra-modality Discrepancy: A Comprehensive Survey of Heterogeneous Person Re-identification**

[https://arxiv.org/abs/1905.10048](https://arxiv.org/abs/1905.10048)

**Deep Multi-Index Hashing for Person Re-Identification**

- intro: Nanjing University
- arxiv: [https://arxiv.org/abs/1905.10980](https://arxiv.org/abs/1905.10980)

**Attention: A Big Surprise for Cross-Domain Person Re-Identification**

[https://arxiv.org/abs/1905.12830](https://arxiv.org/abs/1905.12830)

**Semantics-Aligned Representation Learning for Person Re-identification**

- intro: USTC & MSRA
- keywords: Semantics Aligning Network (SAN)
- arxiv: [https://arxiv.org/abs/1905.13143](https://arxiv.org/abs/1905.13143)

**Rethinking Person Re-Identification with Confidence**

- intro: EPFL
- arxiv: [https://arxiv.org/abs/1906.04692](https://arxiv.org/abs/1906.04692)

**CDPM: Convolutional Deformable Part Models for Person Re-identification**

[https://arxiv.org/abs/1906.04976](https://arxiv.org/abs/1906.04976)

**Resolution-invariant Person Re-Identification**

- intro: IJCAI 2019
- intro: Peking University & Horizon Robotics
- arxiv: [https://arxiv.org/abs/1906.09748](https://arxiv.org/abs/1906.09748)

**Interaction-and-Aggregation Network for Person Re-identification**

- intro: CVPR 2019
- arxiv: [https://arxiv.org/abs/1907.08435](https://arxiv.org/abs/1907.08435)

**Distilled Person Re-identification: Towards a More Scalable System**

- intro: CVPR 2019
- intro: Sun Yat-sen University & YouTu Lab, Tencent
- keywords: Multi-teacher Adaptive Similarity Distillation Framework, Log-Euclidean Similarity Distillation Loss, 
Adaptive Knowledge Aggregator
- paper: [http://openaccess.thecvf.com/content_CVPR_2019/papers/Wu_Distilled_Person_Re-Identification_Towards_a_More_Scalable_System_CVPR_2019_paper.pdf](http://openaccess.thecvf.com/content_CVPR_2019/papers/Wu_Distilled_Person_Re-Identification_Towards_a_More_Scalable_System_CVPR_2019_paper.pdf)

**Universal Person Re-Identification**

- intro: Queen Mary University of London & Vision Semantics Ltd.
- arxiv: [https://arxiv.org/abs/1907.09511](https://arxiv.org/abs/1907.09511)

**ABD-Net: Attentive but Diverse Person Re-Identification**

- intro: ICCV 2019
- arxiv: [https://arxiv.org/abs/1908.01114](https://arxiv.org/abs/1908.01114)
- github: [https://github.com/TAMU-VITA/ABD-Net](https://github.com/TAMU-VITA/ABD-Net)

**Fairest of Them All: Establishing a Strong Baseline for Cross-Domain Person ReID**

- intro: University of Waterloo & SPORTLOGiQ Inc.
- arxiv: [https://arxiv.org/abs/1907.12016](https://arxiv.org/abs/1907.12016)

**Progressive Cross-camera Soft-label Learning for Semi-supervised Person Re-identification**

[https://arxiv.org/abs/1908.05669](https://arxiv.org/abs/1908.05669)

**Mixed High-Order Attention Network for Person Re-Identification**

- intro: ICCV 2019
- arxiv: [https://arxiv.org/abs/1908.05819](https://arxiv.org/abs/1908.05819)
- github: [https://github.com/chenbinghui1/MHN](https://github.com/chenbinghui1/MHN)

**Recover and Identify: A Generative Dual Model for Cross-Resolution Person Re-Identification**

- intro: ICCV 2019
- arxiv: [https://arxiv.org/abs/1908.06052](https://arxiv.org/abs/1908.06052)

**HorNet: A Hierarchical Offshoot Recurrent Network for Improving Person Re-ID via Image Captioning**

- intro: IJCAI 2019
- intro: Nanjing Institute of Advanced Artificial Intelligence & Horizon Robotics
- arxiv: [https://arxiv.org/abs/1908.04915](https://arxiv.org/abs/1908.04915)

**Temporal Knowledge Propagation for Image-to-Video Person Re-identification**

- intro: ICCV 2019
- arxiv: [https://arxiv.org/abs/1908.03885](https://arxiv.org/abs/1908.03885)

**SBSGAN: Suppression of Inter-Domain Background Shift for Person Re-Identification**

- intro: ICCV 2019
- arxiv: [https://arxiv.org/abs/1908.09086](https://arxiv.org/abs/1908.09086)

**Learning Deep Representations by Mutual Information for Person Re-identification**

[https://arxiv.org/abs/1908.05860](https://arxiv.org/abs/1908.05860)

**Orthogonal Center Learning with Subspace Masking for Person Re-Identification**

- intro: Youtu X-lab, Tencent
- arxiv: [https://arxiv.org/abs/1908.10535](https://arxiv.org/abs/1908.10535)

**Adaptive Graph Representation Learning for Video Person Re-identification**

[https://arxiv.org/abs/1909.02240](https://arxiv.org/abs/1909.02240)

**POD: Practical Object Detection with Scale-Sensitive Network**

[https://arxiv.org/abs/1909.02225](https://arxiv.org/abs/1909.02225)

**Second-order Non-local Attention Networks for Person Re-identification**

- intro: ICCV 2019
- arxiv: [https://arxiv.org/abs/1909.00295](https://arxiv.org/abs/1909.00295)

**Cross-Dataset Person Re-Identification via Unsupervised Pose Disentanglement and Adaptation**

- intro: ICCV 2019
- arxiv: [https://arxiv.org/abs/1909.09675](https://arxiv.org/abs/1909.09675)

**View Confusion Feature Learning for Person Re-identification**

- intro: ICCV 2019
- arxiv: [https://arxiv.org/abs/1910.03849](https://arxiv.org/abs/1910.03849)

**Augmented Hard Example Mining for Generalizable Person Re-Identification**

[https://arxiv.org/abs/1910.05280](https://arxiv.org/abs/1910.05280)

**Learning Generalisable Omni-Scale Representations for Person Re-Identification**

- arxiv: [https://arxiv.org/abs/1910.06827](https://arxiv.org/abs/1910.06827)
- github: [https://github.com/KaiyangZhou/deep-person-reid](https://github.com/KaiyangZhou/deep-person-reid)

**Attention Network Robustification for Person ReID**

- intro: DAMO Academy, Alibaba Group
- arxiv: [https://arxiv.org/abs/1910.07038](https://arxiv.org/abs/1910.07038)

**Beyond Human Parts: Dual Part-Aligned Representations for Person Re-Identification**

- intro: ICCV 2019
- keywords: dual part-aligned block (DPB)
- arxiv: [https://arxiv.org/abs/1910.10111](https://arxiv.org/abs/1910.10111)
- github: [https://github.com/ggjy/P2Net.pytorch](https://github.com/ggjy/P2Net.pytorch)

**An End-to-End Foreground-Aware Network for Person Re-Identification**

[https://arxiv.org/abs/1910.11547](https://arxiv.org/abs/1910.11547)

**Learning Disentangled Representation for Robust Person Re-identification**

- intro: NeurIPS 2019
- keywords: identity shuffle GAN (IS-GAN)
- project page: [https://cvlab.yonsei.ac.kr/projects/ISGAN/](https://cvlab.yonsei.ac.kr/projects/ISGAN/)
- arxiv: [https://arxiv.org/abs/1910.12003](https://arxiv.org/abs/1910.12003)

**ID-aware Quality for Set-based Person Re-identification**

[https://arxiv.org/abs/1911.09143](https://arxiv.org/abs/1911.09143)

**Calibrated Domain-Invariant Learning for Highly Generalizable Large Scale Re-Identification**

- intro: WACV 2020
- arxiv: [https://arxiv.org/abs/1911.11314](https://arxiv.org/abs/1911.11314)

**Collaborative Attention Network for Person Re-identification**

[https://arxiv.org/abs/1911.13008](https://arxiv.org/abs/1911.13008)

**Viewpoint-Aware Loss with Angular Regularization for Person Re-Identification**

- intro: AAAI 2020
- arxiv: [https://arxiv.org/abs/1912.01300](https://arxiv.org/abs/1912.01300)
- github: [https://github.com/zzhsysu/VA-ReID](https://github.com/zzhsysu/VA-ReID)

**AANet: Attribute Attention Network for Person Re-Identifications**

- intro: CVPR 2019
- arxiv: [https://arxiv.org/abs/1912.09021](https://arxiv.org/abs/1912.09021)

**In Defense of the Triplet Loss Again: Learning Robust Person Re-Identification with Fast Approximated Triplet Loss and Label Distillation**

- arxiv: [https://arxiv.org/abs/1912.07863](https://arxiv.org/abs/1912.07863)
- github: [https://github.com/TAMU-VITA/FAT](https://github.com/TAMU-VITA/FAT)

**Rethinking the Distribution Gap of Person Re-identification with Camera-based Batch Normalization**

- intro: ECCV 2020
- intro: Tsinghua University & Huawei Inc. & Hefei University of Technology & University of Science and Technology of China
- arxiv: [https://arxiv.org/abs/2001.08680](https://arxiv.org/abs/2001.08680)
- github: [https://github.com/automan000/Camera-based-Person-ReID](https://github.com/automan000/Camera-based-Person-ReID)

**Intra-Camera Supervised Person Re-Identification**

[https://arxiv.org/abs/2002.05046](https://arxiv.org/abs/2002.05046)

**Towards Precise Intra-camera Supervised Person Re-identification**

- intro: Zhejiang University & Alibaba Group
- arxiv: [https://arxiv.org/abs/2002.04932](https://arxiv.org/abs/2002.04932)

**Diversity-Achieving Slow-DropBlock Network for Person Re-Identification**

[https://arxiv.org/abs/2002.04414](https://arxiv.org/abs/2002.04414)

**MagnifierNet: Towards Semantic Regularization and Fusion for Person Re-identification**

[https://arxiv.org/abs/2002.10979](https://arxiv.org/abs/2002.10979)

**Triplet Online Instance Matching Loss for Person Re-identification**

[https://arxiv.org/abs/2002.10560](https://arxiv.org/abs/2002.10560)

**When Person Re-identification Meets Changing Clothes**

[https://arxiv.org/abs/2003.04070](https://arxiv.org/abs/2003.04070)

**Multi-task Learning with Coarse Priors for Robust Part-aware Person Re-identification**

- intro: South China University of Technolog & University of Sydney
- keywords: Multi-task Part-aware Network (MPN)
- arxiv: [https://arxiv.org/abs/2003.08069](https://arxiv.org/abs/2003.08069)

**Transferable, Controllable, and Inconspicuous Adversarial Attacks on Person Re-identification With Deep Mis-Ranking**

- intro: CVPR 2020
- intro: To attack ReID, we propose a learning-to-mis-rank formulation to perturb the ranking of the system output
- arxiv: [https://arxiv.org/abs/2004.04199](https://arxiv.org/abs/2004.04199)
- github: [https://github.com/whj363636/Adversarial-attack-on-Person-ReID-With-Deep-Mis-Ranking](https://github.com/whj363636/Adversarial-attack-on-Person-ReID-With-Deep-Mis-Ranking)

**Real-world Person Re-Identification via Degradation Invariance Learning**

- intro: CVPR 2020
- arxiv: [https://arxiv.org/abs/2004.04933](https://arxiv.org/abs/2004.04933)

**Person Re-identification in the 3D Space**

- intro: University of Technology Sydney
- arxiv: [https://arxiv.org/abs/2006.04569](https://arxiv.org/abs/2006.04569)
- github(official): [https://github.com/layumi/person-reid-3d](https://github.com/layumi/person-reid-3d)

**Rethinking Classification Loss Designs for Person Re-identification with a Unified View**

- intro: University of Science and Technology of China & MicroSoft Research Asia & Columbia University
- arxiv: [https://arxiv.org/abs/2006.04991](https://arxiv.org/abs/2006.04991)

**Multiple Expert Brainstorming for Domain Adaptive Person Re-identification**

- intro: ECCV 2020
- arxiv: [https://arxiv.org/abs/2007.01546](https://arxiv.org/abs/2007.01546)
- github: [https://github.com/YunpengZhai/MEB-Net](https://github.com/YunpengZhai/MEB-Net)

**ESA-ReID: Entropy-Based Semantic Feature Alignment for Person re-ID**

- intro: Alibaba Group
- arxiv: [https://arxiv.org/abs/2007.04644](https://arxiv.org/abs/2007.04644)

**Joint Disentangling and Adaptation for Cross-Domain Person Re-Identification**

- intro: ECCV 2020 oral
- intro: Carnegie Mellon University & NVIDIA
- arxiv: [https://arxiv.org/abs/2007.10315](https://arxiv.org/abs/2007.10315)

**Dual Distribution Alignment Network for Generalizable Person Re-Identification**

[https://arxiv.org/abs/2007.13249](https://arxiv.org/abs/2007.13249)

**Hierarchical Bi-Directional Feature Perception Network for Person Re-Identification**

- intro: ACM MM 2020
- arxiv: [https://arxiv.org/abs/2008.03509](https://arxiv.org/abs/2008.03509)

**Black Re-ID: A Head-shoulder Descriptor for the Challenging Problem of Person Re-Identification**

- arxiv: [https://arxiv.org/abs/2008.08528](https://arxiv.org/abs/2008.08528)
- github: [https://github.com/xbq1994/HAA](https://github.com/xbq1994/HAA)

**Faster Person Re-Identification**

- intro: ECCV 2020
- arxiv: [https://arxiv.org/abs/2008.06826](https://arxiv.org/abs/2008.06826)
- github: [https://github.com/wangguanan/light-reid](https://github.com/wangguanan/light-reid)

**Do Not Disturb Me: Person Re-identification Under the Interference of Other Pedestrians**

- intro: ECCV 2020
- arxiv: [https://arxiv.org/abs/2008.06963](https://arxiv.org/abs/2008.06963)
- github(official): [https://github.com/X-BrainLab/PI-ReID](https://github.com/X-BrainLab/PI-ReID)

**Apparel-invariant Feature Learning for Apparel-changed Person Re-identification**

[https://arxiv.org/abs/2008.06181](https://arxiv.org/abs/2008.06181)

**Cluster-level Feature Alignment for Person Re-identification**

[https://arxiv.org/abs/2008.06810](https://arxiv.org/abs/2008.06810)

**Self-Supervised Gait Encoding with Locality-Aware Attention for Person Re-Identification**

- intro: IJCAI 2020
- arxiv: [https://arxiv.org/abs/2008.09435](https://arxiv.org/abs/2008.09435)
- github: [https://github.com/Kali-Hac/SGE-LA](https://github.com/Kali-Hac/SGE-LA)

**Receptive Multi-granularity Representation for Person Re-Identification**

- intro: Championship solution of NAIC 2019 Person re-ID Track
- arxiv: [https://arxiv.org/abs/2008.13450](https://arxiv.org/abs/2008.13450)

**Proxy Task Learning For Cross-Domain Person Re-Identification**

- intro: ICME 2020
- paper: [https://scihub.wikicn.top/10.1109/ICME46284.2020.9102898](https://scihub.wikicn.top/10.1109/ICME46284.2020.9102898)
- paper: [https://ieeexplore.ieee.org/document/9102898](https://ieeexplore.ieee.org/document/9102898)
- github: [https://github.com/huanghoujing/PTL](https://github.com/huanghoujing/PTL)

**Progressive Bilateral-Context Driven Model for Post-Processing Person Re-Identification**

- arxiv: [https://arxiv.org/abs/2009.03098](https://arxiv.org/abs/2009.03098)
- github: [https://github.com/123ci/PBCmodel](https://github.com/123ci/PBCmodel)

**Devil's in the Detail: Graph-based Key-point Alignment and Embedding for Person Re-ID**

- intro: Tencent Youtu Lab &  Sun Yat-sen University & Huazhong University of Science and Technology
- arxiv: [https://arxiv.org/abs/2009.05250](https://arxiv.org/abs/2009.05250)

**Hybrid-Attention Guided Network with Multiple Resolution Features for Person Re-Identification**

- arxiv: [https://arxiv.org/abs/2009.07536](https://arxiv.org/abs/2009.07536)
- github: [https://github.com/libraflower/MutipleFeature-for-PRID](https://github.com/libraflower/MutipleFeature-for-PRID)

**Beyond Triplet Loss: Person Re-identification with Fine-grained Difference-aware Pairwise Loss**

[https://arxiv.org/abs/2009.10295](https://arxiv.org/abs/2009.10295)

**Batch Coherence-Driven Network for Part-aware Person Re-Identification**

[https://arxiv.org/abs/2009.09692](https://arxiv.org/abs/2009.09692)

**FTN: Foreground-Guided Texture-Focused Person Re-Identification**

[https://arxiv.org/abs/2009.11425](https://arxiv.org/abs/2009.11425)

**Improve Person Re-Identification With Part Awareness Learning**

- intro: TIP 2020
- intro: Institute of Automation, Chinese Academy of Sciences & Horizon Robotics, Inc
- paper: [https://ieeexplore.ieee.org/document/9124699](https://ieeexplore.ieee.org/document/9124699)
- github: [https://github.com/huanghoujing/PAL-MGN](https://github.com/huanghoujing/PAL-MGN)

**Performance Optimization for Federated Person Re-identification via Benchmark Analysis**

- intro: ACMMM 2020
- arxiv: [https://arxiv.org/abs/2008.11560](https://arxiv.org/abs/2008.11560)

**DomainMix: Learning Generalizable Person Re-Identification Without Human Annotations**

[https://arxiv.org/abs/2011.11953](https://arxiv.org/abs/2011.11953)

**Multi-Domain Adversarial Feature Generalization for Person Re-Identification**

[https://arxiv.org/abs/2011.12563](https://arxiv.org/abs/2011.12563)

**Learning to Generalize Unseen Domains via Memory-based Multi-Source Meta-Learning for Person Re-Identification**

[https://arxiv.org/abs/2012.00417](https://arxiv.org/abs/2012.00417)

**Unsupervised Pre-training for Person Re-identification**

- intro: University of Science and Technology of China & Microsoft Research
- intro: LUPerson dataset
- arxiv: [https://arxiv.org/abs/2012.03753](https://arxiv.org/abs/2012.03753)

**UnrealPerson: An Adaptive Pipeline towards Costless Person Re-identification**

- arxov: [https://arxiv.org/abs/2012.04268](https://arxiv.org/abs/2012.04268)
- github: [https://github.com/FlyHighest/UnrealPerson](https://github.com/FlyHighest/UnrealPerson)

**One for More: Selecting Generalizable Samples for Generalizable ReID Model**

- intro: Tencent Youtu Lab & Sun Yat-sen University & Southern University of Science and Technology
- arxiv: [https://arxiv.org/abs/2012.05475](https://arxiv.org/abs/2012.05475)

**Exploiting Sample Uncertainty for Domain Adaptive Person Re-Identification**

- intro: AAAI 2021
- arxiv: [https://arxiv.org/abs/2012.08733](https://arxiv.org/abs/2012.08733)

**Camera-aware Proxies for Unsupervised Person Re-Identification**

- intro: AAAI 2021
- intro: 1Zhejiang University & Alibaba Group
- arxiv: [https://arxiv.org/abs/2012.10674](https://arxiv.org/abs/2012.10674)

**1st Place Solution to VisDA-2020: Bias Elimination for Domain Adaptive Pedestrian Re-identification**

- intro: 1st place solution to VisDA-2020 Challenge (ECCVW 2020)
- intro: Zhejiang University & Alibaba Group
- project page: [http://ai.bu.edu/visda-2020/](http://ai.bu.edu/visda-2020/)
- arxiv: [https://arxiv.org/abs/2012.13498](https://arxiv.org/abs/2012.13498)
- github: [https://github.com/vimar-gu/Bias-Eliminate-DA-ReID](https://github.com/vimar-gu/Bias-Eliminate-DA-ReID)

**HAVANA: Hierarchical and Variation-Normalized Autoencoder for Person Re-identification**

[https://arxiv.org/abs/2101.02568](https://arxiv.org/abs/2101.02568)

**AXM-Net: Cross-Modal Context Sharing Attention Network for Person Re-ID**

[https://arxiv.org/abs/2101.08238](https://arxiv.org/abs/2101.08238)

**TransReID: Transformer-based Object Re-Identification**

- intro: Alibaba Group & Zhejiang University
- arxiv: [https://arxiv.org/abs/2102.04378](https://arxiv.org/abs/2102.04378)

**Deep Miner: A Deep and Multi-branch Network which Mines Rich and Diverse Features for Person Re-identification**

- intro: Digeiz AI Lab & Ecole Polytechnique
- arxiv: [https://arxiv.org/abs/2102.09321](https://arxiv.org/abs/2102.09321)

**AttriMeter: An Attribute-guided Metric Interpreter for Person Re-Identification**

- intro: University of Science and Technology of China & JD AI Research & Ryerson University
- arxiv: [https://arxiv.org/abs/2103.01451](https://arxiv.org/abs/2103.01451)

**Watching You: Global-guided Reciprocal Learning for Video-based Person Re-identification**

- intro: CVPR 2021
- arxiv: [https://arxiv.org/abs/2103.04337](https://arxiv.org/abs/2103.04337)

**Lifelong Person Re-Identification via Adaptive Knowledge Accumulation**

- intro: CVPR 2021
- arxiv: [https://arxiv.org/abs/2103.12462](https://arxiv.org/abs/2103.12462)

**Spatiotemporal Transformer for Video-based Person Re-identification**

- intro: Beihang University & Pengcheng Laboratory & Tsinghua University & University of Science and Technology of China & Xidian University
- arxiv: [https://arxiv.org/abs/2103.16469](https://arxiv.org/abs/2103.16469)

**AAformer: Auto-Aligned Transformer for Person Re-Identification**

- intro: Chinese Academy of Sciences & Peng Cheng Laboratory & Peking University & Alibaba Group
- arxiv: [https://arxiv.org/abs/2104.00921](https://arxiv.org/abs/2104.00921)

**Combined Depth Space based Architecture Search For Person Re-identification**

- intro: CVPR 2021
- arxiv: [https://arxiv.org/abs/2104.04163](https://arxiv.org/abs/2104.04163)

**Graph-based Person Signature for Person Re-Identifications**

- intro: CVPR 2021 Workshops
- arxiv: [https://arxiv.org/abs/2104.06770](https://arxiv.org/abs/2104.06770)

**Unsupervised Multi-Source Domain Adaptation for Person Re-Identification**

- intro: CVPR 2021 oral
- arxiv: [https://arxiv.org/abs/2104.12961](https://arxiv.org/abs/2104.12961)

# Person Search

**End-to-End Deep Learning for Person Search**

- arxiv: [https://arxiv.org/abs/1604.01850v1](https://arxiv.org/abs/1604.01850v2)
- paper: [http://www.ee.cuhk.edu.hk/~xgwang/PS/paper.pdf](http://www.ee.cuhk.edu.hk/~xgwang/PS/paper.pdf)

**Joint Detection and Identification Feature Learning for Person Search**

- intro: CVPR 2017 Spotlight
- intro: The Chinese University of Hong Kong & Sun Yat-Sen University & SenseTime Group Limited
- keywords: Online Instance Matching (OIM) loss function
- homepage(dataset+code):[http://www.ee.cuhk.edu.hk/~xgwang/PS/dataset.html](http://www.ee.cuhk.edu.hk/~xgwang/PS/dataset.html)
- arxiv: [https://arxiv.org/abs/1604.01850](https://arxiv.org/abs/1604.01850)
- paper: [http://www.ee.cuhk.edu.hk/~xgwang/PS/paper.pdf](http://www.ee.cuhk.edu.hk/~xgwang/PS/paper.pdf)
- github(official. Caffe): [https://github.com/ShuangLI59/person_search](https://github.com/ShuangLI59/person_search)

**Person Re-identification in the Wild**

- intro: CVPR 2017 spotlight
- intro: University of Technology Sydney & UTSA & USTC & UCSD
- keywords: PRW dataset
- project page: [http://www.liangzheng.com.cn/Project/project_prw.html](http://www.liangzheng.com.cn/Project/project_prw.html)
- arxiv: [https://arxiv.org/abs/1604.02531](https://arxiv.org/abs/1604.02531)
- github: [https://github.com/liangzheng06/PRW-baseline](https://github.com/liangzheng06/PRW-baseline)
- youtube: [https://www.youtube.com/watch?v=dbOGwBITJqo](https://www.youtube.com/watch?v=dbOGwBITJqo)

**IAN: The Individual Aggregation Network for Person Search**

- intro: Xi’an Jiaotong-Liverpool University & National University of Singapore
- arxiv: [https://arxiv.org/abs/1705.05552](https://arxiv.org/abs/1705.05552)

**Neural Person Search Machines**

- intro: ICCV 2017
- intro: Hefei University of Technology & National University of Singapore & Tencent AI Lab & Panasonic R&D Center Singapore & Southwest Jiaotong University & 360 AI Institute
- arxiv: [https://arxiv.org/abs/1707.06777](https://arxiv.org/abs/1707.06777)
- paper: [https://ai.tencent.com/ailab/media/publications/Neural_Person_Search_Machines.pdf](https://ai.tencent.com/ailab/media/publications/Neural_Person_Search_Machines.pdf)

**Efficient Person Search via Expert-Guided Knowledge Distillation**

- paper: [https://ieeexplore.ieee.org/document/8759990](https://ieeexplore.ieee.org/document/8759990)

**End-to-End Detection and Re-identification Integrated Net for Person Search**

- intro: Chongqing University & Hefei University of Technology
- keywords: I-Net
- arxiv: [https://arxiv.org/abs/1804.00376](https://arxiv.org/abs/1804.00376)

**Person Search via A Mask-guided Two-stream CNN Model**

- intro: ECCV 2018
- intro: Nanjing University of Science and Technology & Youtu Lab, Tencent
- arxiv: [https://arxiv.org/abs/1807.08107](https://arxiv.org/abs/1807.08107)

**Person Search by Multi-Scale Matching**

- intro: ECCV 2018
- intro: Queen Mary University of London & Vision Semantics Ltd
- keywords: Cross-Level Semantic Alignment (CLSA)
- arxiv: [https://arxiv.org/abs/1807.08582](https://arxiv.org/abs/1807.08582)

**RCAA: Relational Context-Aware Agents for Person Search**

- intro: ECCV 2018
- intro: Carnegie Mellon University & Chinese Academy of Sciences & University of Technology Sydney
- paper: [http://openaccess.thecvf.com/content_ECCV_2018/papers/Xiaojun_Chang_RCAA_Relational_Context-Aware_ECCV_2018_paper.pdf](http://openaccess.thecvf.com/content_ECCV_2018/papers/Xiaojun_Chang_RCAA_Relational_Context-Aware_ECCV_2018_paper.pdf)

**Fast Person Search Pipeline**

- intro: ICME 2019
- intro: Sun Yat-sen University
- paper: [https://ieeexplore.ieee.org/abstract/document/8784982/](https://ieeexplore.ieee.org/abstract/document/8784982/)
- paper: [https://sci-hub.tw/10.1109/ICME.2019.00195](https://sci-hub.tw/10.1109/ICME.2019.00195)

**Learning Context Graph for Person Search**

- intro: CVPR 2019 Oral
- intro: Shanghai Jiao Tong University & Tencent YouTu Lab &  Inception Institute of Artificial Intelligence, UAE
- arxiv: [https://arxiv.org/abs/1904.01830](https://arxiv.org/abs/1904.01830)
- github(official, Pytorch): [https://github.com/sjtuzq/person_search_gcn](https://github.com/sjtuzq/person_search_gcn)

**Query-guided End-to-End Person Search**

- intro: CVPR 2019 poster
- intro: OSRAM GmbH & Technische Universität München
- keywords: query-guided end-to-end person search network (QEEPS)
- arxiv: [https://arxiv.org/abs/1905.01203](https://arxiv.org/abs/1905.01203)
- github(official): [https://github.com/munjalbharti/Query-guided-End-to-End-Person-Search](https://github.com/munjalbharti/Query-guided-End-to-End-Person-Search)

**Knowledge Distillation for End-to-End Person Search**

- intro: BMVC 2019
- intro: Technische Universität München & OSRAM GmbH
- arxiv: [https://arxiv.org/abs/1909.01058](https://arxiv.org/abs/1909.01058)

**Re-ID Driven Localization Refinement for Person Search**

- intro: ICCV 2019
- intro: Huazhong University of Science and Technology & Peking University & Shanghai Jiao Tong University & Megvii Technology
- arxiv: [https://arxiv.org/abs/1909.08580](https://arxiv.org/abs/1909.08580)

**End-to-End Thorough Body Perception for Person Search**

- intro: AAAI 2020
- intro: Horizon Robotics & Chinese Academy of Sciences
- paper: [https://aaai.org/Papers/AAAI/2020GB/AAAI-TianK.2778.pdf](https://aaai.org/Papers/AAAI/2020GB/AAAI-TianK.2778.pdf)

**Hierarchical Online Instance Matching for Person Search**

- intro: AAAI 2020
- paper: [https://aaai.org/Papers/AAAI/2020GB/AAAI-ChenD.1557.pdf](https://aaai.org/Papers/AAAI/2020GB/AAAI-ChenD.1557.pdf)
- github: [https://github.com/DeanChan/HOIM-PyTorch](https://github.com/DeanChan/HOIM-PyTorch)

**Robust Partial Matching for Person Search in the Wild**

- intro: CVPR 2020
- intro: Peking University & Intellifusion & CUHK
- keywords: Align-to-Part Network (APNet)
- arxiv: [https://arxiv.org/abs/2004.09329](https://arxiv.org/abs/2004.09329)

**Joint Person Objectness and Repulsion for Person Search**

- intro:  Chinese Academy of Sciences
- aarxiv: [https://arxiv.org/abs/2006.00155](https://arxiv.org/abs/2006.00155)

**Norm-Aware Embedding for Efﬁcient Person Search**

- intro: CVPR 2020
- paper: [http://openaccess.thecvf.com/content_CVPR_2020/papers/Chen_Norm-Aware_Embedding_for_Efficient_Person_Search_CVPR_2020_paper.pdf](http://openaccess.thecvf.com/content_CVPR_2020/papers/Chen_Norm-Aware_Embedding_for_Efficient_Person_Search_CVPR_2020_paper.pdf)
- arxiv: [https://github.com/DeanChan/NAE4PS](https://github.com/DeanChan/NAE4PS)

**A Multi-task Joint Framework for Real-time Person Search**

[https://arxiv.org/abs/2012.06418](https://arxiv.org/abs/2012.06418)

**Diverse Knowledge Distillation for End-to-End Person Search**

- intro: AAAI 2021
- intro: Tongji University & The University of Adelaide & Monash University
- arxiv: [https://arxiv.org/abs/2012.11187](https://arxiv.org/abs/2012.11187)
- github: [https://github.com/zhangxinyu-xyz/DKD-PersonSearch](https://github.com/zhangxinyu-xyz/DKD-PersonSearch)

**Multi-Attribute Enhancement Network for Person Search**

- arxiv: [https://arxiv.org/abs/2102.07968](https://arxiv.org/abs/2102.07968)
- gihtub: [https://github.com/chenlq123/MAE](https://github.com/chenlq123/MAE)

**Sequential End-to-end Network for Efficient Person Search**

- intro: Tongji University
- arxiv: [https://arxiv.org/abs/2103.10148](https://arxiv.org/abs/2103.10148)

**Anchor-Free Person Search**

- intro: CVPR 2021
- intro: Inception Institute of Artificial Intelligence (IIAI) & University of Oxford
- arxiv: [https://arxiv.org/abs/2103.11617](https://arxiv.org/abs/2103.11617)
- github: [https://github.com/daodaofr/AlignPS](https://github.com/daodaofr/AlignPS)

# Pose / Viewpoint for Re-ID

**Pose Invariant Embedding for Deep Person Re-identification**

- keywords: pose invariant embedding (PIE), PoseBox fusion (PBF) CNN
- arixv: [https://arxiv.org/abs/1701.07732](https://arxiv.org/abs/1701.07732)

**Deeply-Learned Part-Aligned Representations for Person Re-Identification**

- intro: ICCV 2017
- arxiv: [https://arxiv.org/abs/1707.07256](https://arxiv.org/abs/1707.07256)
- github(official, Caffe): [https://github.com/zlmzju/part_reid](https://github.com/zlmzju/part_reid)

**Spindle Net: Person Re-identification with Human Body Region Guided Feature Decomposition and Fusion**

- intro: CVPR 2017
- paper: [http://openaccess.thecvf.com/content_cvpr_2017/papers/Zhao_Spindle_Net_Person_CVPR_2017_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2017/papers/Zhao_Spindle_Net_Person_CVPR_2017_paper.pdf)
- github: [https://github.com/yokattame/SpindleNet](https://github.com/yokattame/SpindleNet)

**Pose-driven Deep Convolutional Model for Person Re-identification**

- intro: ICCV 2017
- arxiv: [https://arxiv.org/abs/1709.08325](https://arxiv.org/abs/1709.08325)

**A Pose-Sensitive Embedding for Person Re-Identification with Expanded Cross Neighborhood Re-Ranking**

- intro: CVPR 2018
- arxiv: [https://arxiv.org/abs/1711.10378](https://arxiv.org/abs/1711.10378)
- github(official): [https://github.com/pse-ecn/pose-sensitive-embedding](https://github.com/pse-ecn/pose-sensitive-embedding)

**Pose-Driven Deep Models for Person Re-Identification**

- intro: Masters thesis
- arxiv: [https://arxiv.org/abs/1803.08709](https://arxiv.org/abs/1803.08709)

**Pose Transferrable Person Re-Identification**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Liu_Pose_Transferrable_Person_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Liu_Pose_Transferrable_Person_CVPR_2018_paper.pdf)

**Person re-identification with fusion of hand-crafted and deep pose-based body region features**

[https://arxiv.org/abs/1803.10630](https://arxiv.org/abs/1803.10630)

# GAN for Re-ID

**Unlabeled Samples Generated by GAN Improve the Person Re-identification Baseline in vitro**

- intro: ICCV 2017
- arxiv: [https://arxiv.org/abs/1701.07717](https://arxiv.org/abs/1701.07717)
- github(official, Matlab): [https://github.com/layumi/Person-reID_GAN](https://github.com/layumi/Person-reID_GAN)
- github: [https://github.com/qiaoguan/Person-reid-GAN-pytorch](https://github.com/qiaoguan/Person-reid-GAN-pytorch)

**Person Transfer GAN to Bridge Domain Gap for Person Re-Identification**

- intro: CVPR 2018 spotlight
- intro: PTGAN
- arxiv: [https://arxiv.org/abs/1711.08565](https://arxiv.org/abs/1711.08565)
- github: [https://github.com/JoinWei-PKU/PTGAN](https://github.com/JoinWei-PKU/PTGAN)

**Pose-Normalized Image Generation for Person Re-identification**

- keywords: PN-GAN
- arxiv: [https://arxiv.org/abs/1712.02225](https://arxiv.org/abs/1712.02225)
- github: [https://github.com/naiq/PN_GAN](https://github.com/naiq/PN_GAN)

**Multi-pseudo Regularized Label for Generated Samples in Person Re-Identification**

- arxiv: [https://arxiv.org/abs/1801.06742](https://arxiv.org/abs/1801.06742)
- github: [https://github.com/Huang-3/MpRL-for-person-re-ID](https://github.com/Huang-3/MpRL-for-person-re-ID)

**Joint Discriminative and Generative Learning for Person Re-identification**

- intro: CVPR 2019 oral
- intro: NVIDIA & University of Technology Sydney & Australian National University
- arxiv: [https://arxiv.org/abs/1904.07223](https://arxiv.org/abs/1904.07223)
- github: [https://github.com/NVlabs/DG-Net](https://github.com/NVlabs/DG-Net)
- youtube: [https://www.youtube.com/watch?v=ubCrEAIpQs4](https://www.youtube.com/watch?v=ubCrEAIpQs4)
- bilibili: [https://www.bilibili.com/video/av51439240](https://www.bilibili.com/video/av51439240)

# Human Parsing for Re-ID

**Human Semantic Parsing for Person Re-identification**

- intro: CVPR 2018. SPReID
- arxiv: [https://arxiv.org/abs/1804.00216](https://arxiv.org/abs/1804.00216)
- github: [https://github.com/emrahbasaran/SPReID](https://github.com/emrahbasaran/SPReID)

**Improved Person Re-Identification Based on Saliency and Semantic Parsing with Deep Neural Network Models**

- keywords: Saliency-Semantic Parsing Re-Identification (SSP-ReID)
- arxiv: [https://arxiv.org/abs/1807.05618](https://arxiv.org/abs/1807.05618)

**Identity-Guided Human Semantic Parsing for Person Re-Identification**

- intro: ECCV 2020 spotlight
- arxiv: [https://arxiv.org/abs/2007.13467](https://arxiv.org/abs/2007.13467)
- github: [https://github.com/CASIA-IVA-Lab/ISP-reID](https://github.com/CASIA-IVA-Lab/ISP-reID)

**Human Parsing Based Alignment with Multi-task Learning for Occluded Person Re-identification**

- intro: ICME 2020 Oral
- paper; [https://scihub.wikicn.top/10.1109/ICME46284.2020.9102789](https://scihub.wikicn.top/10.1109/ICME46284.2020.9102789)
- paper: [https://ieeexplore.ieee.org/abstract/document/9102789](https://ieeexplore.ieee.org/abstract/document/9102789)
- github: [https://github.com/huanghoujing/HPNet](https://github.com/huanghoujing/HPNet)

# Partial Person Re-ID

**Partial Person Re-identification**

- intro: ICCV 2015
- arxiv: [https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Zheng_Partial_Person_Re-Identification_ICCV_2015_paper.pdf](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Zheng_Partial_Person_Re-Identification_ICCV_2015_paper.pdf)

**Deep Spatial Feature Reconstruction for Partial Person Re-identification: Alignment-Free Approach**

- intro: CVPR 2018
- intro: Market1501 rank1=83.58%
- keywords: Deep Spatial feature Reconstruction (DSR)
- arxiv: [https://arxiv.org/abs/1801.00881](https://arxiv.org/abs/1801.00881)
- github(official, PyTorch): [https://github.com/lingxiao-he/Partial-Person-ReID](https://github.com/lingxiao-he/Partial-Person-ReID)

**Occluded Person Re-identification**

- intro: ICME 2018
- arxiv: [https://arxiv.org/abs/1804.02792](https://arxiv.org/abs/1804.02792)

**Partial Person Re-identification with Alignment and Hallucination**

- intro: Imperial College London
- keywords: Partial Matching Net (PMN)
- arxiv: [https://arxiv.org/abs/1807.09162](https://arxiv.org/abs/1807.09162)

**SCPNet: Spatial-Channel Parallelism Network for Joint Holistic and Partial Person Re-Identification**

- intro: ACCV 2018
- intro: Megvii Inc. (Face++) & Chinese Academy of Sciences
- arxiv: [https://arxiv.org/abs/1810.06996](https://arxiv.org/abs/1810.06996)
- github: [https://github.com/xfanplus/Open-SCPNet](https://github.com/xfanplus/Open-SCPNet)

**STNReID : Deep Convolutional Networks with Pairwise Spatial Transformer Networks for Partial Person Re-identification**

- intro: Zhejiang University & Megvii Inc
- arxiv: [https://arxiv.org/abs/1903.07072](https://arxiv.org/abs/1903.07072)

**Foreground-aware Pyramid Reconstruction for Alignment-free Occluded Person Re-identification**

[https://arxiv.org/abs/1904.04975](https://arxiv.org/abs/1904.04975)

**A Novel Teacher-Student Learning Framework For Occluded Person Re-Identification**

[https://arxiv.org/abs/1907.03253](https://arxiv.org/abs/1907.03253)

**VRSTC: Occlusion-Free Video Person Re-Identification**

- intro: CVPR 2019
- arxiv: [https://arxiv.org/abs/1907.08427](https://arxiv.org/abs/1907.08427)

**Pose-Guided Feature Alignment for Occluded Person Re-Identification**

- intro: ICCV 2019
- intro: Baidu Research & University of Technology Sydney
- keywords: Pose-Guided Feature Alignment (PGFA)
- paper: [http://openaccess.thecvf.com/content_ICCV_2019/papers/Miao_Pose-Guided_Feature_Alignment_for_Occluded_Person_Re-Identification_ICCV_2019_paper.pdf](http://openaccess.thecvf.com/content_ICCV_2019/papers/Miao_Pose-Guided_Feature_Alignment_for_Occluded_Person_Re-Identification_ICCV_2019_paper.pdf)
- paper: [https://yu-wu.net/pdf/ICCV2019_Occluded-reID.pdf](https://yu-wu.net/pdf/ICCV2019_Occluded-reID.pdf)
- github: [https://github.com/lightas/Occluded-DukeMTMC-Dataset](https://github.com/lightas/Occluded-DukeMTMC-Dataset)

**High-Order Information Matters: Learning Relation and Topology for Occluded Person Re-Identification**

- intro: CVPR 2020
- intro: Institute of Automation, CAS & Megvii Inc. & Beijing Institute of Technology
- arxiv: [https://arxiv.org/abs/2003.08177](https://arxiv.org/abs/2003.08177)
- github: [https://github.com/wangguanan/HOReID](https://github.com/wangguanan/HOReID)

**Pose-guided Visible Part Matching for Occluded Person ReID**

- intro: CVPR 2020
- intro: Dalian University of Technology & Pengcheng Lab & The University of Sydney
- arxiv: [https://arxiv.org/abs/2004.00230](https://arxiv.org/abs/2004.00230)
- github(official, pytorch): [https://github.com/hh23333/PVPM](https://github.com/hh23333/PVPM)

**MHSA-Net: Multi-Head Self-Attention Network for Occluded Person Re-Identification**

- arxiv: [https://arxiv.org/abs/2008.04015](https://arxiv.org/abs/2008.04015)
- github: [https://github.com/hongchenphd/MHSA-Net](https://github.com/hongchenphd/MHSA-Net)

**Holistic Guidance for Occluded Person Re-Identification**

- intro: École de technologie supérieure & Genetec Inc
- arxiv: [https://arxiv.org/abs/2104.06524](https://arxiv.org/abs/2104.06524)

# Cross-modality Re-ID

## RGB-IR Re-ID

**RGB-Infrared Cross-Modality Person Re-Identification**

- intro: ICCV 2017
- paper: [http://openaccess.thecvf.com/content_ICCV_2017/papers/Wu_RGB-Infrared_Cross-Modality_Person_ICCV_2017_paper.pdf](http://openaccess.thecvf.com/content_ICCV_2017/papers/Wu_RGB-Infrared_Cross-Modality_Person_ICCV_2017_paper.pdf)

**RGB-Infrared Cross-Modality Person Re-Identification via Joint Pixel and Feature Alignment**

- intro: ICCV 2019
- keywords: Alignment Generative Adversarial Network (AlignGAN)
- arxiv: [https://arxiv.org/abs/1910.05839](https://arxiv.org/abs/1910.05839)

## Depth-Based Re-ID

**Reinforced Temporal Attention and Split-Rate Transfer for Depth-Based Person Re-Identification**

- intro: ECCV 2018
- arxiv: [http://openaccess.thecvf.com/content_ECCV_2018/papers/Nikolaos_Karianakis_Reinforced_Temporal_Attention_ECCV_2018_paper.pdf](http://openaccess.thecvf.com/content_ECCV_2018/papers/Nikolaos_Karianakis_Reinforced_Temporal_Attention_ECCV_2018_paper.pdf)

**A Cross-Modal Distillation Network for Person Re-identification in RGB-Depth**

[https://arxiv.org/abs/1810.11641](https://arxiv.org/abs/1810.11641)

# Low Resolution Re-ID

**Multi-scale Learning for Low-resolution Person Re-identification**

- intro: ICCV 2015
- arxiv: [https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Li_Multi-Scale_Learning_for_ICCV_2015_paper.pdf](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Li_Multi-Scale_Learning_for_ICCV_2015_paper.pdf)

**Cascaded SR-GAN for Scale-Adaptive Low Resolution Person Re-identification**

- intro: IJCAI 2018
- arxiv: [https://www.ijcai.org/proceedings/2018/0541.pdf](https://www.ijcai.org/proceedings/2018/0541.pdf)

**Deep Low-Resolution Person Re-Identification**

- intro: AAAI 2018
- keywords: Super resolution and Identity joiNt learninG (SING)
- paper: [http://www.eecs.qmul.ac.uk/~xiatian/papers/JiaoEtAl_2018AAAI.pdf](http://www.eecs.qmul.ac.uk/~xiatian/papers/JiaoEtAl_2018AAAI.pdf)

# Reinforcement Learning for Re-ID

**Deep Reinforcement Learning Attention Selection for Person Re-Identification**

- intro: BMVC 2017
- arxiv: [https://arxiv.org/abs/1707.02785](https://arxiv.org/abs/1707.02785)
- paper: [http://www.eecs.qmul.ac.uk/~sgg/papers/LanEtAl_2017BMVC.pdf](http://www.eecs.qmul.ac.uk/~sgg/papers/LanEtAl_2017BMVC.pdf)

# Attributes Prediction for Re-ID

**Multi-Task Learning with Low Rank Attribute Embedding for Person Re-identification**

- intro: ICCV 2015
- paper: [http://legacydirs.umiacs.umd.edu/~fyang/papers/iccv15.pdf](http://legacydirs.umiacs.umd.edu/~fyang/papers/iccv15.pdf)

**Deep Attributes Driven Multi-Camera Person Re-identification**

- intro: ECCV 2016
- arxiv: [https://arxiv.org/abs/1605.03259](https://arxiv.org/abs/1605.03259)

**Improving Person Re-identification by Attribute and Identity Learning**

[https://arxiv.org/abs/1703.07220](https://arxiv.org/abs/1703.07220)

**Person Re-identification by Deep Learning Attribute-Complementary Information**

- intro: CVPR 2017 workshop
- paper: [https://sci-hub.tw/10.1109/CVPRW.2017.186](https://sci-hub.tw/10.1109/CVPRW.2017.186)

**CA3Net: Contextual-Attentional Attribute-Appearance Network for Person Re-Identification**

[https://arxiv.org/abs/1811.07544](https://arxiv.org/abs/1811.07544)

**Attribute analysis with synthetic dataset for person re-identification**

- intro: Shanghai Jiao Tong University
- arxiv: [https://arxiv.org/abs/2006.07139](https://arxiv.org/abs/2006.07139)

**Taking A Closer Look at Synthesis: Fine-grained Attribute Analysis for Person Re-Identification**

- intro: Shanghai Jiao Tong University & National University of Defense Technology
- arxiv: [https://arxiv.org/abs/2010.08145](https://arxiv.org/abs/2010.08145)

# Video Person Re-Identification

**Recurrent Convolutional Network for Video-based Person Re-Identification**

- intro: CVPR 2016
- paper: [http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/McLaughlin_Recurrent_Convolutional_Network_CVPR_2016_paper.pdf](http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/McLaughlin_Recurrent_Convolutional_Network_CVPR_2016_paper.pdf)
- github: [https://github.com/niallmcl/Recurrent-Convolutional-Video-ReID](https://github.com/niallmcl/Recurrent-Convolutional-Video-ReID)

**Deep Recurrent Convolutional Networks for Video-based Person Re-identification: An End-to-End Approach**

[https://arxiv.org/abs/1606.01609](https://arxiv.org/abs/1606.01609)

**Jointly Attentive Spatial-Temporal Pooling Networks for Video-based Person Re-Identification**

- intro: ICCV 2017
- arxiv: [https://arxiv.org/abs/1708.02286](https://arxiv.org/abs/1708.02286)

**Three-Stream Convolutional Networks for Video-based Person Re-Identification**

[https://arxiv.org/abs/1712.01652](https://arxiv.org/abs/1712.01652)

**LVreID: Person Re-Identification with Long Sequence Videos**

[https://arxiv.org/abs/1712.07286](https://arxiv.org/abs/1712.07286)

**Multi-shot Pedestrian Re-identification via Sequential Decision Making**

- intro: CVPR 2018. TuSimple
- keywords: reinforcement learning
- arxiv: [https://arxiv.org/abs/1712.07257](https://arxiv.org/abs/1712.07257)
- github: [https://github.com/TuSimple/rl-multishot-reid](https://github.com/TuSimple/rl-multishot-reid)

**Learning Distributional Representation and Set Distance for Multi-shot Person Re-identification**

- intro: CMU
- arxiv: [https://arxiv.org/abs/1808.01119](https://arxiv.org/abs/1808.01119)

**LVreID: Person Re-Identification with Long Sequence Videos**

[https://arxiv.org/abs/1712.07286](https://arxiv.org/abs/1712.07286)

**Diversity Regularized Spatiotemporal Attention for Video-based Person Re-identification**

- intro: CUHK-SenseTime & Argo AI
- arxiv: [https://arxiv.org/abs/1803.09882](https://arxiv.org/abs/1803.09882)

**Video Person Re-identification with Competitive Snippet-similarity Aggregation and Co-attentive Snippet Embedding**

- intro: CVPR 2018 Poster
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Chen_Video_Person_Re-Identification_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Chen_Video_Person_Re-Identification_CVPR_2018_paper.pdf)

**Exploit the Unknown Gradually: One-Shot Video-Based Person Re-Identification by Stepwise Learning**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Wu_Exploit_the_Unknown_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wu_Exploit_the_Unknown_CVPR_2018_paper.pdf)

**Video Person Re-Identification With Competitive Snippet-Similarity Aggregation and Co-Attentive Snippet Embedding**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Chen_Video_Person_Re-Identification_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Chen_Video_Person_Re-Identification_CVPR_2018_paper.pdf)

**Revisiting Temporal Modeling for Video-based Person ReID**

- arxiv: [https://arxiv.org/abs/1805.02104](https://arxiv.org/abs/1805.02104)
- github: [https://github.com/jiyanggao/Video-Person-ReID](https://github.com/jiyanggao/Video-Person-ReID)

**Video Person Re-identification by Temporal Residual Learning**

[https://arxiv.org/abs/1802.07918](https://arxiv.org/abs/1802.07918)

**A Spatial and Temporal Features Mixture Model with Body Parts for Video-based Person Re-Identification**

[https://arxiv.org/abs/1807.00975](https://arxiv.org/abs/1807.00975)

**Video-based Person Re-identification via 3D Convolutional Networks and Non-local Attention**

- intro: University of Science and Technology of China & University of Chinese Academy of Sciences
- arxiv: [https://arxiv.org/abs/1807.05073](https://arxiv.org/abs/1807.05073)

**Spatial-Temporal Synergic Residual Learning for Video Person Re-Identification**

[https://arxiv.org/abs/1807.05799](https://arxiv.org/abs/1807.05799)

**SCAN: Self-and-Collaborative Attention Network for Video Person Re-identification**

[https://arxiv.org/abs/1807.05688](https://arxiv.org/abs/1807.05688)

**Where-and-When to Look: Deep Siamese Attention Networks for Video-based Person Re-identification**

- intro: IEEE Transactions on Multimedia
- arxiv: [https://arxiv.org/abs/1808.01911](https://arxiv.org/abs/1808.01911)

**STA: Spatial-Temporal Attention for Large-Scale Video-based Person Re-Identification**

- intro: AAAI 2019
- arxiv: [https://arxiv.org/abs/1811.04129](https://arxiv.org/abs/1811.04129)

**Multi-scale 3D Convolution Network for Video Based Person Re-Identification**

- intro: AAAI 2019
- arxiv: [https://arxiv.org/abs/1811.07468](https://arxiv.org/abs/1811.07468)

**Deep Active Learning for Video-based Person Re-identification**

[https://arxiv.org/abs/1812.05785](https://arxiv.org/abs/1812.05785)

**Spatial and Temporal Mutual Promotion for Video-based Person Re-identification**

- intro: AAAI 2019
- arxiv: [https://arxiv.org/abs/1812.10305](https://arxiv.org/abs/1812.10305)

**3D PersonVLAD: Learning Deep Global Representations for Video-based Person Re-identification**

[https://arxiv.org/abs/1812.10222](https://arxiv.org/abs/1812.10222)

**GAN-based Pose-aware Regulation for Video-based Person Re-identification**

- intro: Heriot-Watt University & University of Edinburgh & Queen’s University Belfast & Anyvision
- keywords: Weighted Fusion (WF) & Weighted-Pose Regulation (WPR)
- arxiv: [https://arxiv.org/abs/1903.11552](https://arxiv.org/abs/1903.11552)

**Convolutional Temporal Attention Model for Video-based Person Re-identification**

- intro: ICME 2019
- arxiv: [https://arxiv.org/abs/1904.04492](https://arxiv.org/abs/1904.04492)

**Video Person Re-Identification using Learned Clip Similarity Aggregation**

[https://arxiv.org/abs/1910.08055](https://arxiv.org/abs/1910.08055)

**Video Person Re-ID: Fantastic Techniques and Where to Find Them**

- intro: AAAI 2020
- arxiv: [https://arxiv.org/abs/1912.05295](https://arxiv.org/abs/1912.05295)
- github: [https://github.com/ppriyank/Video-Person-Re-ID-Fantastic-Techniques-and-Where-to-Find-Them](https://github.com/ppriyank/Video-Person-Re-ID-Fantastic-Techniques-and-Where-to-Find-Them)

**Multi-Granularity Reference-Aided Attentive Feature Aggregation for Video-based Person Re-identification**

- intro: CVPR 2020
- intro: 1University of Science and Technology of China & Microsoft Research Asia
- arxiv: [https://arxiv.org/abs/2003.12224](https://arxiv.org/abs/2003.12224)

**Appearance-Preserving 3D Convolution for Video-based Person Re-identification**

- intro: ECCV 2020 Oral
- arxiv: [https://arxiv.org/abs/2007.08434](https://arxiv.org/abs/2007.08434)
- github: [https://github.com/guxinqian/AP3D](https://github.com/guxinqian/AP3D)

**Temporal Complementary Learning for Video Person Re-Identification**

- intro: ECCV 2020
- arxiv: [https://arxiv.org/abs/2007.09357](https://arxiv.org/abs/2007.09357)
- github: [https://github.com/blue-blue272/VideoReID-TCLNet](https://github.com/blue-blue272/VideoReID-TCLNet)

**Reference-Aided Part-Aligned Feature Disentangling for Video Person Re-Identification**

- intro: ICME 2021
- arxiv: [https://arxiv.org/abs/2103.11319](https://arxiv.org/abs/2103.11319)

**Spatial-Temporal Correlation and Topology Learning for Person Re-Identification in Videos**

[https://arxiv.org/abs/2104.08241](https://arxiv.org/abs/2104.08241)

# Re-ranking

**Divide and Fuse: A Re-ranking Approach for Person Re-identification**

- intro: BMVC 2017
- arxiv: [https://arxiv.org/abs/1708.04169](https://arxiv.org/abs/1708.04169)

**Re-ranking Person Re-identification with k-reciprocal Encoding**

- intro: CVPR 2017
- arxiv: [https://arxiv.org/abs/1701.08398](https://arxiv.org/abs/1701.08398)
- github: [https://github.com/zhunzhong07/person-re-ranking](https://github.com/zhunzhong07/person-re-ranking)

**A Pose-Sensitive Embedding for Person Re-Identification with Expanded Cross Neighborhood Re-Ranking**

- intro: CVPR 2018
- arxiv: [https://arxiv.org/abs/1711.10378](https://arxiv.org/abs/1711.10378)
- github(official): [https://github.com/pse-ecn/expanded-cross-neighborhood](https://github.com/pse-ecn/expanded-cross-neighborhood)

**Adaptive Re-ranking of Deep Feature for Person Re-identification**

[https://arxiv.org/abs/1811.08561](https://arxiv.org/abs/1811.08561)

# Unsupervised Re-ID

**Unsupervised Person Re-identification: Clustering and Fine-tuning**

- arxiv: [https://arxiv.org/abs/1705.10444](https://arxiv.org/abs/1705.10444)
- github: [https://github.com/hehefan/Unsupervised-Person-Re-identification-Clustering-and-Fine-tuning](https://github.com/hehefan/Unsupervised-Person-Re-identification-Clustering-and-Fine-tuning)

**Stepwise Metric Promotion for Unsupervised Video Person Re-identification**

- intro: ICCV 2017
- paper: [http://openaccess.thecvf.com/content_ICCV_2017/papers/Liu_Stepwise_Metric_Promotion_ICCV_2017_paper.pdf](http://openaccess.thecvf.com/content_ICCV_2017/papers/Liu_Stepwise_Metric_Promotion_ICCV_2017_paper.pdf)
- github: [https://github.com/lilithliu/StepwiseMetricPromotion-code](https://github.com/lilithliu/StepwiseMetricPromotion-code)

**Dynamic Label Graph Matching for Unsupervised Video Re-Identification**

- intro: ICCV 2017
- arxiv: [https://arxiv.org/abs/1709.09297](https://arxiv.org/abs/1709.09297)
- github: [https://github.com/mangye16/dgm_re-id](https://github.com/mangye16/dgm_re-id)

**Unsupervised Cross-dataset Person Re-identification by Transfer Learning of Spatio-temporal Patterns**

- intro: CVPR 2018
- arxiv: [https://arxiv.org/abs/1803.07293](https://arxiv.org/abs/1803.07293)
- github: [https://github.com/ahangchen/TFusion](https://github.com/ahangchen/TFusion)
- blog: [https://zhuanlan.zhihu.com/p/34778414](https://zhuanlan.zhihu.com/p/34778414)

**Cross-dataset Person Re-Identification Using Similarity Preserved Generative Adversarial Networks**

[https://arxiv.org/abs/1806.04533](https://arxiv.org/abs/1806.04533)

**Unsupervised Cross-dataset Person Re-identification by Transfer Learning of Spatial-Temporal Patterns**

- intro: CVPR 2018
- arxiv: [https://arxiv.org/abs/1803.07293](https://arxiv.org/abs/1803.07293)
- github: [https://github.com/ahangchen/rank-reid](https://github.com/ahangchen/rank-reid)

**Transferable Joint Attribute-Identity Deep Learning for Unsupervised Person Re-Identification**

- intro: CVPR 2018
- arxiv: [https://arxiv.org/abs/1803.09786](https://arxiv.org/abs/1803.09786)

**Adaptation and Re-Identification Network: An Unsupervised Deep Transfer Learning Approach to Person Re-Identification**

- intro: CVPR 2018 workshop. National Taiwan University & Umbo Computer Vision
- keywords: adaptation and re-identification network (ARN)
- arxiv: [https://arxiv.org/abs/1804.09347](https://arxiv.org/abs/1804.09347)

**Domain Adaptation through Synthesis for Unsupervised Person Re-identification**

[https://arxiv.org/abs/1804.10094](https://arxiv.org/abs/1804.10094)

**Unsupervised Domain Adaptive Re-Identification: Theory and Practice**

- intro: Wuhan University & Horizon Robotics & Huazhong Univ. of Science and Technology
- arxiv: [https://arxiv.org/abs/1807.11334](https://arxiv.org/abs/1807.11334)
- github: [https://github.com/LcDog/DomainAdaptiveReID](https://github.com/LcDog/DomainAdaptiveReID)

**Deep Association Learning for Unsupervised Video Person Re-identification**

- intro: BMVC 2018
- arxiv: [https://arxiv.org/abs/1808.07301](https://arxiv.org/abs/1808.07301)

**Support Neighbor Loss for Person Re-Identification**

- intro: ACM Multimedia (ACM MM) 2018
- arxiv: [https://arxiv.org/abs/1808.06030](https://arxiv.org/abs/1808.06030)

**Unsupervised Person Re-identification by Deep Learning Tracklet Association**

- intro: ECCV 2018 Oral
- keywords: Tracklet Association Unsupervised Deep Learning (TAUDL)
- arxiv: [https://arxiv.org/abs/1809.02874](https://arxiv.org/abs/1809.02874)

**Self-similarity Grouping: A Simple Unsupervised Cross Domain Adaptation Approach for Person Re-identification**

- intro: ICCV 2019 oral
- arxiv: [https://arxiv.org/abs/1811.10144](https://arxiv.org/abs/1811.10144)
- github: [https://github.com/OasisYang/SSG](https://github.com/OasisYang/SSG)

**Unsupervised Tracklet Person Re-Identification**

- intro: TPAMI 2019
- arxiv: [https://arxiv.org/abs/1903.00535](https://arxiv.org/abs/1903.00535)
- github: [https://github.com/liminxian/DukeMTMC-SI-Tracklet](https://github.com/liminxian/DukeMTMC-SI-Tracklet)

**Unsupervised Person Re-identification by Deep Asymmetric Metric Embedding**

- intro: TPAMI
- keywords: DEep Clustering-based Asymmetric MEtric Learning (DECAMEL)
- arxiv: [https://arxiv.org/abs/1901.10177](https://arxiv.org/abs/1901.10177)
- github: [https://github.com/KovenYu/DECAMEL](https://github.com/KovenYu/DECAMEL)

**Unsupervised Person Re-identification by Soft Multilabel Learning**

- intro: CVPR 2019 oral
- intro: Sun Yat-sen University & YouTu Lab & Queen Mary University of London
- keywords: MAR (MultilAbel Reference learning), soft multilabel-guided hard negative mining
- project page: [https://kovenyu.com/publication/2019-cvpr-mar/](https://kovenyu.com/publication/2019-cvpr-mar/)
- arxiv: [https://arxiv.org/abs/1903.06325](https://arxiv.org/abs/1903.06325)
- github(official, Pytorch): [https://github.com/KovenYu/MAR](https://github.com/KovenYu/MAR)

**A Bottom-up Clustering Approach to Unsupervised Person Re-identification**

- intro: AAAI 2019 oral
- paper: [https://vana77.github.io/vana77.github.io/images/AAAI19.pdf](https://vana77.github.io/vana77.github.io/images/AAAI19.pdf)
- github: [https://github.com/vana77/Bottom-up-Clustering-Person-Re-identification](https://github.com/vana77/Bottom-up-Clustering-Person-Re-identification)

**A Novel Unsupervised Camera-aware Domain Adaptation Framework for Person Re-identification**

[https://arxiv.org/abs/1904.03425](https://arxiv.org/abs/1904.03425)

**Towards better Validity: Dispersion based Clustering for Unsupervised Person Re-identification**

- arxiv: [https://arxiv.org/abs/1906.01308](https://arxiv.org/abs/1906.01308)
- github: [https://github.com/gddingcs/Dispersion-based-Clustering](https://github.com/gddingcs/Dispersion-based-Clustering)

**PAC-GAN: An Effective Pose Augmentation Scheme for Unsupervised Cross-View Person Re-identification**

[https://arxiv.org/abs/1906.01792](https://arxiv.org/abs/1906.01792)

**Adaptive Exploration for Unsupervised Person Re-Identification**

- arxiv: [https://arxiv.org/abs/1907.04194](https://arxiv.org/abs/1907.04194)
- github: [https://github.com/dyh127/Adaptive-Exploration-for-Unsupervised-Person-Re-Identification](https://github.com/dyh127/Adaptive-Exploration-for-Unsupervised-Person-Re-Identification)

**Learning to Adapt Invariance in Memory for Person Re-identification**

[https://arxiv.org/abs/1908.00485](https://arxiv.org/abs/1908.00485)

**Consistent Cross-view Matching for Unsupervised Person Re-identification**

[https://arxiv.org/abs/1908.10486](https://arxiv.org/abs/1908.10486)

**Learning to Align Multi-Camera Domain for Unsupervised Video Person Re-Identification**

[https://arxiv.org/abs/1909.13248](https://arxiv.org/abs/1909.13248)

**Progressive Unsupervised Person Re-identification by Tracklet Association with Spatio-Temporal Regularization**

[https://arxiv.org/abs/1910.11560](https://arxiv.org/abs/1910.11560)

**Asymmetric Co-Teaching for Unsupervised Cross Domain Person Re-Identification**

- intro: AAAI 2020
- arxiv: [https://arxiv.org/abs/1912.01349](https://arxiv.org/abs/1912.01349)
- github: [https://github.com/FlyingRoastDuck/ACT_AAAI20](https://github.com/FlyingRoastDuck/ACT_AAAI20)

**Memorizing Comprehensively to Learn Adaptively: Unsupervised Cross-Domain Person Re-ID with Multi-level Memory**

[https://arxiv.org/abs/2001.04123](https://arxiv.org/abs/2001.04123)

**Unsupervised Domain Adaptation in the Dissimilarity Space for Person Re-identification**

- intro: ECCV 2020
- arxiv: [https://arxiv.org/abs/2007.13890](https://arxiv.org/abs/2007.13890)

**Unsupervised Attention Based Instance Discriminative Learning for Person Re-Identification**

- intro: WACV 2021
- arxiv: [https://arxiv.org/abs/2011.01888](https://arxiv.org/abs/2011.01888)

**Joint Generative and Contrastive Learning for Unsupervised Person Re-identification**

- arxiv: [https://arxiv.org/abs/2012.09071](https://arxiv.org/abs/2012.09071)
- github: [https://github.com/chenhao2345/GCL](https://github.com/chenhao2345/GCL)

**Joint Noise-Tolerant Learning and Meta Camera Shift Adaptation for Unsupervised Person Re-Identification**

- intro: CVPR 2021
- intro: Xiamen University & University of Trento & Minjiang Universit & Minnan Normal University
- arxiv: [https://arxiv.org/abs/2103.04618](https://arxiv.org/abs/2103.04618)
- github: [https://github.com/FlyingRoastDuck/MetaCam_DSCE](https://github.com/FlyingRoastDuck/MetaCam_DSCE)

**Cluster Contrast for Unsupervised Person Re-Identification**

- intro: Alibaba A.I. Labs & Simon Fraser University
- arxiv: [https://arxiv.org/abs/2103.11568](https://arxiv.org/abs/2103.11568)
- github: [https://github.com/wangguangyuan/ClusterContrast](https://github.com/wangguangyuan/ClusterContrast)

**Intra-Inter Camera Similarity for Unsupervised Person Re-Identification**

- intro: CVPR 2021
- intro: Peking University
- arxiv: [https://arxiv.org/abs/2103.11658](https://arxiv.org/abs/2103.11658)

**Group-aware Label Transfer for Domain Adaptive Person Re-identification**

- intro: CVPR 2021
- arxiv: [https://arxiv.org/abs/2103.12366](https://arxiv.org/abs/2103.12366)

# Weakly Supervised Person Re-identification

**Weakly Supervised Person Re-Identification**

- intro: CVPR 2019
- keywords: multi-instance multi-label learning (MIML), Cross-View MIML (CV-MIML)
- arxiv: [https://arxiv.org/abs/1904.03832](https://arxiv.org/abs/1904.03832)

**Weakly Supervised Person Re-identification: Cost-effective Learning with A New Benchmark**

- keywords: SYSU-30k
- arxiv: [https://arxiv.org/abs/1904.03845](https://arxiv.org/abs/1904.03845)

**Weakly Supervised Tracklet Person Re-Identification by Deep Feature-wise Mutual Learning**

[https://arxiv.org/abs/1910.14333](https://arxiv.org/abs/1910.14333)

# Vehicle Re-ID

**Learning Deep Neural Networks for Vehicle Re-ID with Visual-spatio-temporal Path Proposals**

- intro: ICCV 2017
- arxiv: [https://arxiv.org/abs/1708.03918](https://arxiv.org/abs/1708.03918)

**Viewpoint-Aware Attentive Multi-View Inference for Vehicle Re-Identification**

- intro: CVPR 2018
- paper: [http://openaccess.thecvf.com/content_cvpr_2018/papers/Zhou_Viewpoint-Aware_Attentive_Multi-View_CVPR_2018_paper.pdf](http://openaccess.thecvf.com/content_cvpr_2018/papers/Zhou_Viewpoint-Aware_Attentive_Multi-View_CVPR_2018_paper.pdf)

**RAM: A Region-Aware Deep Model for Vehicle Re-Identification**

- intro: ICME 2018
- arxiv: [https://arxiv.org/abs/1806.09283](https://arxiv.org/abs/1806.09283)

**Vehicle Re-Identification in Context**

- intro: Pattern Recognition - 40th German Conference, (GCPR) 2018, Stuttgart
- project page: [https://qmul-vric.github.io/](https://qmul-vric.github.io/)
- arxiv: [https://arxiv.org/abs/1809.09409](https://arxiv.org/abs/1809.09409)

**Vehicle Re-identification Using Quadruple Directional Deep Learning Features**

[https://arxiv.org/abs/1811.05163](https://arxiv.org/abs/1811.05163)

**Coarse-to-fine: A RNN-based hierarchical attention model for vehicle re-identification**

- intro: ACCV 2018
- arxiv: [https://arxiv.org/abs/1812.04239](https://arxiv.org/abs/1812.04239)

**Vehicle Re-Identification: an Efficient Baseline Using Triplet Embedding**

[https://arxiv.org/abs/1901.01015](https://arxiv.org/abs/1901.01015)

**A Two-Stream Siamese Neural Network for Vehicle Re-Identification by Using Non-Overlapping Cameras**

- intro: ICIP 2019
- arxiv: [https://arxiv.org/abs/1902.01496](https://arxiv.org/abs/1902.01496)

**CityFlow: A City-Scale Benchmark for Multi-Target Multi-Camera Vehicle Tracking and Re-Identification**

- intro: Accepted for oral presentation at CVPR 2019 with review ratings of 2 strong accepts and 1 accept (work done during an internship at NVIDIA)
- arxiv: [https://arxiv.org/abs/1903.09254](https://arxiv.org/abs/1903.09254)

**Vehicle Re-identification in Aerial Imagery: Dataset and Approach**

- intro: Northwestern Polytechnical University
- arxiv: [https://arxiv.org/abs/1904.01400](https://arxiv.org/abs/1904.01400)

**Attributes Guided Feature Learning for Vehicle Re-identification**

[https://arxiv.org/abs/1905.08997](https://arxiv.org/abs/1905.08997)

**A unified neural network for object detection, multiple object tracking and vehicle re-identification**

[https://arxiv.org/abs/1907.03465](https://arxiv.org/abs/1907.03465)

**Part-Guided Attention Learning for Vehicle Re-Identification**

[https://arxiv.org/abs/1909.06023](https://arxiv.org/abs/1909.06023)

**Vehicle Re-identification with Viewpoint-aware Metric Learning**

- intro: ICCV 2019
- intro: Beihang University & Tsinghua University & Megvii Technology
- keywords: Viewpoint-Aware Network (VANet)
- arxiv: [https://arxiv.org/abs/1910.04104](https://arxiv.org/abs/1910.04104)

**PAMTRI: Pose-Aware Multi-Task Learning for Vehicle Re-Identification Using Highly Randomized Synthetic Data**

- intro: ICCV 2019
- arxiv: [https://arxiv.org/abs/2005.00673](https://arxiv.org/abs/2005.00673)
- github: [https://github.com/NVlabs/PAMTRI](https://github.com/NVlabs/PAMTRI)

**Stripe-based and Attribute-aware Network: A Two-Branch Deep Model for Vehicle Re-identification**

[https://arxiv.org/abs/1910.05549](https://arxiv.org/abs/1910.05549)

**Background Segmentation for Vehicle Re-Identification**

[https://arxiv.org/abs/1910.06613](https://arxiv.org/abs/1910.06613)

**Vehicle Re-ID Collection**

[https://github.com/layumi/Vehicle_reID-Collection](https://github.com/layumi/Vehicle_reID-Collection)

**awesome-vehicle-re-identification**

[https://github.com/knwng/awesome-vehicle-re-identification](https://github.com/knwng/awesome-vehicle-re-identification)

**DCDLearn: Multi-order Deep Cross-distance Learning for Vehicle Re-Identification**

[https://arxiv.org/abs/2003.11315](https://arxiv.org/abs/2003.11315)

**Parsing-based View-aware Embedding Network for Vehicle Re-Identification**

- intro: CVPR 2020 poster
- arxiv: [https://arxiv.org/abs/2004.05021](https://arxiv.org/abs/2004.05021)
- github(official): [https://github.com/silverbulletmdc/PVEN](https://github.com/silverbulletmdc/PVEN)

**Multi-Domain Learning and Identity Mining for Vehicle Re-Identification**

- intro: Solution for AI City Challenge, CVPR2020 Workshop
- intro: The 3rd Place Submission to AICity Challenge 2020 Track2
- arxiv: [https://arxiv.org/abs/2004.10547](https://arxiv.org/abs/2004.10547)
- github: [https://github.com/heshuting555/AICITY2020_DMT_VehicleReID](https://github.com/heshuting555/AICITY2020_DMT_VehicleReID)

**VOC-ReID: Vehicle Re-identification based on Vehicle-Orientation-Camera**

- intro: CVPR 2020 workshop, 2nd place solution for AICity2020 Challenge ReID track
- intro: RuiyanAI (睿沿科技)
- arxiv: [https://arxiv.org/abs/2004.09164](https://arxiv.org/abs/2004.09164)
- github: [https://github.com/Xiangyu-CAS/AICity2020-VOC-ReID](https://github.com/Xiangyu-CAS/AICity2020-VOC-ReID)

**VehicleNet: Learning Robust Visual Representation for Vehicle Re-identification**

- intro: The 1st Place Submission to AICity Challenge 2020 re-id track (Baidu-UTS submission)
- arxiv: [https://arxiv.org/abs/2004.06305](https://arxiv.org/abs/2004.06305)
- gtihub: [https://github.com/layumi/AICIty-reID-2020](https://github.com/layumi/AICIty-reID-2020)
- blog: [https://zhuanlan.zhihu.com/p/186905783](https://zhuanlan.zhihu.com/p/186905783)

**Viewpoint-Aware Channel-Wise Attentive Network for Vehicle Re-Identification**

- intro: CVPR Workshop 2020
- arxiv: [https://arxiv.org/abs/2010.05810](https://arxiv.org/abs/2010.05810)

**Self-Supervised Visual Attention Learning for Vehicle Re-Identification**

[https://arxiv.org/abs/2010.09221](https://arxiv.org/abs/2010.09221)

**AttributeNet: Attribute Enhanced Vehicle Re-Identification**

[https://arxiv.org/abs/2102.03898](https://arxiv.org/abs/2102.03898)

**A Strong Baseline for Vehicle Re-Identification**

- intro: CVPR Workshop 2021, 5th AI City Challenge
- intro: Cybercore AI
- arxiv: [https://arxiv.org/abs/2104.10850](https://arxiv.org/abs/2104.10850)
- github: [https://github.com/cybercore-co-ltd/track2_aicity_2021](https://github.com/cybercore-co-ltd/track2_aicity_2021)

# Deep Metric Learning

**Deep Metric Learning for Person Re-Identification**

- intro: ICPR 2014
- paper: [http://www.cbsr.ia.ac.cn/users/zlei/papers/ICPR2014/Yi-ICPR-14.pdf](http://www.cbsr.ia.ac.cn/users/zlei/papers/ICPR2014/Yi-ICPR-14.pdf)

**Deep Metric Learning for Practical Person Re-Identification**

[https://arxiv.org/abs/1407.4979](https://arxiv.org/abs/1407.4979)

**Constrained Deep Metric Learning for Person Re-identification**

[https://arxiv.org/abs/1511.07545](https://arxiv.org/abs/1511.07545)

**Embedding Deep Metric for Person Re-identication A Study Against Large Variations**

- intro: ECCV 2016
- arxiv: [https://arxiv.org/abs/1611.00137](https://arxiv.org/abs/1611.00137)

**DarkRank: Accelerating Deep Metric Learning via Cross Sample Similarities Transfer**

- intro: TuSimple
- keywords: pedestrian re-identification
- arxiv: [https://arxiv.org/abs/1707.01220](https://arxiv.org/abs/1707.01220)

# Projects

**Open-ReID: Open source person re-identification library in python**

- intro: Open-ReID is a lightweight library of person re-identification for research purpose. It aims to provide a uniform interface for different datasets, a full set of models and evaluation metrics, as well as examples to reproduce (near) state-of-the-art results.
- project page: [https://cysu.github.io/open-reid/](https://cysu.github.io/open-reid/)
- github(PyTorch): [https://github.com/Cysu/open-reid](https://github.com/Cysu/open-reid)
- examples: [https://cysu.github.io/open-reid/examples/training_id.html](https://cysu.github.io/open-reid/examples/training_id.html)
- benchmarks: [https://cysu.github.io/open-reid/examples/benchmarks.html](https://cysu.github.io/open-reid/examples/benchmarks.html)

**FastReID: A Pytorch Toolbox for Real-world Person Re-identification**

- intro: SOTA ReID Methods and Toolbox
- intro: JD AI Research
- arxiv: [https://arxiv.org/abs/2006.02631](https://arxiv.org/abs/2006.02631)
- github: [https://github.com/JDAI-CV/fast-reid](https://github.com/JDAI-CV/fast-reid)

**light-reid: a toolbox of light reid for fast feature extraction and search**

- intro: a toolbox of light-reid learning for faster inference, speed both feature extraction and retrieval stages up to >30x
- github: [https://github.com/wangguanan/light-reid](https://github.com/wangguanan/light-reid)

**caffe-PersonReID**

- intro: Person Re-Identification: Multi-Task Deep CNN with Triplet Loss
- gtihub: [https://github.com/agjayant/caffe-Person-ReID](https://github.com/agjayant/caffe-Person-ReID)

**Person_reID_baseline_pytorch**

- intro: Pytorch implement of Person re-identification baseline
- arxiv: [https://github.com/layumi/Person_reID_baseline_pytorch](https://github.com/layumi/Person_reID_baseline_pytorch)

**deep-person-reid**

- intro: Pytorch implementation of deep person re-identification models.
- github: [https://github.com/KaiyangZhou/deep-person-reid](https://github.com/KaiyangZhou/deep-person-reid)

**ReID_baseline**

- intro: Baseline model (with bottleneck) for person ReID (using softmax and triplet loss).
- intro: 一个强力的ReID basemodel
- github: [https://github.com/L1aoXingyu/reid_baseline](https://github.com/L1aoXingyu/reid_baseline)
- blog: [https://zhuanlan.zhihu.com/p/40514536](https://zhuanlan.zhihu.com/p/40514536)

**gluon-reid**

- intro: A code gallery for person re-identification with mxnet-gluon, and I will reproduce many STOA algorithm.
- github: [https://github.com/xiaolai-sqlai/gluon-reid](https://github.com/xiaolai-sqlai/gluon-reid)

**A PyTorch based strong baseline for person search**

[https://github.com/DeepAlchemist/deep-person-search](https://github.com/DeepAlchemist/deep-person-search)

**OpenUnReID**

- intro: PyTorch open-source toolbox for unsupervised or domain adaptive object re-ID
- github: [https://github.com/open-mmlab/OpenUnReID](https://github.com/open-mmlab/OpenUnReID)

# Evaluation

**DukeMTMC-reID**

- intro: The Person re-ID Evaluation Code for DukeMTMC-reID Dataset (Including Dataset Download)
- github: [https://github.com/layumi/DukeMTMC-reID_evaluation](https://github.com/layumi/DukeMTMC-reID_evaluation)

**DukeMTMC-reID_baseline (Matlab)**

[https://github.com/layumi/DukeMTMC-reID_baseline](https://github.com/layumi/DukeMTMC-reID_baseline)

**Code for IDE baseline on Market-1501**

[https://github.com/zhunzhong07/IDE-baseline-Market-1501](https://github.com/zhunzhong07/IDE-baseline-Market-1501)

# Talks

**1st Workshop on Target Re-Identification and Multi-Target Multi-Camera Tracking**

[https://reid-mct.github.io/](https://reid-mct.github.io/)

**Target Re-Identification and Multi-Target Multi-Camera Tracking**

[http://openaccess.thecvf.com/CVPR2017_workshops/CVPR2017_W17.py](http://openaccess.thecvf.com/CVPR2017_workshops/CVPR2017_W17.py)

# Resources

**Re-id Resources**

[https://wangzwhu.github.io/home/re_id_resources.html](https://wangzwhu.github.io/home/re_id_resources.html)

**Person Re-Identification - Papers With Code**

[https://paperswithcode.com/task/person-re-identification](https://paperswithcode.com/task/person-re-identification)

**Awesome Person Re-Identification**

[https://github.com/FDU-VTS/Awesome-Person-Re-Identification](https://github.com/FDU-VTS/Awesome-Person-Re-Identification)
