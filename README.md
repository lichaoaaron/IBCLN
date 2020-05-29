Single Image Reflection Removal through Cascaded Refinement  
========================================

Code and data for the Paper:

**[Single Image Reflection Removal through Cascaded Refinement  ][1]**\
Chao Li, Yixiao Yang, Kun He, Stephen Lin, John E. Hopcroft\
[CVPR 2020]



Introduction
---------------------------

Our main contributions are as follows:
1) We propose a new network architecture, a cascaded network, with loss components that achieves state-of-the-art quantitative results on real-world benchmarks for the single image reflection removal problem.  
2) We design a residual reconstruction loss, which can form a closed loop with the linear method for synthesizing images with reflections, to expand the influence of the synthesis method across the whole network.  
3) We collect a new real-world dataset containing images with densely-labeled ground-truth, which can serve as baseline data in future research. 



Requisites
-----------------------------

* PyTorch
  Use the instructions that are outlined on [PyTorch Homepage][2] for installing PyTorch for your operating system
* Python 3
* Linux
* CPU or NVIDIA GPU + CUDA CuDNN



<a name="someid"></a> Datasets and Designing the experiments
----------------------------------------------------------------

For the training data, we use 4000 images containing 2800 synthetic images and
1200 image patches of size 256 × 256 from 290 real-world training images, containing 200 images from our created dataset and 90 images from [Zhang et al.][3].  For the testing data, we use five real-world datasets, including three sub-datasets from [SIR][4], [Zhang et al.][3] and our dataset [Nature][5].



Description of the files in this repository
---------------------------------------------------

1) ``train.py``: Execute this file to train the model 
2) ``test.py``: Execute this file to test the model 
3) ``model/model.py``: Contains the classes defining the model
4) ``model/networks.py``: Contains the function that defining the model
5) ``options/base_options.py``: This file contains the basic options
6) ``options/train_options.py``: This file contains the options for training
7) ``options/test_options.py``: This file contains the options for testing


Training
------------------------------

To begin the training process , use the **`train.py`** file. Simply execute the following lines to begin the training process

```sh
python train.py
```



Evaluating the model
-------------------------------

To begin the testing process , use the **`test.py`** file. Simply execute the following lines to begin the testing process

```sh
python test.py
```



## Citation

If you find this code and data useful, please consider citing the original work by authors:

```
@article{li2019single,
  title={Single Image Reflection Removal through Cascaded Refinement},
  author={Li, Chao and Yang, Yixiao and He, Kun and Lin, Stephen and Hopcroft, John E},
  journal={arXiv preprint arXiv:1911.06634},
  year={2019}
}
```



License
-------

BSD

[1]: https://arxiv.org/pdf/1911.06634.pdf
[2]: http://pytorch.org/docs/master
[3]: https://drive.google.com/drive/folders/1NYGL3wQ2pRkwfLMcV2zxXDV8JRSoVxwA
[4]: http://rose1.ntu.edu.sg/Datasets/sir2Benchmark.asp
[5]: unfinished
[6]: 