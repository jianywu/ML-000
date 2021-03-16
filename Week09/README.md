学习笔记
测试了衍生变量对结果的影响。
因为时间有点来不及，所以把learning_rate的值选择偏大一些，rounds减少，叶子节点数目也减少了。
kFold选择了5折，而且做shuffle。
期间用seaborn的distplot检查了原始数据的直方图及核密度。
ACC => 0.91804 lightgbm默认模型。
ACC => 0.9177  衍生变量Binning_rate + term * grade
ACC => 0.91804 衍生变量Binning_loan_amnt + binning_annual_income + Binning_dti
