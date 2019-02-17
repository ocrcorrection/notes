---

---

# **源码学习笔记**

## **源码书写整体架构思路**







## **具体模块介绍**

### **readme.md**

~~~
This repository includes the implementation of the method from our paper. It is implemented via tensorflow 1.9.0. Please use the following citation.

# 论文相关信息
@inproceedings{dong2018multi, title={Multi-Input Attention for Unsupervised OCR Correction}, author={Dong, Rui and Smith, David}, booktitle={Proceedings of the 56th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)}, volume={1}, pages={2363--2372}, year={2018} }

It contains the following file:

util.py: basic functions used by other scripts.其他脚本使用的基本函数

data_tokenize.py: create the vocabulary and tokenize the data.创建词汇表，并且标记数据

flag.py: configuration of the model.模型的配置

model.py: model construction. 模型的构建

model_attn.py: attntion model with different variations of attention combination strategies.具有不同变化的注意力组合策略的attention模型

train.py: train the model.训练模型

decode.py: decode the model.解码模型
~~~

### **data_generate_train_noisy.py**



~~~

~~~



### **data_generate_train_synthetic.py**



### **data_processing**.py





### **data_tokenize.py**





### **decode.py**



### **flag.py**





### **model.py**





### **model_attn.py**



### train.py



### **utils.py**



