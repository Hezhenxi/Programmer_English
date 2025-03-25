# Programmer_English

原则是方便发音，便于快读
浊音 i dont know   i on know
     router 路由  ˈruːtər  t 读 d  ruːdər 

sorry?
sorry the what building
sorry can you go over/through that again

put the vocabulary in the sentences to memories. 


---------------------------------------------
Design data-intensive application
---------------------------------------------
publish:2017   Martin Kleppmann
# Design data-intensive application

## preface n.序言 v.为...写序言/ˈprefəs/  The preface of the book 书的序言
NoSQL,大数据, Web-Scale,分片, 最终一致性, ACID, CAP, 云服务
MapReduce,实时

summary	n.摘要，总结 adj.概要的 /ˈsʌməri/  a brief summary 一个简短的总结
scale	n.规模,刻度，大小 v.调节，绘制/skeɪl/ the scale of web 网络规模
intensive	adj.密集的，十分细致的 n.加强器/ɪnˈtensɪv/  
architecture	n.结构，建筑的，架构/ˈɑːrkɪtektʃər/
safari	n.游猎，长途旅行/səˈfɑːri/ A safari is a trip to hunt 游猎指捕猎的旅途

# 数据系统的基石
## chapter 1 可靠性reliability，可拓展性scalability，可维护性maintainability	
PS：之前一直把可扩展性理解成设计模式中的代码开放封闭原则了，代码扩展性。其实是应对负载变化后，可以通过增加副本应对负载压力。比如数据库集群缩放

### picture of summary 
The big ideas behind reliable, scalable & maintainable system
reliable	adj.可靠性，可信赖 n.可靠的人/rɪˈlaɪəbl/ System is more reliable than humans 系统比人可靠
scalable	adj.可拓展性，可伸缩/ˈskeɪləbl/	   highly scalable 高扩展性
maintainable adj.可维护性，保持/meɪnˈteɪnəbl/

reliablity n.可靠性	英/rɪˌlaɪə'bɪlɪti/ 美/rɪˌlaɪə'bɪləti/  good reliablity 好的可靠性
tolerating	v.容忍，容错性，忍受，包容/ˈtɑːləreɪtɪŋ/	if you can tolerate something painful. 如果你能忍受一些伤痛
hardware & sofeware
faults	n.故障，过错 v.发现错误/fɔːlts/   it's my faults 这是我的过错
human error

ps:
	resilience n.恢复力，能复原的，弹力/rɪˈzɪliəns/   The system has hight resilience 系统有高弹性/恢复力 	
	flexible adj.灵活的,柔韧的，有弹性的/ˈfleksəbl/	  Working form home offers the ultimate in flexible life styles. 居家办公提供了极其灵活的生活方式
	feasibility	n.可行性/ˌfizəˈbɪləti/ I doubt the feasibility of the plan.

scalability n.可扩展性，可伸缩性，可量测性/skeɪləˈbɪlɪti/ 
measure	v.测量，估量 n.措施,方法，尺度/ˈmeʒər/ If you measure the quality,value.
load	n.负载，加载 v.装载，承载，写入/loʊd/  Measuring load 测定加载量
performance	 n.演出，性能，表现，执行 adj.性能卓越的，高性能的/pərˈfɔːrməns/ 
perform v.执行，表演/pərˈfɔːrm/
latency	n.延迟,潜伏，潜在因素/'leɪtənsɪ/
percentile	n.百分位数/pərˈsentaɪl/
throughput	n.吞吐量,接待人数/ˈθruːpʊt/		
throughout prep.始终，遍及 adv.始终/θruːˈaʊt/

maintainability n.可维护性 /meɪnˌteɪnəˈbɪlɪti/
operability	n.可操作性/ˌɑpərəˈbɪlɪti/
simplicity	n.简易性/sɪmˈplɪsəti/
evolvability	n.可进化性 evolving 进化/iˈvɑːlvɪŋ/
evolution n.演变，进化/ˌiːvəˈluːʃn/

data-intensive	数据密集型
compute-intensive	计算密集
database	数据库
cache	缓存/kæʃ/
search indexes	搜索索引
stream processing	流处理
batch processing	批处理
data system	数据系统
### 关于数据系统的思考
(API	application programming interface 应用程序编程接口
client requests 	application code	first check if data is cached	read requests	in-memory cache		invalidate or update cache	application code
cache misses and writes		primary database	capture changes to data
asynchronous tasks	message queue	application code 	send email	outside world
search requests		full-text indexes	apply updates to search index)
reliability
scalability
maintainability

### 可靠性
fault 故障
fault-tolerant	容错
resilient	韧性/rɪˈzɪliənt/
failure	失效、失败

#### 硬件故障
hardware faults 	硬件故障
MTTF,mean time to failure	平均无故障时间
AWS,amazon web services	亚马逊网络服务
prevent error	阻止预防错误
flexibility	灵活性
elasticity	弹性

#### 软件错误
systematic error	系统性错误
discrepancy	差异/dɪsˈkrepənsi/

#### 人为错误

decouple	分离，解耦/diːˈkʌpl/
sandbox		沙箱
corner case		边缘场景
telemetry	远距离测量术/təˈlemətri/

#### 可靠性有多重要

### 可拓展性
degradation		降级，恶化/ˌdeɡrəˈdeɪʃn/
Scalability 可扩展性

#### 描述负载
load parameters		负载参数
fan-out		扇出/fæn/

