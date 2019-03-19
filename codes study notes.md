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

## **数据处理部分**

### **data_generate_train_noisy.py**

##### **寻找witness**





### **data_generate_train_synthetic.py**

**语料库的插入，删除，替换 ——>  纠错**



### data_processing.py

**数据的拆分，生成x, y, z**

![ ](https://raw.githubusercontent.com/yaolinxia/img_resource/master/multi-input attention/微信截图_20190302105722.png)

~~~python
out_x = open(out_fn + '.x', 'w')                    # output file for OCR'd text
out_y = open(out_fn + '.y', 'w')                    # output file for duplicated texts (witnesses)
out_z = open(out_fn + '.z', 'w')                    # output file for manual transcription
# output file for the information of OCR'd text, each line contains:
# (group no., line no., file_id, begin index in file, end index in file, number of witnesses, number of manual transcriptions)
out_x_info = open(out_fn + '.x.info', 'w')
    
# output file for the information of each witness, each line contains:
# (line no, file_id, begin index in file)
out_y_info = open(out_fn + '.y.info', 'w')

# output file for the information of each manual transcription,
# each line contains: (line no, file_id, begin index in file)
out_z_info = open(out_fn + '.z.info', 'w')
~~~





### **data_tokenize.py**

**数据单元化，标记化**

**创建了Vocabulary**

## **模型部分**

> 主要看train, train调用其他各个部分

### **decode.py**



### **flag.py**

**模型的配置**



### **model.py**





### **model_attn.py**



### train.py

**inputs:**

```
训练数据
x_train = pjoin(FLAGS.data_dir, 'train.ids.x')
y_train = pjoin(FLAGS.data_dir, 'train.ids.y')
验证数据
x_dev = pjoin(FLAGS.data_dir, FLAGS.dev + '.ids.x')
y_dev = pjoin(FLAGS.data_dir, FLAGS.dev + '.ids.y')
词汇表
vocab_path = pjoin(FLAGS.voc_dir, "vocab.dat")
模型， epoch
model, epoch = create_model(sess, vocab_size, False)

```

### **utils.py**



## **kenlm**

- <https://zhuanlan.zhihu.com/p/39722203>
- 服务器上已安装，pip

### 介绍

- 训练语言模型

