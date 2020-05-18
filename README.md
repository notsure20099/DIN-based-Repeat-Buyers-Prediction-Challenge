# 基于DIN模型的，天池-淘宝复购预测比赛解决方案
## 比赛资料
[比赛链接]（https://tianchi.aliyun.com/competition/entrance/231576/introduction）  
## 环境配置所需依赖库
* deepctr
* scikit-learn
* numpy
* pandas
* xgboost
## 2.步骤说明
(1)原始数据集包含了不同用户在一月到八月间的购买行为以及订单资料，为了构建训练集，需要将八月的购买行为单独划分出来作为标签。  
(2)进行数据预处理(包括缺失值填充，归一化，独热编码等)，以及特征工程(针对时间特征做rfm模型处理等)  
(3)分别采用xgboost和DNN进行训练和预测，其中DNN采用百度Paddle框架搭建。  
(4)模型融合输出结果  
## 3.文件说明
原始数据train.csv  
基于原始数据打标签以及特征工程文件data_feature_project.ipynb  
模型1:xgboost以及模型训练和预测结果xgboost_predict.ipynb  
模型2:基于百度paddle框架的DNN搭建，以及DNN模型训练和预测paddle_DNN_predict.ipynb  
基于两种模型的模型融合结果输出xgboost_DNN_predict.ipynb  