#### 描述性能
throughput		吞吐量/ˈθruːpʊt/
response time	响应时间
distribution	分布
arithmetic mean	算术平均值/əˈrɪθmətɪk/
median		中位数/ˈmiːdiən/
tail latencies	尾部延迟
SLO,service level objective		服务级别目标
SLA,service level agreements	服务级别协议
queueing delay		排队延迟
head-of-line blocking	头部阻塞

#### 应对负载的方法
scaling up		纵向扩展
scaling out		横向扩展
vertical scaling	垂直扩展
horizontal scaling	水平扩展
shared-nothing	无共享
elastic		弹性
highly unpredictable	极难预测
stateless services		无状态服务/ˈsteɪtləs/	less 极少/les/
magic scaling sauce		通用可拓展架构
assumption	假设n/əˈsʌmpʃn/		assume	假设v/əˈsuːm/

### 可维护性
legacy 		遗留，遗产/ˈleɡəsi/
operability		可操作性/ˌɑpərəˈbɪlɪti/		
opera 歌剧/ˈɑːprə/	
operation 操作/ˌɑːpəˈreɪʃn/
simplicity	简易性/sɪmˈplɪsəti/
complexity	复杂度/kəmˈpleksəti/
extensibility	可拓展性
modifiability	可修改性
plasticity		可塑性	
plastics	塑料/ˈplæstɪks/

#### 可操作性：人生苦短，关爱运维
visibility	可见性/ˌvɪzəˈbɪləti/

#### 简单性：管理复杂度
accidental	意外的/ˌæksɪˈdentl/
abstraction	抽象/æbˈstrækʃn/
directly	直接的/dəˈrektli/

#### 可演化性：拥抱变化
agile	敏捷的/ˈædʒl/
TDD,test-driven development
refactoring	重构/ˌriˈfæktərɪŋ/
evolvability	可演化性

### 本章小结
a big ball of mud 烂泥堆
functional requirements	功能需求
nonfunctional	非功能性
processing capacity	/kəˈpæsəti/处理容量	
capability	能力，才能/ˌkeɪpəˈbɪləti/

## chapter 2 data mode & query language数据模型和查询语言
### picture of summary 
Trading Route	贸易路线 route路线/ruːt/

the realational empire	关系型帝国
query planners 
the declarative river
sql metropolis 大都市/məˈtrɑːpəlɪs/
postgreSQL,oracle,mysql,sqlServer,DB2,xpath,css, 

key-value district  键值地区
NoSql danger zone
redis,berkeley DB,voldmort,riak,aerospike

document data district	文档数据地区
ruins XML database 摧毁，破坏/ˈruːɪnz/
ims,rethinkDB,mongoDB,couchDB,hyperdex mapReduce forest 森林/ˈfɔːrɪst/

column-family district	列家族地区  column栏目，列/ˈkɑːləm/
HBase,cassandra

graph data peaks 图数据高峰
cypher,neo4j,datalog,datomic,orientDB,titan,sparql,codasyl

### 关系模型与文档模型

#### NoSQL的诞生
nosql,not only sql
polyglot persistence 混合持久化	通晓多种语言/ˈpɑːliɡlɑːt/ 持久化，坚持不懈/pərˈsɪstəns/

#### 对象关系不匹配
impedance mismatch	阻抗不匹配	阻抗/ɪmˈpiːdns/
ORM,object-relational mapping	对象关系映射
locality	局部性，地点/loʊˈkæləti/

#### 多对-和多对多的关系
duplication	副本/ˌduːplɪˈkeɪʃn/
normalization	规范化/ˌnɔrməlɪˈzeɪʃən/

#### 文档数据库是否在重蹈覆辙?
hierarchical model	层次模型	等级的/ˌhaɪəˈrɑːrkɪkl/  /ˈmɑːdl/
relational model	关系模型
network model		网络模型

##### 网络模型
access path 访问路径/ˈækses/	/pæθ/

##### 关系模型
##### 与文档数据库相比
#### 关系型数据库与文档数据库在今日的对比
##### 哪个数据模型更方便写代码?

##### 文档模型中的架构灵活性
schemaless	无模式
schema-on-read	读时模式
schema-on-writes	写时模式

##### 查询的数据局部性
##### 文档和关系数据库的融合
### 数据查询语言
##### Web上的声明式查询
##### MapReduce查询

### 图数据模型
multi-table index cluster tables	多表索引集群表
column-family	列簇
vertices	顶点/ˈvɜːtɪsiːz/  pyramid vertices	金字塔尖
chrome	n.铬合金/kroʊm/
edges	边缘/ˈedʒɪz/
arcs	弧，电弧/ɑːrks/

#### 属性图
vertex	顶点/ˈvɜːrteks/
outgoing edges	出边
ingoing edges	入边
tail vertex		尾顶
head vertex		头顶

#### Cypher查询语言
#### SQL中的图查询
#### 三元组存储和SPARQL
##### 语义网络
##### RDF数据模型
#### SPARQL查询语言
#### 基础:Datalog
### 本章小结

## chapter 3 storage /ˈstɔːrɪdʒ/	& retrieve 存储与检索

