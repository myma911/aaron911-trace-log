一个简单易用的java分布式日志组件
### 一.系统介绍

 1. 无入侵的分布式日志系统，基于logback搜集日志，设置链路ID，方便查询关联日志
 
 2. 基于elasticsearch作为查询引擎
 

### 二.架构

 
* log-core 核心组件包含日志搜集端，负责搜集日志并推送到kafka，redis等队列

* log-server 负责把队列中的日志日志异步写入到elasticsearch 