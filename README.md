---
layout:     post
title:      "Spark_大数据技术实现航空订票数据处理"
subtitle:   " \"大数据技术实现航空订票数据处理\""
date:       2019-06-22 13:00:00
author:     "jack"
header-img: "img/post-bg-sea2.jpg"
catalog: true
tags:
    - hadoop
    - 大数据
    - spark


---

### **GDS**机票数据处理系统

#### 1.项目整体设计

- 利用Kafka拉取日志数据，并创建消费者将数据消费至分布式存储平台；
- 利用分布式处理技术对结构化日志数据进行聚合处理，并将处理结果存入MySQL；
- 对数据处理结果进行WEB展示；
- 对数据进行统计指标计算，形成报表存储至HDFS.

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172132.png)

#### 2.实现环境搭建

ECS 轻量型服务器 Centos

- 39.97.44.21
- 39.107.97.163
- 39.107.69.248

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172239.png)

所需环境

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172254.png)

#### 3. 实现过程

##### 3.1 数据分析和前期设计

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172408.png)

##### 3.2 kafka 生产者分发到集群

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172509.png)

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172527.png)

##### 3.3 hbase创建和设计

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172755.png)



#### 3.4 storm-kafka

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172852.png)

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172842.png)

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172831.png)

#### 4. 结果总结

编写前端进行展示

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626173001.png)

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172947.png)

![](https://jackyanghc-picture.oss-cn-beijing.aliyuncs.com/20190626172928.png)
