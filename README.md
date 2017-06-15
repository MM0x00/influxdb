# influxdb 在线实验环境

## 软件简介

InfluxDB是从头开始构建的时间序列数据库，用于处理高写入和查询负载。InfluxDB旨在用作涉及大量时间戳数据的任何用例的后备存储，包括DevOps监控，应用指标，IoT传感器数据和实时分析

所属类别是数据库

特点：

- schemaless(无结构)，可以是任意数量的列
- Scalable
- min, max, sum, count, mean, median 一系列函数，方便统计
- Native HTTP API, 内置http支持，使用http读写
- Powerful Query Language 类似sql
- Built-in Explorer 自带管理工具
## 软件官网

https://www.influxdata.com/

## Dockerfile 使用方法

### 使用
运行容器

InfluxDB映像公开了一个共享卷/var/lib/influxdb，因此您可以挂载主机目录以访问持久化的容器数据。容器的典型调用可能是：
```
$ docker run -p 8086:8086 \
      -v $PWD:/var/lib/influxdb \
      influxdb
```
修改$PWD到要存储与InfluxDB容器关联的数据的目录。

您也可以通过使用命名卷来使Docker控制卷安装点。
```
$ docker run -p 8086:8086 \
      -v influxdb:/var/lib/influxdb \
      influxdb
```
## 资源链接

- https://www.influxdata.com/
- https://hub.docker.com/_/influxdb/
- http://www.ttlsa.com/monitor-safe/monitor/distributed-time-series-database-influxdb/
- http://blog.csdn.net/post_yuan/article/details/52419458
