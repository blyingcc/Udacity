项目背景：
基于客户生命周期价值理论，为了实现用户价值最大化，降低用户流失率一直是众多企业关心的问题。本项目基于sparkify音乐APP的海量真实用户日志文件进行分析。旨在通过多维度特征的用户画像分析，构造模型，对流失用户进行预测。由于文件量级较大，scikit-learn 等很难高效处理。基于分布式技术的Spark可以很好解决该问题，并通过pyspark.ml库实现用户流失预测模型。

数据来源：
数据来源于Sparkify音乐APP的用户日志文件，格式为JOSON,迷你集128M，亚马逊AWS集群数据高达12G。日志包含18个字段，描述用户各个时间戳的相关操作日志。

 |-- artist: string (nullable = true)
 |-- auth: string (nullable = true)
 |-- firstName: string (nullable = true)
 |-- gender: string (nullable = true)
 |-- itemInSession: long (nullable = true)
 |-- lastName: string (nullable = true)
 |-- length: double (nullable = true)
 |-- level: string (nullable = true)
 |-- location: string (nullable = true)
 |-- method: string (nullable = true)
 |-- page: string (nullable = true)
 |-- registration: long (nullable = true)
 |-- sessionId: long (nullable = true)
 |-- song: string (nullable = true)
 |-- status: long (nullable = true)
 |-- ts: long (nullable = true)
 |-- userAgent: string (nullable = true)
 |-- userId: string (nullable = true)


需要安装的包：
pyspark，主要应用pyspark.ml，pyspark.sql.建议数据集较大在Amazon AWS云平台进行模型训练。


定义问题：
通过日志文件提取用户的各项特征，并用具体指标实现，基于这些指标构造模型，预测用户是否会流失。这是一个二分类的预测问题。

评估指标：
用户流失预测需要综合考虑准确率、召回率，采用F1和准确率两个指标综合衡量。

项目要点：
数据清理-进行日志时间戳的转换，设置用户标签，空值、重复值、异常值的检查处理；
可视化和数据探索性分析来-分析用户详细的行为特征，尤其是流失用户的具体操作。运用可视化探索流失用户与非流失用户在各项特征的分布规律；
特征的构造、数据集的转换-基于用户的各项特征进行用户-特征标签数据集的构造，包括用户性别、级别、注册日期、页面关键按钮操作频率、互动频率、产品的丰富度、产品使用频次、在线时间分布、忠实度等；
评估指标的选择-f1和准确度；
算法的选择-基于数据集维度、量级的特点，选择逻辑回归、决策树、随机森林进行预训练；
模型训练-采用IBM云平台进行在线分布式训练；
模型调优；
模型评估、结果的呈现；
通过模型参数，查看到影响用户流失最大的三个因素。

这是Udacity数据挖掘纳米学位最后一个项目，感谢8个月时间里，各位老师和同学的支持和鼓励。数据连通我们，也连同世界。
