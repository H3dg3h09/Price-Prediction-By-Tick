# 基于 Tick 数据的**单只股票**价格趋势预测

_>_ 对算法的初步探索, 不具有交易指导意义

## 模型使用

- LSMT 对应文件 lstm.ipynb
- CatBoost 对应文件 final.ipynb

\*cm.ipynb 为中间文件, 可以忽略

## 调试尝试

1. **五折交叉验证**（5-fold cross-validation）:通常用于模型选择和调参，而不是用于最终的模型训练。交叉验证的主要目的是评估模型在未见过的数据上的表现，以防止过拟合，并选择最优的模型参数。
2. **网格搜索**（Grid Search）: 主要用于系统地遍历模型的多种参数组合，通过交叉验证确定最佳效果参数。它的工作原理是，你先为每一个输入参数选择一个小的有限集，然后网格搜索会穷举各种参数组合，找出在验证集上评分最高的参数组合。

## 模型判断

1. 使用测试集和训练的*均方误差* 比值作为评判标准, 越和 1 靠近越优
2. 曲线状态

## 结果

训练集
![image](https://github.com/H3dg3h09/Price-Prediction-By-Tick/blob/main/output/cat_res_tarin.png)
测试集
![image](https://github.com/H3dg3h09/Price-Prediction-By-Tick/blob/main/output/cat_res_test.png)
