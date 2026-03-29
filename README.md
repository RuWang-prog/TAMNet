# TAMNet: Triple Adaptive Multiplexing Network for Wide-Area Infrared Small Target Detection
[点击这里查看文章](https://www.sciencedirect.com/science/article/pii/S0925231226007204)
![Alt text](Fig.1.jpg)
# Requirements
Python 3<br>
pytorch 1.2.0 or higher<br>
numpy, PIL, tqdm, shutil<br>
# Algorithm Introduction
We propose a triple adaptive multiplexing network (TAMNet) for wide-area infrared small target detection (WIRSTD) in this paper. Experiments on the dataset provided by the PRCV2024 Wide Area Infrared Small Target Detection Challenge (hereafter PRCV2024) demonstrate the effectiveness of our method. The contributions can be summarized as follows:<br>
1. We propose TAMNet featuring dedicated adaptive multiplexing strategies in feature extraction, contextual understanding, and prediction generation to achieve exceptional cross-domain generalization for WIRSTD.<br>
2. We propose a novel attention-decoupled parallel attention residual block (PARB) module that adaptively integrates multi-branch features to maximally preserve and reinforce subtle features while effectively mitigating cross-domain feature distortion induced by attention mechanisms.<br>
3. We propose local saliency module (LSM) as a replacement for the skip connections (SK) to handle complex background variations by explicitly modeling multi-scale context to implicitly derive stable targetbackground relationships.<br>
# Commands
## Commands for train
Run `trainVMDNAL.py` to perform network training in single GPU and multiple GPUs.

Checkpoints and Logs will be saved to `./log/`, and the `./log/` has the following structure:
```
├──./log/
│    ├── PRCV2024 
│    │    ├── VMDNAL_eopch400.pth.tar
```
## Commands for test
Run `testVMDNAL.py` to perform network inference and evaluation. 
The PA/mIoU and PD/FA values will be saved to ./test_[current time].txt
Network predictions will be saved to `./results/` that has the following structure:
```
├──./results/
│    ├── PRCV2024
│    │   ├── VMDNAL
│    │   │    ├── XXX.png
```
# Recources
The pre-trained models can be downlaod via [Baidu Drive](https://pan.baidu.com/s/1tVihrj5e50SbhtHITsiCSg?pwd=8mj5) (key:8mj5) and [One Drive](https://1drv.ms/u/c/be18513de13ace81/IQBNdZohOEbfRLdhKKlfwNydAXqD5jp_dWpUDKYk-bpsE4A?e=ZXsliw).
# Citation
If you find the code useful, please consider citing our paper using the following BibTeX entry.
```
@article{WANG2026133323,
title = {TAMNet: Triple adaptive multiplexing network for wide-area infrared small target detection},
journal = {Neurocomputing},
volume = {681},
pages = {133323},
year = {2026},
issn = {0925-2312},
author = {Ru Wang and Fanglong Wu and Yadong Chen and Peng Cheng},
}
```

