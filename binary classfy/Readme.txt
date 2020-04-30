这是一个二分类的练习赛，某个金融机构想根据提供的信息构建模型，来对代理商培训效果进行预测。评分标准：AUC-ROC。
字段信息如下：
		变量	描述
		 ID	 唯一身份
		 program_id	 节目编号
		 程序类型	 节目类型
		 program_duration	 计划持续时间（天）
		 test_id	 测试编号
		 test_type	 测试类型（离线/在线）
		 难度级别	 考试难度
		 trainee_id	 学员ID
		 性别	 实习生性别
		 教育	 受训者的教育程度
		 city_tier	 实习生居住城市的等级
		 年龄	 受训年龄
		 total_programs_enrolled	 学员注册的课程总数
		 is_残疾人	 受训者是否患有残疾？
		 trainee_engagement_rating	讲师/教学助理为课程提供了学员参与度评分
		 is_pass	 0-测试失败，1-测试通过
