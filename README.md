# 我的论文阅读列表

推荐系统 广告算法 CTR预估 CVR预估

---

### Recommender Systems

 - [《Deep Neural Networks for YouTube Recommendations》](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/45530.pdf)
 - [《Wide & Deep Learning for Recommender Systems》](http://delivery.acm.org/10.1145/2990000/2988454/p7-cheng.pdf?ip=111.193.50.224&id=2988454&acc=OA&key=4D4702B0C3E38B35%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35%2E5945DC2EABF3343C&__acm__=1529772374_349403d9ca8b561f9ba275c2702d17cd)

    LR是CTR预估最经典的一个模型，具有简单、高效和解释性强等特点，但是线性模型的表达能力有限，虽然可以通过交叉特征的方式让LR学到一些非线性特征，但是人工交叉特征成本很高，并且还要求算法工程师对所从事的业务有着很深的理解，才能做好特征工程，此外当需要交叉高阶特征时，再强的专家也很难实现，现实的业务中特征数量会很多，一旦交叉很可能会出现特征爆炸的情况。
    这篇文章提出了一个wide&deep模型可以有效的解决传统LR存在的缺点，整个模型分成wide和deep两部分：（1）wide部分就是传统的LR，主要学习一些可以被解释的线性特征和一些交叉特征；（2）deep部分就是一个DNN网络，DNN可以有效的学习到特征之间的相互作用，尤其是可以学习到高阶特征交互，并且可以增加embeddings层处理高维稀疏特征。最后将wide和deep两部分组合在一起经过sigmoid函数输出，显著地提升了模型的效果。

### CTR Prediction
 - [《Ad Click Prediction: a View from the Trenches》](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/41159.pdf)
 - [《DeepFM: A Factorization-Machine based Neural Network for CTR Prediction》](https://arxiv.org/abs/1703.04247)
 - [《Practical Lessons from Predicting Clicks on Ads at Facebook》](http://quinonero.net/Publications/predicting-clicks-facebook.pdf)
 - [《Deep & Cross Network for Ad Click Predictions》](https://arxiv.org/abs/1708.05123)