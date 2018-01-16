# Kaggle-Grocery-Sales-Forecasting-rank-33th-
A silver solution for https://www.kaggle.com/c/favorita-grocery-sales-forecasting

这是我做的第二个时序相关的比赛，Kaggle第一块银牌，public榜68，private榜33，top 2%，美滋滋啊~

在kernel区下载了一份当时分最高的kernel（public榜0.513），然后开始做特征工程：
- 删掉了一些cv上没有提分的特征
- min、max、方差、偏度、峰度
- 均值的一阶差分
- 指数衰减的求和
- item和store类别特征的onehot编码和种类计数（参考了Porto比赛第二名的解决方案）

最后，看大家都在说可能会有大的shake up出现，为以防万一，训练模型时采用的是4个lightgbm种子融合的方法（还是参考了Porto比赛第二名的解决方案），private榜还是很稳的~

kaggle讨论区：https://www.kaggle.com/c/favorita-grocery-sales-forecasting/discussion/47537
kaggle kernel区：https://www.kaggle.com/deepdreamer/a-silver-solution-33rd