### picture of summary
Ocean of distributed data
To replication
Log-Structured storage
BigTable tablelands
Riak,Cassandra,HBase
Hightlands of search
Bay of embedded storage engines
Lucene, Rocks DB,LevelDB
Repulic of transaction processing
Forest of secondary indexes
Land of the B-Trees
HyperDex,BerkerleyDB,MySQL, PostgreSQL,Oracle, SqlServer,MongoDB
Log Shipping
VALLEY OF IN-MEMEORY STORAGE
HADOOP REGION 
Tower of Spark, Hive , Drill, LAKE OF HDFS,Impala, Presto
SEA OF STORAGE & RETRIEVAL
REALM OF DATA WAREHOUSES
KINGDOM OF ANALYTICS
MOUNTAINS OF COLUMN STORAGE
Vertica, Parquet, ParAccel, RedShift
ISLANDS OF SCIENTIFIC INQUIRY
FENOME DATA
ARRAY DDATABASES

### 驱动数据库的数据结构
log-structured	日志结构
page-oriented	面相页
append-only 仅追加
additional	附加，额外

#### 哈希索引
dictionary	字典
seek 寻找
compaction	压缩/ˈkɑːmpækt , kəmˈpækt/
solid state disk 固态硬盘SSD/ˈsɑːlɪd steɪt dɪsk/

#### SSTables和LSM树
sorted string table 排序字符串表SSTable

##### 构建和维护SSTables
memtable 内存表

##### 用SSTables制作LSM树
term 术语，关键词

##### 性能优化
#### B树

##### 让B树更可靠
WAL write-ahead-log 预写式日志
redo log 重做日志
latches	锁存器/ˈlætʃɪz/

##### B树优化
#### 比较B树和LSM树

##### LSM树的优点
write amplification 写放大

##### LSM树的缺点
#### 其他索引结构
primary key 主键

##### 将值存储在索引中
heap file 堆文件
clustered index 聚集索引
index with included columns 包含列索引/ covering index 覆盖索引

##### 多列索引
nonclustered index	非聚集索引
concatenated index 连接索引
multi-dimensional index 多维索引

##### 全文搜索和模糊索引
##### 在内存中存储一切
anti-caching	反缓存

### 事务处理还是分析?
OLTP online transaction processing 在线事务处理
OLAP online analytice processing  在线分析处理
data warehouse 数据仓库

#### 数据仓库
ETL extract-transform-load 获取转换加载
SKU Stock Keeping Unit 库存单位

##### OLTP数据库和数据仓库之间的分歧
#### 星型和雪花型:分析的模式
### 列存储
#### 列压缩
##### 内存带宽和向量处理
#### 列存储中的排序顺序
##### 几个不同的排序顺序
#### 写入列存储
#### 聚合:数据立方体和物化视图
### 本章小结


## chapter 4 encode & evolution 编码与演化

### picture of summary
GULF OF BINARY ENCODINGS
To Storage & Retrieval
BUKL STORAGE TUNDRA
Log files, CSV,	SQL dumps, Parquet, Avro, JDBC 
RANDOM ACCESS STORAGE
Protocol Buffers, Thrift 
DOCUMENT DATABASES
JSON, swagger
PEOPLE'S REPUBLIC OF RPC 
EJB, CORBA,LONG ROAD OF SCHEMA, EVOLUTION , Swagger,WSDL, XML,
Castle in the air(IIIusion of transparent RPC)
MESSSAGE PASSING
Akka, Erlang
BAY OF REST
BAY OF SOAP
MICROSERVICES REEF
INTEROPERABILITY ROCKS
COAST OF TEXTUAL ENCONDINGS

feature 功能
schema-on-read 读时模式
schemaless	无模式
format 格式
schema 模式
server-side 服务端
rolling upgrade 滚动升级
staged rollout 阶段发布
client-side 客户端
backward compatibility 向后兼容
forward compatibility 向前兼容
REST 具象状态传输
RPC	远程过程调用

### 编码的数据格式
encode 编码
serialization 序列化
marshalling	编组
decode 解码
Parsing 解析
deserialization 反序列化
unmarshalling 反编组

#### 语言特定的格式
#### JSON、XML和二进制变体
##### 二进制编码
#### Thrift与Protocol Buffers
##### 字段标签和演变模式
##### 数据类型和演变模式
#### Avro
##### 作者模式和读者模式
##### 模式演变规则
###### 但作者模式到底是什么
##### 动态生成的模式
##### 代码生成和动态类型的语言
#### 模式的优点
### 数据流的类型
#### 数据库中的数据流
##### 在不同的时间写入不同的值
##### 归档存储
#### 服务中的数据流：REST和RPC
service-oriented architecture  SOA面向服务的体系结构

##### Web服务
middleware 中间件
RMI 远程方法调用
DCOM 分布式组件对象模型
CORBA	公共对象请求代理体系结构
idempotence 幂等，去重

##### 远程过程调用（RPC）的问题
##### RPC的当前方向
##### 数据编码与RPC的演化
#### 消息传递中的数据流
##### 消息掮客
##### 分布式的Actor框架
###	本章小结

# 分布式数据
## 扩展至更高的载荷
load 载荷
vertical scaling 垂直扩展
scale up 向上扩展
share-memory architecture 共享内存架构
shared-disk architecture 共享磁盘架构

### 无共享架构
shared-nothing architecture 无共享架构
horizontal scale 水平扩展
scale out 向外扩展
node 节点

## 复制VS分区
replication n.复制,重复，拷贝 /ˌreplɪ'keɪʃ(ə)n/
partitioning 分区
partitions 分区
shard 分片
transaction 事务

### picture of summary
BAY OF CAUSALITY
QUORUM HARBOR
LEADERLESS REPLICATION
MULTI-LEADER REPLICATION
SINGLE-LEADER REPLICATION
LOGICAL COASTF
FOREST OF CONSISTENCY MODELS

