# JoCaD

The full code will be made public after the paper is published

# Abstract

Noisy labels due to mistakes in manual labeling or data collecting are challenging for the expansion of deep neural network applications. Current robust network learning methods such as Decoupling, Co-teaching, and Joint Training with Co-Regularization are very promising for learning with noisy labels, yet the coordination between consistency and diversity is not fully considered which is crucial for the performance of the model. To tackle this issue, a novel robust learning paradigm called Joint training by combining Consistency and Diversity (JoCaD) is proposed in this paper. The JoCaD is devoted to maximize the prediction consistency of the networks while keeping enough diversity on their representation learning. Specifically, aiming to reconcile the relationship between consistency and diversity, an effective implementation is proposed which dynamically adjusts joint loss to boost the model learning with noisy labels. The extensive experimental results on MNIST, CIFAR-10, CIFAR-100, and Clothing1M demonstrate that our proposed JoCaD has better performance than some representative SOTA methods.

## Data
The MNIST and CIFAR datasets are publicly available, so we have written the data download method into the code and simply run the code to download the dataset. As for clothing1M, please contact tong.xiao.work@gmail.com to request the download link.

## The setting of Tg on benchmark datasets from symmetrical 20% to 80% and asymmetrical 40% (MNIST, CIFAR-10, CIFAR-100 and Clothing1M)
For MNIST, Tg is 10, 10, 10 and 25.
For CIFAR-10, Tg is 5, 10, 20 and 20.
For CIFAR-100, Tg is 10, 10, 25 and 20.
For Clothing1m, Tg is 10.

## Running JoCaD on benchmark datasets (MNIST, CIFAR-10, CIFAR-100 and Clothing1M)
Here is an example: 

```bash
python main.py --dataset cifar100 --noise_type symmetric --noise_rate 0.8 --co_lambda 0.85 --beta 0.01 --turning_point 25
```
