# **数据生成：阶段一**

**数据生成时间：**2019/04/15

## 数据来源

### **汉字**

3900个常用汉字，其中包括一个空格

|        | 最常用字       | 较常用字       | 最不常用字     | 总数    |
| ------ | -------------- | -------------- | -------------- | ------- |
| 总数   | 1000           | 1000           | 1900           |         |
| 训练集 | 2000*1000(62M) | 1500*1000(47M) | 1000*1900(9M)  | 5400000 |
| 测试集 | 200*1000(6.2M) | 150*1000(4.7M) | 100*1900(5.9M) | 540000  |

### **汉字字体**

- 微软宋体：SimSun
- 微软黑体：SimHei
- 微软仿宋：fangsong_GB2312
- 微软雅黑：msyh

### **标点符号**

| 总数 | 训练集  | 测试集 |
| ---- | ------- | :----- |
| 29   | 29*2000 | 29*100 |
|      | 58000   | 2900   |

~~~
. point
。 period
， comma
: colon
; semicolon
； semicolon
！ exclamation
? question
“ left_quotation
” right_quotation
( left_parenthesis
) right_parenthesis
[ left_square_bracket
] right_square_bracket
《 left_quotes
》 right_quotes
- dash
< less_than
> greater_than
= equal
+ add
% percent
# hash_tag
* asterisk
@ at
/ slash
  space
￥ cny
$ usd
~~~



### **数字字母**

| 总数 | 训练集  | 测试集 |
| ---- | ------- | :----- |
| 62   | 62*2000 | 62*100 |
|      | 124000  | 6200   |

### **总数据**

训练集：5400000+58000+124000= 5582000

测试集：540000+2900+6200 = 549100

## **数据存放**

- 38服务器 290端口
- /usr/local/src/data/stage3/all_3991

![ ](https://raw.githubusercontent.com/yaolinxia/img_resource/master/multi-input attention/微信截图_20190422145437.png)



### **存在问题**

- 缺少

# 数据生成：阶段二

**数据生成时间：**2019/04/22

## 数据来源

7000+35+62=7097

### **汉字**

7000个常用汉字，其中包括一个空格

|        | 最常用字       | 较常用字               | 最不常用字                    | 总数    |
| ------ | -------------- | ---------------------- | ----------------------------- | ------- |
| 总数   | 2500           | 2000                   | 2500                          |         |
| 训练集 | 1000*2500(78M) | 900*2000(56M)[1:38:10] | 800*2500=200000(62M)[1:51:09] | 6300000 |
| 测试集 | 200*2500(16M)  | 90*2000(5.6M)          | 80*2500(6.2M)[0:10:27]        | 880000  |

### **字体库路径**

- ` C:\Windows\Fonts`

### **汉字字体**

- 微软宋体：SimSun
- 微软黑体：SimHei
- 微软仿宋：fangsong_GB2312
- 微软雅黑：msyh
- 华文楷体：STKAITI
- 华文中宋：STZHONGS



### **英文字体**

- Times New Roman常规：times.ttf
- Times New Roman粗体：timesbd.ttf
- Arial常规：arial.ttf
- Calibri常规：calibri.ttf

> 新下载的字体，存放在H:\python-workspace\ocr_postcorrection\data\字体

### **标点符号**

- 在原来的基础上，添加了6个

~~~
、 stop
【 left_bracket
】 right_bracket
〔 left_bracket
〕 right_bracket
～ wave_pattern
~~~



| 总数 | 训练集        | 测试集       |
| ---- | ------------- | :----------- |
| 35   | 35*1000(1.2M) | 35*100(120K) |
|      | 35000         | 3500         |

### **数字字母**

> 训练数据一样，加入了一些英文的字体

| 总数 | 训练集           | 测试集       |
| ---- | ---------------- | :----------- |
| 62   | 62*1000(1.5M)    | 62*100(148K) |
|      | 62000（1分44秒） | 6200         |

### **总数据**

训练集：6300000+35000+62000= 6397000

测试集：880000+3500+6200 = 889700

### **配置文件**

configs/single_char_7097.yaml



## **数据存放**

- 38服务器 290端口
- /usr/local/src/data/stage3/