## 5.复制
change 变更
single leader 单领导者
multi leader 多领导者
leaderless 无领导者
eventual consistency 最终一致性
read-your-writes 读己之写
monotonic read 单调读

### 领导者与追随者
replica n.副本 /ˈreplɪkə/
leader-base replication 基于领导的复制
active 主动
passive 被动
master 主
slave 从
leader 领导
primary 首要
followers 追随者
read replicas 只读副本
sencondaries 次要
hot-standby 热备
change stream 变更流

#### 同步复制与异步复制
synchronously adj.同步 /ˈsɪŋkrənəs/
asynchronously 异步
semi n.半决赛，半独立住宅/ˈsemi/
semi-synchronous 半同步
durable adj.耐用的，持久的 n.耐用品，耐久品 /ˈdʊrəbl/
consensus n.共识，一致的意见/kənˈsensəs/

#### 设置新从库
log sequence number 日志序列号LSN
coordinate v.协调 n.坐标/koʊˈɔːrdɪneɪts/
binlog coordinates 二进制日志坐标
cauht up 赶上

#### 处理节点宕机
##### 从库失效:追赶恢复
##### 主库失效:故障切换
failover 故障切换
timeout  超时
controller node 控制器节点
split brain 脑裂

#### 复制日志的实现
##### 基于语句的复制
statement n.陈述，语句，报告，声明/ˈsteɪtmənt/
nondeterministic 非确定函数
auto increment 自增列

##### 传输预写式日志(WAL)
write ahead log  预习式日志WAL

##### 逻辑日志复制(基于行)
change data capture 捕获数据变更

##### 基于触发器的复制
### 复制延迟问题
eventually consistency 最终一致性
replication lag 复制延迟

#### 读已之写
read-after-write 写后读
read-after-write 读写一致性
read-your-writes consistency 读己之写一致性

#### 单调读
moving backward in time 时光倒流
monotonic reads 单调读
strong consistency 强一致性
eventually consistency 最终一致性

#### 一致前缀读
consistent prefix reads 一致前缀读
partitioned /sharded 分区/分片

##### 复制延迟的解决方案
transaction n.交易，处理，业务，事务/trænˈzækʃn/

### 多主复制
#### 多主复制的应用场景
##### 运维多个数据中心
##### 需要离线操作的客户端
##### 协同编辑
#### 处理写入冲突
##### 同步与异步冲突检测
##### 避免冲突
##### 收敛至一致的状态
convergent adj.收敛 /kənˈvɜːrdʒənt/
last write wins 最后写入胜利 LWW

##### 自定义冲突解决逻辑
##### 什么是冲突?
#### 多主复制拓扑
circular topology 环形拓扑
version vectors 版本向量

### 无主复制
leaderless 无领导的

#### 当节点故障时写入数据库
##### 读修复和反熵
read repair 读修复
anti-entropy process 反熵过程

##### 读写的法定人数
quorum n.(会议的)法定人数/ˈkwɔːrəm/

#### 仲裁一致性的局限性
timing 时序

##### 监控陈旧度
#### 松散法定人数与带提示的接力
sloppy adj.马虎的，草率的/ˈslɑːpi/
sloppy quorum 松散的法定人数
hinted handoff 带提示的接力

##### 运维多个数据中心
#### 检测并发写入
##### 最后写入胜利(丢弃并发写入)
concurrent adj.并发 /kənˈkɜːrənt/

##### “此前发生”的关系和并发
causally adv.因果/ˈkɔːzəlɪ/
causally dependent 因果依赖

##### 捕获"此前发生"关系
##### 合并同时写入的值
tombstone n.墓碑/ˈtuːmstoʊn/

##### 版本向量
vector n.矢量，向量/ˈvektər/
version vector 版本向量
dotted version vector 分散版本矢量
causal context 因果上下文

### 本章小结

## 6.分区
### picture of summary
PARTIONING ATOLL
TERM PARTICIONED
DOCUMENT PARTITIONED
SECONDARY INDEXES
REBLANCING
REQUEST ROUTING
KEY RANGE PARTITIONING
HASH PARTIIONNING

### 分区与复制
partitions 分区
sharding 分片

### 键值数据的分区
skew v.倾斜  /skjuː/
hot spot  热点

#### 根据键的范围分区
#### 根据键的散列分区
consistent hashing 一致性哈希

#### 负载倾斜与消除热点
### 分片与次级索引
#### 按文档的二级索引
document-based 基于文档的分区
term-based 基于关键词

#### 根据关键词(Term)的二级索引
field 字段
column 列
local index 本地索引
global index 全局索引
scatter 分散
gather 聚集
term-partitioned 关键词分区 

### 分区再平衡
reblancing 再平衡

#### 平衡策略
##### 反面教材:hash mod N
##### 固定数量的分区
##### 动态分区
pre-splitting 预分隔

##### 按节点比例分区
#### 运维：手动还是自动平衡
### 请求路由
service discovery  服务发现
round-robin load balancer 循环策略的负载均衡
config server 配置服务器
gossip protocol 流言协议
massively parallel processing 大规模并行处理

#### 执行并行查询
### 本章小结
### 参考文献

# 衍生数据
## 12.数据系统的未来
### 数据集成
#### 组合使用衍生数据的工具
##### 理解数据流
##### 衍生数据与分布式事务
##### 全局有序的限制
##### 排序事件以捕捉因果关系
#### 批处理与流处理
microbatches  微批次

