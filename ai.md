# AI



## 1.parameter server

Ring All Reduce (环同步)



## 2.通信与原语

### 机器内部通信

*共享内存*

PCIe (cpu与gpu)

NVlink(直连接gpu-gpu，gpu-cpu),非常的高速

### 机器与机器间通信

tcp/ip

rdma(rmote direct memory access)

CPU offload :无需CPU干预，远程主机cpu缓存（cache）不会被访问的内存内容所填充

kernel bypass:专有verbs interface ,应用程序可以直接在用户态执行数据传输

zero copy:每个应用程序都能直接访问集群中的设备的虚拟内存



带宽，延迟





### 通信协调

#### 点对点

MPI 



#### 集合

NCCL/HCCL



### 通信原语

#### 一对多（Scatter）

broadcast（网络参数初始化）

#### 多对一 （reduce）

Sum,min,max,prod,lor,gather (汇集)

#### 多对多（all reduce）

all gather ,多环通信会用到，reduce scatter

all to all



## 3.并行处理硬件架构

simd

misd

mimd

simd



SIMT编程的GPU架构

## 4.分布式训练系统

分布式用户接口

执行单节点训练

通信协调



tensorflow



pytorch





#### 自行并行原理

1.张量排布模型

2.分布式算子

3.张量排布变换

4.切分策略搜索算法

5.分布式自动微分



## 5.大模型 foundation models 

1.预训练网络模型重要性

Pre-Train 



2.



## 6.挑战

算法,数据,框架，资源调度，全栈，全流程的综合能力

### 1.内存墙

static memory (parameter)

dynamic memory （一般是static的3倍）

### 2.通信墙



### 3.性能墙



### 4.调优墙

### 



 