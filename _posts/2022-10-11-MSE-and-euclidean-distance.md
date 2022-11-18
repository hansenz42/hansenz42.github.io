---
layout: post
title: "你还没搞懂 均方误差（MSE） 与欧氏距离 (Euclidean Distance) 的区别吗？"
categories: CHN
---

最近在学习机器学习的 NLP 模型，接触到了词嵌入（word embedding）这个概念。其中提到了词嵌入可以用来做类比推理，在比较两个词向量的相似度时可以使用余弦相似度（Cosine similarity）或者欧氏距离（Euclidean Distance）。在看到使用欧式距离的时候，突然想起在机器学习模型中经常使用的 MSE 也就是均方误差的概念很接近。想深究一下两个概念之间的区别。看了网上的文章，发现没有讲的特别清楚

# 公式

欧氏距离： $ || u - v ||^2 $
表示两个向量之间相减的平方

MSE： $ {1 \over n} \sum_{i=1}^{n} (Y_i - \hat{Y}_i)^2 $
表示所有估计样本和真实样本之间距离之和的平均值

# 理解

如果将机器学习模型 Y 的输出看作是一个向量，那么 MSE 求和的部分就是在求估计样本 Y 和 Y^  之间的欧氏距离。所以可以这么理解，MSE 是机器学习中的一个概念，使用了欧氏距离来衡量模型输出的准确度。

# 参考

[Regression metrics](https://apple.github.io/turicreate/docs/userguide/evaluation/regression.html) 介绍了 RMSE （均方根误差）和欧氏距离的关系，其中提到了RMSE 是使用欧氏距离来计算误差的
