## **数据**

- [ ] **网上OCR相关数据集总结**<https://www.cnblogs.com/lillylin/p/6893500.html>

- [ ] **论文数据集以及源码**<http://www.ccs.neu.edu/home/dongrui/ocr.html>

- [ ] **中文数据集**

  <https://github.com/HCIILAB/SCUT_FORU_DB_Release>


## **论文**

- **2017-2018_ocr论文汇总：**<https://www.cnblogs.com/lillylin/p/9954858.html>
- **ocr 论文**：<https://handong1587.github.io/deep_learning/2015/10/09/ocr.html>

### OCR矫正方面论文【参考文献中提到】

#### **集成方法**

ensemble methods have been shown to be effective in ocr postcorrection by combining ocr output from multiple scans of the same document

集成方法通过将来自同一文档的多次扫描的OCR输出组合起来，在OCR后校正中被证明是有效的。

#### **监督方法**

existing methods aim at generating consensus results by aligning multiple inputs, followed by supervised methods such as classification

现有方法旨在通过对多个输入进行对齐来生成共识结果，然后通过诸如分类的监督方法来生成共识结果

#### 非监督方法

基于字典的选择和投票

> 监督学习，需要人工标记，用来训练
>
> 非监督的选择方法，只有在其中一个输入中存在正确的单词或者字符时，才能工作
>
> 总的来说，这些方法不能纠正单输入

#### **多输入attention**

- 多输入attention在机器翻译，文本摘要中已经有所探究（连接多个输入生成摘要）

- flat attention combination 可能会受输入序列的顺序影响

- [x] Shaobin Xu and David A. Smith. 2017. **Retrieving and** 
  **combining repeated passages to improve OCR**. In
  JCDL.(**重复文本使用**)(**投票**)【杨】

  > 重复文本和近重复的文本在很多语料库中会出现。所以OCR的输出，因为质量的不同，会存在很多的重复文本

#### Multi - attention

- [x] Jindˇrich Libovick´y and Jindˇrich Helcl. 2017. **Attention**
  **strategies for multi-source sequence-to-sequence**
  **learning**. In ACL. 【姚】
- [ ] Barret Zoph and Kevin Knight. 2016. Multi-source
  neural translation. In NAACL.

#### 基线纠正

- [x] David A. Smith, Ryan Cordell, Elizabeth Maddock
  Dillon, Nick Stramp, and John Wilkerson. 2014.
  **Detecting and modeling local text reuse**. In JCDL.【熊】


#### 其他

- [ ] Guillaume Chiron, Antoine Doucet, Mickael Coustaty,
  Muriel Visani, and Jean-Philippe Moreux. 2017.
  Impact of OCR errors on the use of digital libraries:
  Towards a better access to information. In JCDL.(严重的错误会妨碍可访问性)
- [ ] Mike Schuster and Kuldip K. Paliwal. 1997. Bidirectional
  recurrent neural networks. IEEE Transactions
  on Signal Processing, 45(11):2673–2681.
- [ ] Sepp Hochreiter and J¨urgen Schmidhuber. 1997.
  Long short-term memory. Neural Computation,
  9(8):1735–1780.
- [ ] Daniel Lopresti and Jiangying Zhou. 1997. Using consensus
  sequence voting to correct OCR errors. Computer
  Vision and Image Understanding, 67(1):39–

  **[download error]**

### **OCR矫正方面论文【参考文献中未提到】**

#### **2018**

