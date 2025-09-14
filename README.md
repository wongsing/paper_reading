# paper_reading
## 2025.9.14
### 1.LangDAug: Langevin Data Augmentation for Multi-Source Domain Generalization in Medical Image Segmentation(ICML25)
a.域偏移-域泛化（表示学习方法：通过学习域不变特征或解耦域不变 / 特定特征提升泛化性+数据增强方法：通过合成样本丰富模型表征，实现与表示学习相当甚至更优的性能，且实现更简单。）  
b.EBM（能量基模型）训练与域间遍历（采用朗之万动力学（LD）这一基于梯度的马尔可夫链蒙特卡洛（MCMC）方法进行近似采样）-朗之万数据增强，对训练集中每个样本，运行 LD 生成K个中间样本（朗之万样本），与原始样本共同构成增强数据集-模型训练与推理，分割模型（ResNet34 为骨干网络）使用原始样本 + 朗之万样本训练，最终部署到未见过的目标域
