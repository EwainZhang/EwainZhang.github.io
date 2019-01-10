
# 文本分类任务
## 基本框架
text->Feature engineering->classifier->class

## Feature engineering
Extract text features
+ Classic text features
+ Construct new features
+ Extract from neural network

Classic text features
1. TF
2. TFIDF
3. Doc2vec
4. Word2vec


Construct new features:
1. 寻找可能影响分类的新特征：例如文章的长度
2. 人工构造可能影响分类的新特征：$(x, y, z)--> (x, y, z, xy, xz, yz)$


Neural networks:
神经网络=特征提取器+分类器
文本量级达到百万时deep learning superior to tradition learning


Features selection:
reasons:
减弱维数灾难，计算量减少
降低学习任务难度

methods：(详见西瓜书)
1. 包裹式
2. 嵌入式
3. 过滤式


Dimesionality reductionn:
+ supervised(using class information of sample): LDA 
+ unsupervised: LSA, Ida, NMF


Classifier:
1.sklearn: LR, SVM, Nbais, random forest, bagging
2.Lightgbm ( HAng LI's statistic learning 8.4.3)
3.xgboost
4.netural network


models fussion:（西瓜书第八章）
+ fussion methods
1.  投票法
2.  学习法

key: 训练多个好而不同的单模型