##### 维护衍生状态
##### 应用演化后重新处理数据
gradual evolution 逐渐演化
##### Lambda架构
##### 统一批处理和流处理
### 分拆数据库
#### 组合使用数据存储技术
##### 创建索引
##### 一切的元数据库
##### 开展分拆工作
exactly-once 恰好一次
loose coupling 松散耦合

##### 分拆系统vs集成系统
##### 少了什么？
differential dataflow 差分数据库

#### 围绕数据流设计应用
funtional reactive programming FRP函数响应式编程
unbunding	分拆

##### 应用代码作为衍生函数
##### 应用代码和状态的分离
##### 数据流：应用代码与状态变化的交互
tuple space 元组空间

##### 流处理器和服务
#### 观察衍生数据状态
write path	写路径
read path	读路径

##### 物化视图和缓存
cache 缓存
materialized view 物化视图和缓存

##### 有状态，可离线的客户端
offline-first 离线优先
end-to-end 端到端
consistency 一致性

### 将状态变更推送给客户端
##### 端到端的事件流
##### 读也是事件
##### 多分区数据处理
### 将事情做正确
#### 为数据库使用端到端的参数
##### 正好执行一次操作
idempotent 幂等

##### 抑制重复
##### 操作标识符

##### 在数据系统中应用端到端思考
#### 强制约束
correctness 正确性

##### 唯一性约束需要达成共识
##### 基于日志消息传递中的唯一性
##### 多分区请求处理
#### 及时性与完整性
timeliness 及时性
linearizability  线性一致性
integrity  完整性

##### 数据流系统的正确性
##### 宽松地解释约束
compensating transaction 补偿性事务

##### 无协调数据系统
coordination-avoiding 无协调

#### 信任但验证
system model 系统模型
rowhammer 破坏系统安全机制

##### 维护完整性，尽管软件有Bug
##### 不要盲目信任承诺
auditing 审计

##### 验证的文化
self-validating 自我验证
self-auditing 自我审查

##### 为可审计性而设计
provenance  出处，起源

##### 端到端原则重现
##### 用于可审计数据系统的工具
proof of work 工作证明
merkle tree 默克尔树
certificate transparency

### 做正确的事情
#### 预测性分析
##### 偏见与歧视
##### 责任与问责
##### 反馈循环
systems thinkin

#### 隐私和追踪
surveillance 监控/sɜːrˈveɪləns/


##### 监视
##### 同意与选择的自由
##### 隐私与数据使用
privacy 隐私

##### 数据资产与权力
##### 记着工业革命
##### 立法和自律
### 本章小结
data integration 数据集成

### 参考文献
# 后记






=============================================
scenario 1 Software Enginner
=============================================



---------------------------------------------
HSBC_JD
---------------------------------------------
regular 常规的，定期，有规律的/ˈreɡjələr/
regulation	法规，监管/ˌreɡjuˈleɪʃn/
adjust	调整/əˈdʒʌst/
constant	常量，恒定的，不断的/ˈkɑːnstənt/
uplift	隆起，提高/ˈʌplɪft/
establish 建立/ɪˈstæblɪʃ/
equivalent	相同的，等量的/ɪˈkwɪvələnt/
mission	 使命，任务/ˈmɪʃn/		missionary 使者
revenues  收益，财政收入/ˈrɛvəˌnuz/

------------HSBC recruitment-------------------------------

recruitment	招聘/rɪˈkruːtmənt
internal 内部的，内心/ɪnˈtɜːrnl/
external 外部的，外界的，外来/ɪkˈstɜːrnl
retrieve 取回，恢复，检索，寻回/rɪˈtriːvd/

---------------------------------------------
Tell me about your self tips
---------------------------------------------
essentially 本质上，基本上/ɪˈsenʃəli/

---------------------------------------------
Senior Software Enginner interview
---------------------------------------------
achieve 实现əˈtʃiːv
activities 活跃ækˈtɪvətiz
actual 实际ˈæktʃuəl
adapt 适应əˈdæpt
advisor 顾问/ædˈvaɪzər
affect 影响/əˈfekt
archive  归档 ˈɑːrkaɪv
associations 协会əˌsoʊsiˈeɪʃənz
atmosphere 气氛ˈætməsfɪr       how would you describe your working atmosphere and some people with whom your working with
auto 汽车/ˈɔːtoʊ/
automat  自动售货机/ˈɔːtəmæt/
automated 自动化ˈɔːtəmeɪtɪd
automatically 自动ˌɔtəˈmætɪkli/
areas 地区，地域ˈɛriəz

basis 基础 ˈbeɪsɪs/
budget	预算ˈbʌdʒɪt
career 职业kəˈrɪr
certain 确定/某些sɜːrtn   uncertainties不确定ənˈsɜrtəntiz
chunks 块tʃʌŋks/

complex 复杂的 kəmˈpleks
compliance 遵从kəmˈplaɪəns  config compliance 
contact 接触，联络ˈkɑːntækt
continuous 连续的 kənˈtɪnjuəs
countless 不可计算ˈkaʊntləs

defined 定义/明确dɪˈfaɪnd
deliver 交付dɪˈlɪvər	deliverable 可交付的dɪˈlɪvərəbl
depth	深度depθ
device 设备 dɪˈvaɪs
digest	消化 ’daɪdʒes
discover 发现 dɪˈskʌvər

elaborate 详尽ɪˈlæbəreɪt
electrical 用电的 ɪˈlektrɪkl
elegant 优雅的，简洁的ˈelɪɡənt
entry 进入ˈentri

