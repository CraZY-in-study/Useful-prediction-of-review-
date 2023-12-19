# Useful-prediction-of-review-from-Yelp-dataset
本文数据来来源是Yelp 2008-2018的评论数据，针对useful字段，根据三个数据集提取变量对useful进行预测，内容包括：

数据预处理：

-对文本有用性的客观指标构建：文本NLP技术、LDA主题提取

-对评论者的网络中心度指标的构建：使用年限、评价有效性等

-对商家的知名度指标构建：针对商户名称的评论有效指标、收到评论数量等

构建模型：

-线性模型

-LightGBM模型

-XGboost模型

-LightGBM和XGBoost融合模型

数据分析：

-模型评价

-不同数据集对useful预测准确性的贡献

-对商家提出建议

