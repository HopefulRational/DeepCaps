# Tensorflow and Keras Implementation of Deep Capsule Neural Networks
Official Implementation of "DeepCaps: Going Deeper with Capsule Networks" paper presented at CVPR 2019.

This code provides deep capsule neural networks (DeepCaps) implemented in Keras with Tensorflow backend. The code supports training the model in multiple GPUs. 

The current `test error on CIFAR10 = 7.26%`.   

## Usage
```
git clone https://github.com/brjathu/deepcaps.git
cd deepcaps
```

## Supported Datasets
 - `CIFAR10`
 - `CIFAR100` 
 - `SVHN` 
 - `F-MNIST`
 - `MNIST`
 - `tiny-imagenet`
 
## Training

If you are training on multiple GPUs change the `numGPU` parameter in `args` class in `train.py` file. 
```
CUDA_VISIBLE_DEVICES=0,1,2,3 python train.py
```

If you are training on single GPU change the `numGPU` parameter in `args` class in `train.py` file to 1.
```
CUDA_VISIBLE_DEVICES=0 python train.py or python train.py
```
To test with several other datasets commnet out the required dataset in the `train.py` file.


## Performance

Dataset | Test error | 
-------|:-------:|
EMNIST-Letters |95.36 ± 0.30% |
EMNIST-Balanced |90.46 ± 0.22% |
EMNIST-Digits |99.79 ± 0.11% |
MNIST |99.71 ± 0.18% |
Fashion MNIST |93.71 ± 0.64% |


## Download pre-trained models and ensemble test

Download this [CIFAR10 - pretrained models](https://drive.google.com/open?id=1Plj-dH4OoSORqWf-23XxToW0X46NdVmR) and extract the files inside model directory. Then run `ensemble.py` file.
```
python ensemble.py
```

## We credit
We have used [this](https://github.com/XifengGuo/CapsNet-Keras) as the base CapsNet implementation. We thank and credit the contributors of this repository.

## Contact
Jathushan Rajasegaran - brjathu@gmail.com  
Discussions, suggestions and questions are welcome!

## References
[1] J. Rajasegaran, V. Jayasundara, S.Jeyasekara, N. Jeyasekara, S. Seneviratne, R. Rodrigo.. "DeepCaps : Going Deeper with Capsule Networks." *Conference on Computer Vision and Pattern Recognition.* 2019. [[arxiv]](https://arxiv.org/abs/1806.07366)

---

If you found this code useful in your research, please consider citing
```
@article{chen2018neural,
  title={DeepCaps : Going Deeper with Capsule Networks},
  author={Jathushan Rajasegaran, Vinoj Jayasundara, Sandaru Jayasekara, Hirunima Jayasekara, Suranga Seneviratne, Ranga Rodrigo},
  journal={Conference on Computer Vision and Pattern Recognition},
  year={2019}
}
```