- [x] [Jie Mei](https://dblp.uni-trier.de/pers/hd/m/Mei:Jie), [Aminul Islam](https://dblp.uni-trier.de/pers/hd/i/Islam:Aminul), [Abidalrahman Moh'd](https://dblp.uni-trier.de/pers/hd/m/Moh=d:Abidalrahman), [Yajing Wu](https://dblp.uni-trier.de/pers/hd/w/Wu:Yajing), [Evangelos E. Milios](https://dblp.uni-trier.de/pers/hd/m/Milios:Evangelos_E=):
  Statistical learning for OCR error correction. [Inf. Process. Manage.54(6)](https://dblp.uni-trier.de/db/journals/ipm/ipm54.html#MeiIMWM18): 874-887 (2018)【姚】

  > 使用了丰富的语料库，结合丰富的语义特征集合，设计了一套矫正管道，采用了一种可以更好处理边界模糊的标记化方法

- [x] [Kareem Mokhtar](https://dblp.uni-trier.de/pers/hd/m/Mokhtar:Kareem), [Syed Saqib Bukhari](https://dblp.uni-trier.de/pers/hd/b/Bukhari:Syed_Saqib), [Andreas Dengel](https://dblp.uni-trier.de/pers/hd/d/Dengel:Andreas):
  OCR Error Correction: State-of-the-Art vs an NMT-based Approach. [DAS2018](https://dblp.uni-trier.de/db/conf/das/das2018.html#MokhtarBD18): 429-434【熊】

  > 两种新颖的促进OCR系统准确度的深度学习方法，和一个能够进一步加强输出结果质量的后处理技巧
  >
  > 采用**归一化技术**，基于字符的模型

- [x] [Ewerton Cappelatti](https://dblp.uni-trier.de/pers/hd/c/Cappelatti:Ewerton), [Regina de Oliveira Heidrich](https://dblp.uni-trier.de/pers/hd/h/Heidrich:Regina_de_Oliveira), [Ricardo Oliveira](https://dblp.uni-trier.de/pers/hd/o/Oliveira:Ricardo), [Cíntia Monticelli](https://dblp.uni-trier.de/pers/hd/m/Monticelli:C=iacute=ntia), [Ronaldo Rodrigues](https://dblp.uni-trier.de/pers/hd/r/Rodrigues:Ronaldo), [Rodrigo Goulart](https://dblp.uni-trier.de/pers/hd/g/Goulart:Rodrigo), [Eduardo Velho](https://dblp.uni-trier.de/pers/hd/v/Velho:Eduardo):
  Post-correction of OCR Errors Using PyEnchant Spelling Suggestions Selected Through a Modified Needleman-Wunsch Algorithm. [HCI (28) 2018](https://dblp.uni-trier.de/db/conf/hci/hci2018-28.html#CappelattiHOMRG18): 3【杨】[B刊]

  > 提出了一种改进的再匹配算法
  >
  > 提出了一个spellchecker的方法
  >
  > 适用于英文，可能中文不是很适用

- [x] [David Smith](https://dblp.uni-trier.de/pers/hd/s/Smith:David), [Rui Dong](https://dblp.uni-trier.de/pers/hd/d/Dong:Rui):
  Multi-Input Attention for Unsupervised OCR Correction. [ACL (1) 2018](https://dblp.uni-trier.de/db/conf/acl/acl2018-1.html#SmithD18): 2363-2372

  > 利用重复文本进行无监督的训练学习

- [x] [Yang He](https://dblp.uni-trier.de/pers/hd/h/He_0003:Yang), [Jingling Yuan](https://dblp.uni-trier.de/pers/hd/y/Yuan:Jingling), [Lin Li](https://dblp.uni-trier.de/pers/hd/l/Li:Lin):
  Enhancing RNN Based OCR by Transductive Transfer Learning From Text to Images. [AAAI 2018](https://dblp.uni-trier.de/db/conf/aaai/aaai2018.html#HeYL18): 8083-8084

  > 角度新颖，从OCR模型训练的速度提高上，加速了OCR的识别，以及避免了重复

- [ ] [Stephen Mutuvi](https://dblp.uni-trier.de/pers/hd/m/Mutuvi:Stephen), [Antoine Doucet](https://dblp.uni-trier.de/pers/hd/d/Doucet:Antoine), [Moses Odeo](https://dblp.uni-trier.de/pers/hd/o/Odeo:Moses), [Adam Jatowt](https://dblp.uni-trier.de/pers/hd/j/Jatowt:Adam):
  Evaluating the Impact of OCR Errors on Topic Modeling. [ICADL 2018](https://dblp.uni-trier.de/db/conf/icadl/icadl2018.html#MutuviDOJ18): 3-14

- [x] [Vivi Nastase](https://dblp.uni-trier.de/pers/hd/n/Nastase:Vivi), [Julian Hitschler](https://dblp.uni-trier.de/pers/hd/h/Hitschler:Julian):
  Correction of OCR Word Segmentation Errors in Articles from the ACL Collection through Neural Machine Translation Methods. [LREC 2018](https://dblp.uni-trier.de/db/conf/lrec/lrec2018.html#NastaseH18) 

  > 数据集，来自ACL的论文
  >
  > 针对的问题是OCR识别后的分词错误

- [x] [Iyad Abu Doush](https://dblp.uni-trier.de/pers/hd/d/Doush:Iyad_Abu), [Faisal Alkhateeb](https://dblp.uni-trier.de/pers/hd/a/Alkhateeb:Faisal), [Anwaar Hamdi Gharaibeh](https://dblp.uni-trier.de/pers/hd/g/Gharaibeh:Anwaar_Hamdi):
  A novel Arabic OCR post-processing using rule-based and word context techniques. [IJDAR 21(1-2)](https://dblp.uni-trier.de/db/journals/ijdar/ijdar21.html#DoushAG18): 77-89 (2018)【C期刊】

  > 提出了一种新的对齐算法-快速自动文本对齐算法

- [x] [Christian Reul](https://dblp.uni-trier.de/pers/hd/r/Reul:Christian), [Uwe Springmann](https://dblp.uni-trier.de/pers/hd/s/Springmann:Uwe), [Christoph Wick](https://dblp.uni-trier.de/pers/hd/w/Wick:Christoph), [Frank Puppe](https://dblp.uni-trier.de/pers/hd/p/Puppe:Frank):
  Improving OCR Accuracy on Early Printed Books by Utilizing Cross Fold Training and Voting. [DAS 2018](https://dblp.uni-trier.de/db/conf/das/das2018.html#ReulSWP18): 423-428

  > 利用交叉训练和投票，改善在早期打印书本上的OCR准确率， 不同的OCR模型会产生不同的OCR文本， 经过投票，决定最终的输出



#### **2017**

- [ ] [Diego Mollá Aliod](https://dblp.uni-trier.de/pers/hd/a/Aliod:Diego_Moll=aacute=), [Steve Cassidy](https://dblp.uni-trier.de/pers/hd/c/Cassidy:Steve):
  Overview of the 2017 ALTA Shared Task: Correcting OCR Errors. [ALTA 2017](https://dblp.uni-trier.de/db/conf/acl-alta/acl-alta2017.html#AliodC17): 115-118
- [ ] [Axel Jean-Caurant](https://dblp.uni-trier.de/pers/hd/j/Jean=Caurant:Axel), [Cyrille Suire](https://dblp.uni-trier.de/pers/hd/s/Suire:Cyrille), [Vincent Courboulay](https://dblp.uni-trier.de/pers/hd/c/Courboulay:Vincent), [Jean-Christophe Burie](https://dblp.uni-trier.de/pers/hd/b/Burie:Jean=Christophe):
  Limiter L'Impact Des Erreurs OCR Sur Les Représentations Distribuées De Mots. [DH 2017](https://dblp.uni-trier.de/db/conf/dihu/dh2017.html#Jean-CaurantSCB17)
- [ ] [Rohit Saluja](https://dblp.uni-trier.de/pers/hd/s/Saluja:Rohit), [Devaraj Adiga](https://dblp.uni-trier.de/pers/hd/a/Adiga:Devaraj), [Parag Chaudhuri](https://dblp.uni-trier.de/pers/hd/c/Chaudhuri:Parag), [Ganesh Ramakrishnan](https://dblp.uni-trier.de/pers/hd/r/Ramakrishnan:Ganesh), [Mark James Carman](https://dblp.uni-trier.de/pers/hd/c/Carman:Mark_James):
  Error Detection and Corrections in Indic OCR Using LSTMs. [ICDAR 2017](https://dblp.uni-trier.de/db/conf/icdar/icdar2017.html#SalujaACRC17): 17-22
- [ ] [Rohit Saluja](https://dblp.uni-trier.de/pers/hd/s/Saluja:Rohit), [Devaraj Adiga](https://dblp.uni-trier.de/pers/hd/a/Adiga:Devaraj), [Ganesh Ramakrishnan](https://dblp.uni-trier.de/pers/hd/r/Ramakrishnan:Ganesh), [Parag Chaudhuri](https://dblp.uni-trier.de/pers/hd/c/Chaudhuri:Parag), [Mark James Carman](https://dblp.uni-trier.de/pers/hd/c/Carman:Mark_James):
  A Framework for Document Specific Error Detection and Corrections in Indic OCR. [OST@ICDAR 2017](https://dblp.uni-trier.de/db/conf/icdar/ost2017.html#SalujaARCC17): 25-30
- [ ] [Guillaume Chiron](https://dblp.uni-trier.de/pers/hd/c/Chiron:Guillaume), [Antoine Doucet](https://dblp.uni-trier.de/pers/hd/d/Doucet:Antoine), [Mickaël Coustaty](https://dblp.uni-trier.de/pers/hd/c/Coustaty:Micka=euml=l), [Muriel Visani](https://dblp.uni-trier.de/pers/hd/v/Visani:Muriel), [Jean-Philippe Moreux](https://dblp.uni-trier.de/pers/hd/m/Moreux:Jean=Philippe):
  Impact of OCR Errors on the Use of Digital Libraries: Towards a Better Access to Information. [JCDL 2017](https://dblp.uni-trier.de/db/conf/jcdl/jcdl2017.html#ChironDCVM17): 249-252

#### **2016**

- [ ] [Haithem Afli](https://dblp.uni-trier.de/pers/hd/a/Afli:Haithem), [Loïc Barrault](https://dblp.uni-trier.de/pers/hd/b/Barrault:Lo=iuml=c), [Holger Schwenk](https://dblp.uni-trier.de/pers/hd/s/Schwenk:Holger):
  OCR Error Correction Using Statistical Machine Translation. [Int. J. Comput. Linguistics Appl. 7(1)](https://dblp.uni-trier.de/db/journals/ijcla/ijcla7.html#AfliBS16): 175-191 (2016)
- [ ] [Eva D'hondt](https://dblp.uni-trier.de/pers/hd/d/D=hondt:Eva), [Cyril Grouin](https://dblp.uni-trier.de/pers/hd/g/Grouin:Cyril), [Brigitte Grau](https://dblp.uni-trier.de/pers/hd/g/Grau:Brigitte):
  Low-resource OCR error detection and correction in French Clinical Texts.[Louhi@EMNLP 2016](https://dblp.uni-trier.de/db/conf/acl-louhi/acl-louhi2016.html#DhondtGG16): 61-68
- [ ] [Mariam Muhammad](https://dblp.uni-trier.de/pers/hd/m/Muhammad:Mariam), [Tarek Elghazaly](https://dblp.uni-trier.de/pers/hd/e/Elghazaly:Tarek), [Mostafa Ezzat](https://dblp.uni-trier.de/pers/hd/e/Ezzat:Mostafa), [Mervat Gheith](https://dblp.uni-trier.de/pers/hd/g/Gheith:Mervat):
  A Spell Correction Model for OCR Errors for Arabic Text. [AISI 2016](https://dblp.uni-trier.de/db/conf/aisi/aisi2016.html#MuhammadEEG16): 124-136
- [ ] [Ido Kissos](https://dblp.uni-trier.de/pers/hd/k/Kissos:Ido), [Nachum Dershowitz](https://dblp.uni-trier.de/pers/hd/d/Dershowitz:Nachum):
  OCR Error Correction Using Character Correction and Feature-Based Word Classification. [DAS 2016](https://dblp.uni-trier.de/db/conf/das/das2016.html#KissosD16): 198-203
- [ ] [V. S. Vinitha](https://dblp.uni-trier.de/pers/hd/v/Vinitha:V=_S=), [C. V. Jawahar](https://dblp.uni-trier.de/pers/hd/j/Jawahar:C=_V=):
  Error Detection in Indic OCRs. [DAS 2016](https://dblp.uni-trier.de/db/conf/das/das2016.html#VinithaJ16): 180-185
- [ ] [Haithem Afli](https://dblp.uni-trier.de/pers/hd/a/Afli:Haithem), [Zhengwei Qiu](https://dblp.uni-trier.de/pers/hd/q/Qiu:Zhengwei), [Andy Way](https://dblp.uni-trier.de/pers/hd/w/Way:Andy), [Páraic Sheridan](https://dblp.uni-trier.de/pers/hd/s/Sheridan:P=aacute=raic):
  Using SMT for OCR Error Correction of Historical Texts. [LREC 2016](https://dblp.uni-trier.de/db/conf/lrec/lrec2016.html#AfliQWS16)
- [ ] [Ido Kissos](https://dblp.uni-trier.de/pers/hd/k/Kissos:Ido), [Nachum Dershowitz](https://dblp.uni-trier.de/pers/hd/d/Dershowitz:Nachum):
  OCR Error Correction Using Character Correction and Feature-Based Word Classification. [CoRR abs/1604.06225](https://dblp.uni-trier.de/db/journals/corr/corr1604.html#KissosD16) (2016)

#### **2015**

- [ ] [Xiaoping Wang](https://dblp.uni-trier.de/pers/hd/w/Wang:Xiaoping), [Yanghua Xiao](https://dblp.uni-trier.de/pers/hd/x/Xiao:Yanghua), [Wei Wang](https://dblp.uni-trier.de/pers/hd/w/Wang_0009:Wei):
  Web Knowledge Base Improved OCR Correction for Chinese Business Cards. [WAIM 2015](https://dblp.uni-trier.de/db/conf/waim/waim2015.html#WangXW15): 573-576 【**C会**】

#### 2014

- [ ] [Mayce Ibrahim Ali Al Azawi](https://dblp.uni-trier.de/pers/hd/a/Azawi:Mayce_Ibrahim_Ali_Al), [Thomas M. Breuel](https://dblp.uni-trier.de/pers/hd/b/Breuel:Thomas_M=):
  Context-Dependent Confusions Rules for Building Error Model Using Weighted Finite State Transducers for OCR Post-Processing. [Document Analysis Systems 2014](https://dblp.uni-trier.de/db/conf/das/das2014.html#AzawiB14): 116-120
- [ ] [Günter Mühlberger](https://dblp.uni-trier.de/pers/hd/m/M=uuml=hlberger:G=uuml=nter), [Johannes Zelger](https://dblp.uni-trier.de/pers/hd/z/Zelger:Johannes), [David Sagmeister](https://dblp.uni-trier.de/pers/hd/s/Sagmeister:David):
  User-driven correction of OCR errors: combing crowdsourcing and information retrieval technology. [DATeCH 2014](https://dblp.uni-trier.de/db/conf/datech/datech2014.html#MuhlbergerZS14): 53-56
- [ ] [William B. Lund](https://dblp.uni-trier.de/pers/hd/l/Lund:William_B=), [Eric K. Ringger](https://dblp.uni-trier.de/pers/hd/r/Ringger:Eric_K=), [Daniel David Walker](https://dblp.uni-trier.de/pers/hd/w/Walker:Daniel_David):
  How well does multiple OCR error correction generalize? [DRR 2014](https://dblp.uni-trier.de/db/conf/drr/drr2014.html#LundRW14): 90210A-90210A-13
- [ ] [Kazem Taghva](https://dblp.uni-trier.de/pers/hd/t/Taghva:Kazem), [Shivam Agarwal](https://dblp.uni-trier.de/pers/hd/a/Agarwal:Shivam):
  Utilizing web data in identification and correction of OCR errors. [DRR 2014](https://dblp.uni-trier.de/db/conf/drr/drr2014.html#TaghvaA14): 902109-902109-6
- [ ] **[Jinying Chen](https://dblp.uni-trier.de/pers/hd/c/Chen:Jinying), [Yue Wu](https://dblp.uni-trier.de/pers/hd/w/Wu_0001:Yue), [Huaigu Cao](https://dblp.uni-trier.de/pers/hd/c/Cao:Huaigu), [Prem Natarajan](https://dblp.uni-trier.de/pers/hd/n/Natarajan:Prem):**
  **Confusion Network Based Recurrent Neural Network Language Modeling for Chinese OCR Error Detection. [ICPR 2014](https://dblp.uni-trier.de/db/conf/icpr/icpr2014.html#ChenWCN14): 1266-1271  ** 【C会】

#### **2013**

- [ ] [Daniel David Walker](https://dblp.uni-trier.de/pers/hd/w/Walker:Daniel_David), [Eric K. Ringger](https://dblp.uni-trier.de/pers/hd/r/Ringger:Eric_K=), [Kevin D. Seppi](https://dblp.uni-trier.de/pers/hd/s/Seppi:Kevin_D=):
  Evaluating supervised topic models in the presence of OCR errors. [DRR2013](https://dblp.uni-trier.de/db/conf/drr/drr2013.html#WalkerRS13): 865812

#### **2012**

- [ ] [Yuen-Hsien Tseng](https://dblp.uni-trier.de/pers/hd/t/Tseng:Yuen=Hsien):
  Error correction in a Chinese OCR test collection. [SIGIR 2002](https://dblp.uni-trier.de/db/conf/sigir/sigir2002.html#Tseng02): 429-430

