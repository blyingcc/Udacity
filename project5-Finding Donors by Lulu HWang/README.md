# 机器学习纳米学位
# 监督学习
## 项目: 为CharityML寻找捐献者
### 安装

这个项目需要安装下面这些python包：

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [matplotlib](http://matplotlib.org/)


### 数据

修改的人口普查数据集含有将近32,000个数据点，每一个数据点含有13个特征。这个数据集是Ron Kohavi的论文*"Scaling Up the Accuracy of Naive-Bayes Classifiers: a Decision-Tree Hybrid",*中数据集的一个修改版本。你能够在[这里](https://www.aaai.org/Papers/KDD/1996/KDD96-033.pdf)找到论文，在[UCI的网站](https://archive.ics.uci.edu/ml/datasets/Census+Income)找到原始数据集。

**特征**

- `age`: 一个整数，表示被调查者的年龄。 
- `workclass`: 一个类别变量表示被调查者的通常劳动类型，允许的值有 {Private（个人）, Self-emp-not-inc（无限责任公司）, Self-emp-inc（有限责任公司）, Federal-gov（联邦政府）, Local-gov（地方政府）, State-gov（州政府）, Without-pay（无薪人员）, Never-worked（未从业者）}
- `education_level`: 一个类别变量表示教育程度，允许的值有 {Bachelors（学士）, Some-college（大学未毕业）, 11th, HS-grad（高中毕业）, Prof-school（职业学校）, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters（硕士）, 1st-4th, 10th, Doctorate（博士）, 5th-6th, Preschool（学前）}
- `education-num`: 一个整数表示在学校学习了多少年 
- `marital-status`: 一个类别变量，允许的值有 {Married-civ-spouse（已婚）, Divorced（离婚）, Never-married（未婚）, Separated（离异）, Widowed（丧偶）, Married-spouse-absent（已婚分居）, Married-AF-spouse（再婚）} 
- `occupation`: 一个类别变量表示一般的职业领域，允许的值有 {Tech-support（技术支持）, Craft-repair（维修手工艺）, Other-service（服务业）, Sales（销售）, Exec-managerial（管理）, Prof-specialty（专业技术）, Handlers-cleaners（清洁）, Machine-op-inspct（机器操作）, Adm-clerical（行政文员）, Farming-fishing（养殖渔业）, Transport-moving （运输行业）, Priv-house-serv(私人房屋管理), Protective-serv（保卫工作), Armed-Forces(武装部队)}
- `relationship`: 一个类别变量表示家庭情况，允许的值有 {Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried}
- `race`: 一个类别变量表示人种，允许的值有 {White(白人), Asian-Pac-Islander（亚洲太平洋岛民）, Amer-Indian-Eskimo（阿米尔-印度-爱斯基摩人）, Other（其他）, Black黑人} 
- `sex`: 一个类别变量表示性别，允许的值有 {Female, Male} 
- `capital-gain`: 连续值。 
- `capital-loss`: 连续值。 
- `hours-per-week`: 连续值。 
- `native-country/district`: 一个类别变量表示原始的国家，允许的值有 {United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands}

**目标变量**

- `income`: 一个类别变量，表示收入属于那个类别，允许的值有 {<=50K, >50K}