evaluate 评估/ɪˈvæljueɪt/
eventual 最终/ɪˈventʃuəl/
evolving 进化/iˈvɑːlvɪŋ/
executives 主管ɪgˈzɛkjətɪvz	
expectations 期望ˌɛkspɛkˈteɪʃənz
expert 专家ˈɛkspərt
exploring	探索ɪkˈsplɔːrɪŋ

field 领域fiːld
foreman 领班fɔːrmən
frustrated 沮丧，无效ˈfrʌstreɪtɪd

gain 获取ɡeɪn
guide 指导ɡaɪd  guidelines 准则ˈgaɪˌdlaɪnz

implement 实施/执行ˈɪmplɪment 
industry 行业/ˈɪndəstri/
innovative 创新ˈɪnəveɪtɪv
institute 机构、研究所ˈɪnstɪtuːt
integeration 整合ˌɪntɪˈɡreɪʃn
intermediary  中间人ˌɪntərˈmidiˌeri
internal 内部的ɪnˈtɜːrnl
involved 参与ɪnˈvɑːlvd
iterration 迭代ˌɪtəˈreɪʃn
incorrect 不正确的ˌɪnkəˈrekt

labs 实验室læbz
latest 最新的，最晚的ˈleɪtɪst
loop 循环luːp

maintanance 维护ˈmeɪntənəns/
maintain	保持，维护/meɪnˈteɪn/	maintainer保持器 retaine 医保持器
maintainability 可维护性/meɪnˌteɪnəˈbɪlɪti/
flexible	灵活的 /ˈfleksəbl/
scalability  可拓展，可伸缩/skeɪləˈbɪlɪti
reliability 可靠性 rɪˌlaɪə'bɪləti/		rəˌlīəˈbilədē
robustness	健壮性，鲁棒性/roʊˈbʌstnəs/

manufacture 制造业 ˌmænjuˈfæktʃər
mechanical 机械的 məˈkænɪk

nevertheless 然而/ˌnevərðəˈles

occurring 发生əˈkɜːrɪŋ
organizations 组织ˌɔrgənəˈzeɪʃənz
oriented 面向的ˈɔːrientɪd

pleased 高兴，乐于 /pliːzd/
pace 步伐、速度peɪs
perspectives 视角pərˈspɛktɪvz
portfolio 文件夹pɔːrtˈfoʊlioʊ

prior 先前的，占先的ˈpraɪər
prototypes 原型ˈproʊtəˌtaɪps

recommend 推荐/ˌrekəˈmend
release 发布,释放rɪˈliːs
reveal 揭示rɪˈviːl

scenario 方案 səˈnærioʊ
scenarios 方案/情节sɪˈnɛrioʊz
scenes	场景 sinz
since	自从 sɪns
sing	唱歌 sɪŋ 杏
simplification 简化ˌsɪmplɪfɪˈkeɪʃn/
solve 解决	sɑːlv
specific 具体的spəˈsɪfɪk
stakeholders 受益者ˈsteɪkˌhoʊldərz
states 国家、州/状态	 steɪts
stress 压力stres

verification 验证vɛrəfəˈkeɪʃən
versus 对比 vsˈvɜːrsəs/
vision 视野ˈvɪʒn

within 之内wɪˈðɪn
workable 可行的ˈwɜːrkəbl
whom  谁 huːm  与who同义，作为动词或介词的宾语) To whom should I write



============================================
scenario 2  Daily life
============================================
roast	烤，嘲讽 /roʊst
toast	烤的面包，吐司，敬酒，祝酒/toʊst/
formal	正式的/ˈfɔːrml/
grade   等级/ɡreɪd/ second grade
occasionally 偶尔/əˈkeɪʒnəli/
profit	利润/ˈprɑːfɪt/
profile  轮廓/ˈproʊfaɪl/

competition 竞争，竞赛，对手/ˌkɑːmpəˈtɪʃn/
match 匹配，比赛/mætʃ/
race 比赛，种族，角逐/reɪs/

innovation 创新，改革/ˌɪnəˈveɪʃn/
motivation	动机，积极/ˌmoʊtɪˈveɪʃn/
positive	积极性，乐观的/ˈpɑːzətɪv/
live 居住，直播/lɪv , laɪv/

surround 包围，环绕/səˈraʊnd/
surrender 投降，屈服/səˈrendər/

subject 主题/ˈsʌbdʒɪkt、
object 对象，反对/ˈɑːbdʒekt
subjective 主观的/səbˈdʒektɪv/
objective	客观的/əbˈdʒektɪv/

grand 宏伟的/ɡrænd/	grandfather
grande	宏大的/grɑnd/
merry 愉快的/ˈmeri/
marry  结婚/ˈmæri/
roam 漫步/roʊm/

pause 暂停/pɔːz/
resume 简历，恢复继续/rɪˈzuːm/
original	原始的，原来的,独创的/əˈrɪdʒənl/
ordinary 普通的/ˈɔːrdneri/
common	常见的，共同的，普通的/ˈkɑːmən/
comment 评论/ˈkɑːment/
traditional 传统的/trəˈdɪʃənl/
ancestors 祖先/ˈænˌsɛstərz/
reality		现实/riˈæləti/

treasure	宝藏，财富/ˈtreʒər/
trust	信任/trʌst/
medal	奖章/ˈmedl/
metal	金属/ˈmetl/
material	材料/məˈtɪriəl/
silver	银/ˈsɪlvər/
bronze 铜质/ˌbrɑːnz /
bachelor	单身汉，学士/ˈbætʃələr/

