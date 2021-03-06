### 产品简介

**Pnadora 智能异常检测与预测** 是基于机器学习、深度学习进行数据处理、建模、异常检测、预测的分析产品。用户通过使用机器学习得到的分析结果来指导自身的业务。机器学习主要应用的场景有：

* IT 运营场景：通过流量异常检测进行系统安全分析，如 DNS/HTTP 数据泄露检测、可疑登陆检测。
* 医学场景：患者的异常身体指标检测，及时跟进患者身体状况。
* 商业营销场景：电商网站识别消费者提交支付次数，来衡量网站的转化效果。
* 金融类场景：金融机构通过异常指标进行风险控制、股票走势预测
* 社交类场景：用户画像、用户倾向分析、受欢迎话题分析
* 其他：降雨预测、比赛结果预测

#### 产品优势

 Pnadora 智能异常检测与预测的主要优势如下：
 
 **友好的操作方式**
 
 通过对底层的算法进行封装，提供可视化的操作环境，用户通过页面可视化配置任务指标即可创建异常检测任务，无需编程语言，降低了用户的学习成本，让数据挖掘变成一件简单的事情。
 
 ![](https://pandora-kibana.qiniu.com/ml_interface.png)
 
 **优质的机器学习算法**
 
 提供诸如聚类、回归、神经网络等机器学习及深度学习算法，进行精准的异常检测与预测，准确度比传统机器学习算法高出很多。
 
 **与 Pandora 智能日志管理平台完美融合**
 
 机器学习直接基于 Pandora 智能日志管理平台存储的数据进行建模分析，无需复杂的导入导出。
 
### 用户指南

点击进入[机器学习](https://portal.qiniu.com/pandora/logdb)入口。通过如下图操作逻辑实现对历史静态异常值检测以及异常值预测。

![](https://pandora-kibana.qiniu.com/ml_structure.png)

#### 异常检测

##### 创建异常检测任务并配置

配置需要进行异常分析的指标：

1. 点击`创建任务`。

![](https://pandora-kibana.qiniu.com/create_task2.png)

2. 选择需要分析的仓库、指标、字段(数值类型)、时间字段以及时间范围来确定需要分析的指标。

![](https://pandora-kibana.qiniu.com/create_task3.png)

|配置项|解释|
|:--|:--|
|仓库|分析的日志所在的仓库|
|指标|需要分析的指标，包括计数, 去重计数, 求和, 平均值, 最大值, 最小值|
|字段|目标分析字段|
|时间字段|若日志里有多个时间字段，选择感兴趣的时间字段来分析该字段的时序范围内的异常|
|时间范围|分析的时序范围|
|时间聚合粒度|时间聚合粒度|

3. 填写任务名称与描述生成任务的异常指标视图，同时将任务保存到任务概览。

![](https://pandora-kibana.qiniu.com/des_task.png)

!>注意：配置异常指标之后需要点击预览指标，系统将根据预览结果决定是否允许创建异常检测任务。预览无数据或者数据量不够均达不到创建异常检测条件。

##### 查看异常检测结果

1. 配置好任务以后任务立即开始执行，系统开始分析指定时间范围内的历史数据并呈现分析视图。
   视图上显示指标的预期值范围以及实际值。偏离预期曲线的点即为异常值，异常数据区间高亮标示，一眼      就能看到异常区间。异常点偏离期望曲线越远，表示异常程度越严重。

2. 可以拖动时间轴查看不同时间的任务详情。

3. 可在视图中交互性查看每个点具体的异常信息，包括该指标的异常时间、异常程度、期望值、实际值、异常描述等信息。
   异常程度根据算法对应不同分值，异常程度有四种：critical、warning、major、minor，分别对应的异常分值为75～100，50～75，25～50，0～25。
   
   ![](https://pandora-kibana.qiniu.com/detect_detail.png)

4. 异常列表显示此任务范围内的全部异常情况，可根据异常程度对异常结果进行筛选。

![](https://pandora-kibana.qiniu.com/abnormal_list.png)

#### 异常预测

1. 系统对历史时序数据检测完成之后，在异常检测页面右上角点击`预测`，创建预测任务。

![](https://pandora-kibana.qiniu.com/create_forecast.png)

2. 根据历史时序数据对所选预测时间范围的数据进行预测。

![](https://pandora-kibana.qiniu.com/forecast.png)

3. 预测结果包括预测指标区间以及预测指标值。

![](https://pandora-kibana.qiniu.com/forecast1.png)






