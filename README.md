# Adaptive Discriminative Region Discovery for Scene Recognition

By [Zhengyu Zhao](https://zhengyuzhao.github.io/).

Radboud University (RU).

### Introduction

This repository contains the codes for Adi-Red approach described in the paper [From Volcano to Toyshop: Adaptive Discriminative Region
Discovery for Scene Recognition](). This approach achieved state-of-the-art performance in terms of Top-1 classification accuracy on the scene benchmark [SUN397](https://groups.csail.mit.edu/vision/SUN/), by discovering discriminative local image patches efficiently. 

**Note**

### Citation

If you use this approach in your research, please cite:

	@article{Zhao2018,
		author = {Zhengyu Zhao and Martha Larson},
		title = {From Volcano to Toyshop: Adaptive Discriminative Region Discovery for Scene Recognition},
		Booktitle={ACM Multimedia},
		Year={2018}
	}


### Results
1. Visualization of discriminative patches (smallest-scale) discovered by Adi-Red on Places365-Standard validation set. Specially, some patches (from "airfield", "bathroom" and "Japanese garden") convey object-level information. Other patches (from "baseball field" and "campsite") capture contextual semantics, i.e., the interaction between object parts and their surroundings. In another case, non-objectness patterns are captured successfully for the scenes (such as "crosswalk" and "beach"), where finding nameable objects (for example, people and cars in the crosswalk scene) based on region proposals is redundant and might even introduce confusion instead of contributing to their discriminative properties.


![patches](https://github.com/ZhengyuZhao/Adaptive-Discriminative-Region-Discovery/blob/master/figures/discriminative_patches_final.jpg)





2. We use the multi-scale deep features generated by our approach to train a linear SVM classifier with parameter C fixed for all the     implementations.
Top-1 accuracy on SUN397: 

	Networks|Baseline|Adi-Red
	:---:|:---:|:---:
	AlexNet|54.17%|61.01%
	ResNet-18|66.96%|70.58%
	ResNet-50|71.38%|73.59%
	

	

