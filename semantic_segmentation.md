# 语义分割

## 描述

语义分割是密集预测任务，其设定预测输入图像的每个像素的类标签的目标。通常，分割算法的目的是计算具有等于输入的空间分辨率的标签图。

通常的评估指标是：

- 联盟上的平均交点（mIoU）：每类IoU的平均值= TP /（TP + FP + FN）其中TP，FP，FN - 真实阳性，假阳性，评估集中像素的假阴性预测
- 像素精度
- 平均精度
- 两者结合

## 结果

**注意**：ADE20K数据集的评估是通过计算像素精度的平均值和并集上的平均交点来完成的。

### PASCAL VOC 2012 - 验证集

[数据集描述](datasets/pascal_voc_2012_segmentation.md)

| Model                          | Score | Weights                                                      | Paper                                     | Code                                                         |
| ------------------------------ | ----- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------------ |
| SDN-M2* + COCO + MS            | 88.80 | N/A                                                          | [paper](https://arxiv.org/abs/1708.04943) | N/A                                                          |
| DeepLab_v3-Xception-65 + COCO  | 83.58 | [TensorFlow](http://download.tensorflow.org/models/deeplabv3_pascal_train_aug_2018_01_04.tar.gz) | [paper](https://arxiv.org/abs/1706.05587) | [TensorFlow](https://github.com/tensorflow/models/tree/master/research/deeplab) |
| ResNet-38 Model A1-2 + COCO    | 82.86 | [MXNet](https://cloudstor.aarnet.edu.au/plus/index.php/s/JKWePbLPlpfRDW4) | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| ResNet-38 Model A2-2           | 80.84 | N/A                                                          | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| SDN-M3                         | 79.90 | N/A                                                          | [paper](https://arxiv.org/abs/1708.04943) | N/A                                                          |
| DeepLab_v2                     | 79.00 | [Caffe](https://bitbucket.org/aquariusjay/deeplab-public-ver2) | [paper](https://arxiv.org/abs/1606.00915) | [Caffe](https://bitbucket.org/aquariusjay/deeplab-public-ver2) |
| ResNet-38 Model A1-2           | 78.76 | N/A                                                          | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| ResNet-38 Model A2-1           | 78.14 | N/A                                                          | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| DeepLab_v3-MobileNet-v2 + COCO | 77.33 | [TensorFlow](http://download.tensorflow.org/models/deeplabv3_mnv2_pascal_train_aug_2018_01_29.tar.gz) | [paper](https://arxiv.org/abs/1706.05587) | [TensorFlow](https://github.com/tensorflow/models/tree/master/research/deeplab) |

### PASCAL VOC 2012 — 测试集

[数据描述](datasets/pascal_voc_2012_segmentation.md)

| Model                          | Score | Weights                                                      | Paper                                     |                             Code                             |
| ------------------------------ | ----- | ------------------------------------------------------------ | ----------------------------------------- | :----------------------------------------------------------: |
| DeepLab_v3-Xception-65 + COCO  | 87.80 | [TensorFlow](http://download.tensorflow.org/models/deeplabv3_pascal_trainval_2018_01_04.tar.gz) | [paper](https://arxiv.org/abs/1706.05587) | [TensorFlow](https://github.com/tensorflow/models/tree/master/research/deeplab) |
| SDN-M3 + COCO                  | 86.60 | N/A                                                          | [paper](https://arxiv.org/abs/1708.04943) |                             N/A                              |
| EncNet-ResNet-101 + COCO       | 85.90 | N/A                                                          | [paper](https://arxiv.org/abs/1803.08904) | [PyTorch](https://github.com/zhanghang1989/PyTorch-Encoding) |
| PSPNet-ResNet-101 + COCO       | 85.60 | [Caffe](https://drive.google.com/open?id=0BzaU285cX7TCNVhETE5vVUdMYk0) | [paper](https://arxiv.org/abs/1612.01105) |          [Caffe](https://github.com/hszhao/PSPNet)           |
| ResNet-38 Model A1-2 + COCO    | 84.90 | [MXNet](https://cloudstor.aarnet.edu.au/plus/index.php/s/YqNptRcboMD44Kd) | [paper](https://arxiv.org/abs/1611.10080) |         [MXNet](https://github.com/itijyou/ademxapp)         |
| SDN-M3                         | 83.50 | N/A                                                          | [paper](https://arxiv.org/abs/1708.04943) |                             N/A                              |
| RefineNet-ResNet-152           | 83.40 | [MatConvNet](https://drive.google.com/open?id=1SMROCLfXldmCFnkCcCDyGWB0BSrttDMw) | [paper](https://arxiv.org/abs/1611.06612) |     [MatConvNet](https://github.com/guosheng/refinenet)      |
| EncNet-ResNet-101 + MS         | 82.90 | N/A                                                          | [paper](https://arxiv.org/abs/1803.08904) | [PyTorch](https://github.com/zhanghang1989/PyTorch-Encoding) |
| PSPNet-ResNet-101              | 82.60 | [Caffe](https://drive.google.com/open?id=0BzaU285cX7TCNVhETE5vVUdMYk0) | [paper](https://arxiv.org/abs/1612.01105) |          [Caffe](https://github.com/hszhao/PSPNet)           |
| RefineNet-ResNet-101           | 82.40 | [MatConvNet](https://drive.google.com/open?id=1zaPvO9GRLWaEX9F_7puM5h7_CxOeNkfq) | [paper](https://arxiv.org/abs/1611.06612) |     [MatConvNet](https://github.com/guosheng/refinenet)      |
| DeepLab_v3-MobileNet-v2 + COCO | 80.25 | [TensorFlow](http://download.tensorflow.org/models/deeplabv3_mnv2_pascal_trainval_2018_01_29.tar.gz) | [paper](https://arxiv.org/abs/1706.05587) | [TensorFlow](https://github.com/tensorflow/models/tree/master/research/deeplab) |

### PASCAL Context

[数据描述](datasets/pascal_context.md)

| Model                  | Score | Weights                                                      | Paper                                     | Code                                                         |
| ---------------------- | ----- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------------ |
| EncNet-ResNet-101 + MS | 52.60 | [PyTorch](https://hangzh.s3.amazonaws.com/encoding/models/encnet_resnet101_pcontext-6f7c3722.zip) | [paper](https://arxiv.org/abs/1803.08904) | [PyTorch](https://github.com/zhanghang1989/PyTorch-Encoding) |
| EncNet-ResNet-101      | 51.70 | [PyTorch](https://hangzh.s3.amazonaws.com/encoding/models/encnet_resnet101_pcontext-6f7c3722.zip) | [paper](https://arxiv.org/abs/1803.08904) | [PyTorch](https://github.com/zhanghang1989/PyTorch-Encoding) |
| ResNet-38 Model A2-2   | 48.10 | N/A                                                          | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| RefineNet-ResNet-152   | 47.30 | [MatConvNet](https://drive.google.com/open?id=1eGEhsG0qCbsots5PCS6lLgVSKsHba1-M) | [paper](https://arxiv.org/abs/1611.06612) | [MatConvNet](https://github.com/guosheng/refinenet)          |
| RefineNet-ResNet-101   | 47.10 | [MatConvNet](https://drive.google.com/open?id=1v5MDf0_TBx4XLTEMR3mMNvnYDPacW9_o) | [paper](https://arxiv.org/abs/1611.06612) | [MatConvNet](https://github.com/guosheng/refinenet)          |
| DeepLab_v2             | 45.70 | [Caffe](https://bitbucket.org/aquariusjay/deeplab-public-ver2) | [paper](https://arxiv.org/abs/1606.00915) | [Caffe](https://bitbucket.org/aquariusjay/deeplab-public-ver2) |

### ADE20K — 验证集

[数据描述](datasets/ade20k.md)

| Model                             | Score | Weights                                                      | Paper                                     | Code                                                         |
| --------------------------------- | ----- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------------ |
| DeepLab_v3-Xception-65 + ImageNet | 64.08 | [TensorFlow](http://download.tensorflow.org/models/deeplabv3_xception_ade20k_train_2018_05_29.tar.gz) | [paper](https://arxiv.org/abs/1706.05587) | [TensorFlow](https://github.com/tensorflow/models/tree/master/research/deeplab) |
| PSPNet-ResNet-269 + MS            | 63.31 | N/A                                                          | [paper](https://arxiv.org/abs/1612.01105) | [Caffe](https://github.com/hszhao/PSPNet)                    |
| EncNet-ResNet-101                 | 63.17 | N/A                                                          | [paper](https://arxiv.org/abs/1803.08904) | [PyTorch](https://github.com/zhanghang1989/PyTorch-Encoding) |
| ResNet-38 Model A2-2              | 62.45 | N/A                                                          | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| PSPNet-ResNet-269                 | 62.34 | N/A                                                          | [paper](https://arxiv.org/abs/1612.01105) | [Caffe](https://github.com/hszhao/PSPNet)                    |
| ResNet-38 Model A1-2              | 61.56 | [MXNet](https://cloudstor.aarnet.edu.au/plus/index.php/s/E4JeZpmssK50kpn) | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| PSPNet-ResNet-50                  | 60.86 | [Caffe](https://drive.google.com/open?id=0BzaU285cX7TCN1R3QnUwQ0hoMTA) | [paper](https://arxiv.org/abs/1612.01105) | [Caffe](https://github.com/hszhao/PSPNet)                    |
| EncNet-ResNet-50                  | 60.42 | [PyTorch](https://github.com/Lextal/SotA-CV/blob/master/content/encoding/models/encnet_resnet50_ade-558e8904.zip) | [paper](https://arxiv.org/abs/1803.08904) | [PyTorch](https://github.com/zhanghang1989/PyTorch-Encoding) |

### ADE20K — 测试集

[数据描述](datasets/ade20k.md)

| Model                  | Score | Weights | Paper                                     | Code                                                         |
| ---------------------- | ----- | ------- | ----------------------------------------- | ------------------------------------------------------------ |
| ResNet-38 Model A2-2   | 56.41 | N/A     | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| EncNet-ResNet-101 + MS | 55.67 | N/A     | [paper](https://arxiv.org/abs/1803.08904) | [PyTorch](https://github.com/zhanghang1989/PyTorch-Encoding) |
| PSPNet-ResNet-101      | 55.38 | N/A     | [paper](https://arxiv.org/abs/1612.01105) | [Caffe](https://github.com/hszhao/PSPNet)                    |

### Cityscapes — 验证集

[数据描述](datasets/cityscapes_semantic.md)

| Model                             | Score | Weights                                                      | Paper                                     | Code                                                         |
| --------------------------------- | ----- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------------ |
| ResNet-38 Model A2-2              | 80.60 | N/A                                                          | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| DeepLab_v3-Xception-65 + ImageNet | 80.42 | [TensorFlow](http://download.tensorflow.org/models/deeplabv3_cityscapes_train_2018_02_06.tar.gz) | [paper](https://arxiv.org/abs/1706.05587) | [TensorFlow](https://github.com/tensorflow/models/tree/master/research/deeplab) |
| ResNet-38 Model A1-2              | 78.08 | [MXNet](https://cloudstor.aarnet.edu.au/plus/index.php/s/2hbvpro6J4XKVIu) | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| ResNet-38 Model A2-1              | 77.18 | N/A                                                          | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| DeepLab_v3-MobileNet-v2 + COCO    | 73.57 | [TensorFlow](http://download.tensorflow.org/models/deeplabv3_cityscapes_train_2018_02_06.tar.gz) | [paper](https://arxiv.org/abs/1706.05587) | [TensorFlow](https://github.com/tensorflow/models/tree/master/research/deeplab) |

### Cityscapes — Testing set

[数据描述](datasets/cityscapes_semantic.md)

| Model                             | Score | Weights                                                      | Paper                                     | Code                                                         |
| --------------------------------- | ----- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------------ |
| DeepLab_v3-ResNet-101 + COCO + MS | 82.70 | N/A                                                          | [paper](https://arxiv.org/abs/1706.05587) | [TensorFlow](https://github.com/tensorflow/models/tree/master/research/deeplab) |
| PSPNet-ResNet-101 + COCO          | 80.20 | [Caffe](https://drive.google.com/file/d/0BzaU285cX7TCT1M3TmNfNjlUeEU/view) | [paper](https://arxiv.org/abs/1612.01105) | [Caffe](https://github.com/hszhao/PSPNet)                    |
| DeepLab_v3-ResNet-101             | 78.51 | N/A                                                          | [paper](https://arxiv.org/abs/1706.05587) | [TensorFlow](https://github.com/tensorflow/models/tree/master/research/deeplab) |
| ResNet-38 Model A2-2              | 78.40 | N/A                                                          | [paper](https://arxiv.org/abs/1611.10080) | [MXNet](https://github.com/itijyou/ademxapp)                 |
| PSPNet-ResNet-101                 | 78.40 | [Caffe](https://drive.google.com/file/d/0BzaU285cX7TCT1M3TmNfNjlUeEU/view) | [paper](https://arxiv.org/abs/1612.01105) | [Caffe](https://github.com/hszhao/PSPNet)                    |
| RefineNet-ResNet-101              | 73.60 | [MatConvNet](https://drive.google.com/open?id=17Fv9FZQLqfeyurbYJ7QJ-DC4HZBue9LA) | [paper](https://arxiv.org/abs/1611.06612) | [MatConvNet](https://github.com/guosheng/refinenet)          |