mosquito	蚊子/məˈskiːtoʊ/
mentally  精神上，思想上adv/ˈmentəli/
spirit	精神,灵魂n/ˈspɪrɪt/
sprite	雪碧/spraɪt/
steel 钢铁/stiːl/
steal	偷/stiːl/
buck 美元，雄鹿/bʌk/
liquid	液体，液态/ˈlɪkwɪd/
solid	固态/ˈsɑːlɪd/
fries	油炸，炸薯条/fraɪz/
smelly	臭的/ˈsmeli/

invent	发明/ɪnˈvent/
rule  规则/ruːl/
rude  粗鲁/ruːd/

templ 寺庙，神殿，太阳穴/ˈtempl/
temp  临时的/temp/
tempo	节奏，拍子/ˈtempoʊ/
ryhthm	节奏，韵律/ˈrɪðəm/
order 	顺序n，命令v /ˈɔːrdər/
sequence  序列，顺序，顺序排列/ˈsiːkwəns/

influence	影响，作用/ˈɪnfluəns/
fluently  流利的/ˈfluəntli/
option	选项/ˈɑːpʃn/
stock  股票/stɑːk/

authorize  授权vt/ˈɔːθəraɪz/
fancy	想要，认为v; 想象; 花哨，昂贵;/ˈfænsi/

---------------------------------------------
phone	2024-10-31
---------------------------------------------
spam 垃圾邮件电话/spæm/
snooze 打盹/snuːz/
volume	卷，体积，音量ˈvɑːljuːm
mute 沉默的，无声的/mjuːt/
gallery	画廊，相册/ˈɡæləri/
junk	废旧物品/dʒʌŋk/
blurry  模糊不清的/ˈblɜːri/
widgets	小组件/ˈwɪdʒɪts/
launch  启动，发射/lɔːntʃ/

---------------------------------------------
ill
---------------------------------------------
sweat  流汗/swet/
---------------------------------------------
wechat
---------------------------------------------
access 进入/ˈækses/
auto 汽车/ˈɔːtoʊ/
can 能 /kən/
cant 不能/kænt/
barely 仅仅，几乎/ˈberli/
chat 聊天/tʃæt/
correct 对的，修正 /kəˈrekt/
colleagues 同事/ˈkɑligz/	里
college 大学/ˈkɑːlɪdʒ/		咧

tickle 挠痒痒，使快乐/ˈtɪkl/
recall 回忆，召回 /rɪˈkɔːl/

deal 处理，成交/diːl/
overhead	头顶上/ˌoʊvərˈhed /
overdo 	过火，过头
bonus 奖金/ˈboʊnəs/
similar	相似的/ˈsɪmələr/
collapse	崩溃/kəˈlæps/
---------------------------------------------
weather
---------------------------------------------
cloudy 多云、阴天ˈklaʊdi
moderate 中等的，节制的  美ˈmɑːdəreɪt  英/ˈmɒdərət
overcast 阴天 美/ˌoʊvərˈkæst/ 英/ˌəʊvəˈkɑːst/
shower 沐浴，小雨ˈʃaʊər

---------------------------------------------
ali pay
---------------------------------------------
addition 加法 əˈdɪʃn
asset 资产 ˈæset
balance 平衡，余额ˈbæləns
devision 除法 dɪˈvɪʒn
divide  除以 dɪˈvaɪd
debit 借记ˈdebɪt
debt  债务 det
equal to 等于ˈiːkwəl tu

gross 总的，总收入，毛利率ɡroʊs
minus  减ˈmaɪnəs

multi 多种ˈmʌlti
multiplication  乘法ˌmʌltɪplɪˈkeɪʃn
multiply by 乘以ˈmʌltɪplaɪ baɪ

of 属于 əv
offset 抵消，偏移量ˈɔːfset

plus 加上 plʌs

stuff 东西 stʌf
subtraction  减法 səbtrækʃən
============================================
scenario 3  youtube video
============================================
premium 高级，优质的，附加费 ˈpriːmiəm
advertisement 广告/ˌædvərˈtaɪzmənt/

---------------------------------------------
persian	波斯/ˈpɜːrʒn/
gulf	海湾，沟壑/ɡʌlf/

---------------------------------------------

---------------------------------------------
post video
---------------------------------------------
drag 拖拽/dræɡ/

clingy 紧身的，粘人的/ˈklɪŋi/
stray 迷路，流浪/streɪ/
pregnant	怀孕的/ˈpreɡnənt/
caption 字幕标题/ˈkæpʃn/

strict 严格/strɪkt/
restrict 限制/rɪˈstrɪkt/

---------------------------------------------
xinjiang
---------------------------------------------
footage 影片，录像/ˈfʊtɪdʒ/
episode 插曲，剧集/ˈepɪsoʊd/

---------------------------------------------
NBA
---------------------------------------------
Buzzer Beater 绝杀ˈbʌzər ˈbiːtər/ 蜂鸣器
strike	罢工，击打/straɪk/
---------------------------------------------
Judge Mindy and accused booth
---------------------------------------------
accused 被告，控诉，谴责əˈkjuːzd
amends 补偿，赎罪/əˈmendz/
court 法院，法庭，球场 kɔːrt
charge 起诉，控告，充电 tʃɑːrdʒ   discharge 排出，解雇 ，放电dɪsˈtʃɑːrdʒ 
disappointed 失望的ˌdɪsəˈpɔɪntɪd
embarrassed 尴尬 ɪmˈberəs

former 前，以前，昔日ˈfɔrmər
genuinely 真诚的ˈdʒenjuɪnli


judge 法官，审判员，裁判 dʒʌdʒ
recused 回避 rɪˈkjuzd
root 根，支持 ruːt/

---------------------------------------------
How to be native english speaker
---------------------------------------------
applause 掌声əˈplɔːz
accent 口音，重音ˈæksent
clarity 清晰 ˈklærəti unclarity不明确
Eliminate your accent   消除ɪˈlɪmɪneɪt
Immersion  浸泡，沉浸ɪˈmɜːrʒn

---------------------------------------------
CoolVision  The USA city
---------------------------------------------
-------new york----------
avenue 大街/ˈævənuː	
tenant 租户，房客ˈtenənt
rent	租金，租用/rent

-------shanghai-------------
traffic 交通/ˈtræfɪk/    traffic jam 堵车	jam 果酱拥堵 dʒæm/ 
garden	公园ˈɡɑːrdn
park	公园，园区，运动场 pɑːrk
lie		躺，撒谎laɪ
liar	撒谎者ˈlaɪər
lawyer	律师ˈlɔːjər
temple	寺庙ˈtempl/

============================================
scenario 4 Iyrics of songs
============================================
---------------------------------------------
viva la vida 
---------------------------------------------
castl 城堡ˈkæsl/

---------------------------------------------
lazy song
---------------------------------------------
tone 语气，音调  toʊn	at the tone 在语音

============================================
scenario 4 search frequently
============================================
---------------------------------------------
vocabulary
---------------------------------------------
browser 浏览器ˈbraʊzər

craft 工艺 kræft
crash 崩溃，碰撞kræʃ
credit 信用ˈkredɪt
channel 频道，海峡ˈtʃænl

demestic  国内的、家庭的 dəˈmestɪk

fluent 流利ˈfluːənt
frequently 频繁ˈfriːkwəntli/

hint  提示，暗示 hɪnt
hotspot 热点ˈhɑːt spɑːt


immature 幼稚ˌɪməˈtʃʊr
immediately  立即，马上 ɪˈmiːdiətli

mainland 大陆ˈmeɪnlænd


payload 有效载荷ˈpeɪloʊd
previous 前一个ˈpriːviəs
principal 主要的ˈprɪnsəpl

priority 优先 praɪˈɔːrəti
private 私人ˈpraɪvət
province 省ˈprɑːvɪns
proxy 代理 ˈprɑːksi
pronunciation  发音 prəˌnʌnsiˈeɪʃn
presentation 演示，提交，出示ˌpriːzenˈteɪʃn		present 目前，出席，现存ˈpreznt 

register  注册ˈredʒɪstər
refer 参考，提及rɪˈfɜːr

sentence 句子，判决/ˈsentəns/
staff 职工/stæf/

tablet 平板 /ˈtæblət/

tail 尾部 /teɪl/

vocabulary 词汇 /vəˈkæbjəleri/

---------------------------------------------
sentence
---------------------------------------------
grammer	语法/ˈɡræmər/
academic	学术的，学业的/ˌækəˈdemɪk/

A country filled with lies
as in  就像 as in the words that
---------------------------------------------
pronuciation
---------------------------------------------
----æ---------
audio	音频 录音/ˈɔːdiəʊ/
letter 字母 信/ˈletər/
vowels 韵母 /ˈvaʊəl/
consonants 一致的，子音 /ˈkɑnsənənt/
tense	紧张的；紧的；拉紧的；绷紧的/tens/
jaw	下巴，下颌 /dʒɔː/
chin 下巴/tʃɪn/
chain 链子/tʃeɪn/
remain	保持，剩余的 /rɪˈmeɪn/
distort	扭曲，失真/dɪˈstɔːrt/
backed 支持，后退，后援/bækt/  backed you  ，you 发 朱，是舌尖抵上颚原因。 would you

pleasure 快乐，愉悦/ˈpleʒər/
precious 珍贵宝贵/ˈpreʃəs/  treasure
dialect	方言/ˈdaɪəlekt/
----/ɛ/ ---------
front 前frʌnt
phonetic 拼音/fənetɪk/

----/ə/ /ɑ/--------- 	
instructions 指令，教导  /ɪnstrʌkʃ(ə)n/
promise		承诺/ˈprɑːmɪs/
brand new   崭新的/ˌbrænd ˈnuː/
similar	相似的 /ˈsɪmələr/
familiar 熟练的，密友 /fəˈmɪliər/
family	家人/ˈfæməli/

----/t/ ---------
pathologist	病理学家/pəˈθɑːlədʒɪst/
flap 摆动，闪 /flæp/
vanishing 消失的，绝迹ˈvænɪʃɪŋ/
glottal	声门，喉音/ˈɡlɑːtl/
through 经过/θruː/
throw	扔/θroʊ/
throat 喉咙/θroʊt/

-------rhythm---------
syllables	音节/ˈsɪləbəlz/
pitch	投手，音高/pɪtʃ/
nouns	名词/naʊnz/
verbs	动词/vɜːrb/
adjectives	形容词/ˈædʒɪktɪvz/
adverbs	 副词/ˈædvərbz/
intonation	语调/ˌɪntəˈneɪʃn/
dictation	听写/dɪkˈteɪʃn/
dictionary	字典/ˈdɪkʃəneri/
