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

原则是方便发音，便于快读
浊音 i dont know   i on know
     router 路由  ˈruːtər  t 读 d  ruːdər 

sorry?
sorry the what building
sorry can you go over/through that again

put the vocabulary in the sentences to memories. 


about word , I make a big mistake, never memorize the words by one word, should by sentence or phrasal words

# scenario 1 Software Enginner 软件工程师

## HSBC_JD
divison n.部门/dɪˈvɪʒn/
sustain v.维持  /səˈsteɪn/ sustain good divison relationship 维持良好的部门关系
position n.位置，岗位 vt.使处于/pəˈzɪʃn/
primary adj.主要的，重要的，初级的，基本的 n.初选/ˈpraɪmeri/   primary school 小学  junior high school 初中  senior high school  高中
inhabitant  n.居民，栖息动物/ɪnˈhæbɪtənt/
engage v.从事，衔接，聘用，交战，建立密切关系/ɪnˈɡeɪdʒ/ Warning , do not engage with local inhabitant  警告，不要和当地居民接触。
qualification  n.资格，学历，资历/ˌkwɑːlɪfɪˈkeɪʃn/
certificate n.证明，鉴定，证书/ˌsɜːrtɪfɪˈkeɪʃn/
prefer v.更喜欢，较喜欢/prɪˈfɜːr/
attach  v.贴上，重视 /əˈtætʃ/
regular adj.常规的，定期，有规律的 n.常客/ˈreɡjələr/		he's a regular 他是常客。
regulation	n.法规，监管 adj.规定的，必须使用的/ˌreɡjuˈleɪʃn/
adjust	调整/əˈdʒʌst/
constant	常量，恒定的，不断的/ˈkɑːnstənt/
uplift	隆起，提高/ˈʌplɪft/
establish 建立/ɪˈstæblɪʃ/
equivalent	相同的，等量的/ɪˈkwɪvələnt/
mission	 使命，任务/ˈmɪʃn/		missionary 使者
revenues  收益，财政收入/ˈrɛvəˌnuz/
inactive adj.未激活的，不激活的/ɪnˈæktɪv/
deactivate vt.使停止工作/ˌdiːˈæktɪveɪt/
coordinate n.坐标 v.协调/koʊˈɔːrdɪneɪt/
proficient adj.熟练的 n.专家/prəˈfɪʃnt/
pro n.职业选手，职业运动员 adj.职业的，专业的 prep.支持，赞成  adv.站在赞成方面 /proʊ/
profession n.专业，职业/prəˈfeʃn/
verbal adj.口头 n.口供/ˈvɜːrbl/
oral	adj.口头的 n.口语考试/ˈɔːrəl/

prove v.证明，显示/pruːf/
evidence n.证据 v.证明，表明/ˈevɪdəns/
proof n.证明，证据 adj.防... 抗... vt.使防水，防火/pruːf/  bulletproof boy 防弹少年团
audit n.vt. 审计 /ˈɔːdɪt/
diverse	adj.多种多样的/daɪˈvɜːrs/
impact	n.影响，冲击	v.冲击，撞击/ˈɪmpækt/	Some careers have more impact than others. 比其它人更有影响力/冲击力的某些职业生涯。
produce vt.生产，制造，拍摄 n.产品，农产品/prəˈduːs , ˈprɑːduːs/ Our producer produce a good produce. 我们的导演制作一个好产品
producer n.生产商，制造商，制作人，监制，消息队列生产者/prəˈduːsər/
director n.董事，主任，导演，经理，理事/dəˈrektər/   this film director also producer  这部电影导演同样是制片商。

require   vt.要求，需要/rɪˈkwaɪər/     
requirement  n.要求，必要条件/rɪˈkwaɪərmənt/  requirement is clear? 需求是否清晰
scope  n.范围，边界，机会，能力 vt.仔细看，彻底检查 /skoʊp/  where is your ability scope 你的能力边界在哪里？
opinion  n.意见，观点，看法/əˈpɪnjən/  What's your opinion  你怎么看？
azure n.蔚蓝的 /ˈæʒər/  microsoft azure 微软ae泽

## HSBC recruitment
hybrid   adj.混合的，杂种的 n.杂种/ˈhaɪbrɪd/
recruitment	n.招聘,招收 /rɪˈkruːtmənt/
internal adj.里面的，内部的，内心 n.内脏，本质/ɪnˈtɜːrnl/		folder shows phone internal storage .文件夹显示手机内部存储。
external adj.外部的，外界的，外来 n.外部，外观，外面/ɪkˈstɜːrnl/  external HTTPS Load Balancing  外部HTTPS负载均衡
retrieve 取回，恢复，检索，寻回/rɪˈtriːvd/
admire	vt.欣赏，羡慕，钦佩/ədˈmaɪər/	 I just admire your cage,it's pretty good 我很羡慕你的笼子，很棒
efficiency	效率,功率n/ɪˈfɪʃnsi/
eager 渴望的/ˈiːɡər/

occupy  v.占据，占用/ˈɑːkjupaɪ/   this thread occupy memory is too much 这个线程占领内存太多
territory n.领土/ˈterətɔːri/   India actually has occupied territory of China 印度实际占领中国的领土。
terrorist n.adj.恐怖分子/ˈterərɪst/   Missile strike airline is terrorism.  导弹攻击客机是恐怖主义行为。
constrains  v.约束，限制，限定，强制/kənˈstreɪnz/   design constrains 设计约束
tuning v.(收音机、电视)调谐,调频道，调整，矫音 n.收听，调音 /ˈtuːnɪŋ/ performance tuning 性能调优
strategy n.策略，战略，规划 /ˈstrætədʒi/
charter n.特许，许可证 /ˈtʃɑːrtər/  standard chartered bank 标准特许银行 渣打
 

## java
bean  n.豆子，豆荚  vt.击中头部 /biːn/
module n.模块，单元/ˈmɑːdʒuːl/
ram up 向上运送，吊起/ræm ʌp/
atom n.原子/ˈætəm/
optimistic adj.乐观的 /ˌɑːptɪˈmɪstɪk/   optimistic lock
slice n.片，薄片，部分  v.切，割，划  /slaɪs/
yield  n.产量，产出，利润 v.让步，放弃/jiːld/ yield cup by time slice 根据时间片让出cpu
spec  n.规格/spek/  
specification n.规格说明书/ˌspesɪfɪˈkeɪʃn/
hierarchy n.等级制度，统治集团，层次体系/ˈhaɪərɑːrki/
daemon n.守护神，守护进程/ˈdiːmən/
acknowledge v.承认，认可，感谢，致意，告知收悉/əkˈnɑːlɪdʒ/  resume acknowledge  告知简历收悉
acknowledgement  n.致谢，确认，应答/əkˈnɑːlɪdʒmənt/
flood n.洪水，水灾  vt.淹没/flʌd/
protocol n.协议，议定书 v.拟草案，记入议定书 /ˈproʊtəkɑːl/
parallel adj.平行的，并行的  n.纬线 adv.平行地，并列地/ˈpærəlel/
virtual  adj.虚拟的 /ˈvɜːrtʃuəl/ virtual machine 虚拟机
lock v.锁 n.锁定 /lɑːk/
block n.块，阻挡，街区，大楼  vt.阻塞，堵塞，阻碍 /blɑːk/
discard v.丢弃，抛弃  n.被抛弃的人 /dɪˈskɑːrd , ˈdɪskɑːrd/  Do you want discard them. 你想丢弃他们吗
ultimate adj.最终的，终极的，最后的  n.精华，极品/ˈʌltɪmət/
ultra n.过激分子，极端主义者  adj.激进的/ˈʌltrə/
span   n.跨度，范围  vt.跨越，持续，包括 /spæn/
spin v.快速旋转 ，吐 n.高速旋转/spɪn/
proto n.原始，原型/ˈproʊtə/ protobuf 谷歌数据模型
statement n.陈述，表达，报告/ˈsteɪtmənt/
shard	n.碎片/ʃɑːrd/
ineration n.迭代 /ˌɪtəˈreɪʃn/
handle  n.手柄，饼状物，把手 v.处理，应付，控制，操纵/ˈhændl/
invocation n.调用/ˌɪnvəˈkeɪʃn/  invocation handle	动态代理 调用控制
promote vt.促进，推动，提升，促销 /prəˈmoʊt/
process n.过程，进程流程，工序 v.处理，加工，审核 v.队列行进 adj.处理过的/ˈprɑːses , prəˈses/
semaphore n.旗语;信号量  v.发信号 /ˈseməfɔːr/
transfer v.转移，转让，改变，转乘  n.转移，迁移/trænsˈfɜːr , ˈtrænsfɜːr/
restful API representation state transfer 表现层状态传输
cache	n.高速缓存器，隐藏物，贮存器	vt.高速缓存，藏匿/kæʃ/
latches	n.插销，弹簧锁 v.用碰锁锁上/ˈlætʃɪz/
chunk n.组块，大块，厚片 /tʃʌŋk/
buffer n.缓冲器，缓存区，减震器，缓冲物，愚蠢老头 vt.缓存，保护/ˈbʌfər/
bloom vi.开花，变得健康（快活，自信） n.花 /bluːm/  bloom filter 布隆过滤器
offset vt.抵消，偏移量 adj.胶印的  n.抵消，补偿，出发，开端/ˈɔːfset/
idempotent n.幂等 adv.幂等的/aɪˈdempətənt/
serialization n.连载小说，连续剧，序列化 英/ˌsɪəriəlaɪˈzeɪʃn/ 美/ˌsɪriələˈzeɪʃn/
compacton	n.压实，压缩，密封，填料，烧结成型
compatibility n.兼容性，并存/kəmˌpætəˈbɪləti/
compress v.压缩，浓缩，精简 n.敷布，压布/kəmˈpres , ˈkɑːmpres/
schema n.计划或理论的提要，纲要 /ˈskiːmə/ XML schema
evolution  n.演变，进化，发展，渐进 /ˌiːvəˈluːʃn/  java language evolution in 2025.
interact vi.互动，交互，合作，沟通/ˌɪntərˈækt/ interactive message 互动消息
interval n.间隔，间隙，间歇，休息时间/ˈɪntərvl/  halftime means inerval time of Second Half 中场时间意思是距离下半场的时间
font n.字模，字形/fɑːnt/
front n.前面的，表面，正面 adj.在前面 v.向，在前面，领导 adv.在前面/frʌnt/
frontend n.前端 /frʌnt/
backend n.后端
intention n.打算，意图，目的，计划/ɪnˈtenʃn/ insert intention 插入意图
passion n.激情，酷爱/ˈpæʃn/ 

### GCP   问题题目
duration n.持续时间，期间 /duˈreɪʃn/
meet vt.满足 ，会见
toil vt.辛苦工作 n.苦工/tɔɪl/  reduce toil 减少辛劳工作
fire Store 火热的商店
command n.v.命令，指令，控制，指挥 /kəˈmænd/ command line 命令行
armor	n.装甲，盔甲 v.为...装甲，盔甲 /ˈɑrmər/ cloud armor 云盔甲
ban  n.禁令 vt.取缔，明令禁止，禁止 /bæn/
assess vt.评估 评定，估算 /əˈses/ assess app resilience评估软件弹性   assessment考核
assessor n.法庭/官方团体的顾问，审判员，评估员，考核人/əˈsesər/
proctor n.监考人员 vt.监督 /ˈprɑːktər/
voucher n.代金券，券票 /ˈvaʊtʃər/
claim  v.宣称，声称  n.索款，赔款，声明 /kleɪm/  Always try to claim they are the original pure Chinese  一直尝试宣称自己是原始纯种中国人
claim  v.认领，索要/kleɪm/  claim the swags 领取脏物/包裹
badge n.徽章 v.授予徽章 /bædʒ/
perks  n.补贴，津贴 v.竖起 /pɜːrks/  Nipple perk 
figure n.图形，任务，认为，计算 /ˈfɪɡjər ɪt aʊt/ figure it out 了解它

#### Developer
uptime n.(计算机)运行时间  uptime check.运行时间检查
zip n.拉链 v.压缩 /zɪp/ use zipkin and cloud trace for latency metric 使用ipkin 和Trace 来收集延迟指标
patch  n.补丁
redundant  adj.冗余的，多余的，不需要的/rɪˈdʌndənt/ 
recursive   adj.递归，循环 /rɪˈkɜːrsɪv/  remove recursive 递归删除
reCAPTCHA  n.重新验证码
friction  n.摩擦，摩擦力，分歧，不合/ˈfrɪkʃn/  reCAPTCHA add user friction 多重验证码增加用户摩擦。
ease  v.缓解，减轻，缓和 n.容易，自在 /iːz/ ease of use 易用性
corrupt adj.腐败，贪污，受贿  v.损坏，堕落，腐化  /kəˈrʌpt/ file system corrupted 文件系统损坏
intermit v.间歇，暂停   intermit load 间歇性负载
spawn n.产卵，引发，引起/spɔːn/  will Not spawn a separete pipeline 不会引起单独的管道
falsifialbe  网络.伪证的 non-falsifiable不可伪证的
preditermine vt.预先决定，事先安排/ˌpriːdɪˈtɜːrmɪn/ preditermine traffic 预定流量
board n.板 船，董事会 /bɔːrd/  change advisory board  变更咨询委员会（CAB）
modern adj.现代的 n.现代人 英/ˈmɒdn/ 美/ˈmɑːdərn/ modernize 使现代化
restore vt.恢复，修复，归还 /rɪˈstɔːr/ order will be restored秩序将会被恢复
horizontal   adj.水平的，横的  n.水平面，水平线 /ˌhɔːrɪˈzɑːntl/ horizontal pod autoscale pod横向扩展
Meter n.米，计，表  vt.用仪表计量 /ˈmiːtər/ JMeter java仪表计量
mutual n.相互的，共同的/ˈmjuːtʃuəl/ mTLS mutual Transport Layer Security 双向的传输层协议，SSL证书认证
correlate v.相关 adj.相关联的 /ˈkɔːrələt , ˈkɔːrəleɪt/ correlate them 关联它们
monolithic adj.庞大而单一的 /ˌmɑːnəˈlɪθɪk/ monolithic application 单体应用
aggregate  adj.v.聚合，合计 /ˈæɡrɪɡeɪtɪd/ aggregated exports 聚合导出
monotonic  adj.单调的，无变化的 UUID increse monotonically UUID单挑增长
facilitate  vt.促进，使便利 /fəˈsɪlɪteɪt/ facilitate elastic scaling 促进弹性扩展
semantic adj.语义的 /sɪˈmæntɪk/ semantic version 语义的版本
cannonical adj.典型的，经典的 /kəˈnɑːnɪkl/ 
interleave vt.交错，插入，夹进 /ˌɪntərˈliːv/ interleave phone table into customer table ,将电话表交错到用户表
convention  n.公约，协定 /kənˈvenʃn/  tag convention 版本协议
pending  adj.待定 prep.在等待时期  v.悬而未决 /ˈpendɪŋ/
throughout  prep.遍及，贯穿   adv.始终 /θruːˈaʊt/
throughput  n.吞吐量 /ˈθruːpʊt/
issue n.问题，发型 vt.发型，发出 /ˈɪʃuː/   troubleshot the issue 定位问题
dormant  adj.休眠的，蛰伏的，冬眠的 /ˈdɔːrmənt/  dormant bucket‘s peak.  休眠存储桶高峰
degradation n.毁坏，恶化，堕落/ˌdeɡrəˈdeɪʃn/ service degradation 服务降级
diagnose v.诊断 /ˌdaɪəɡˈnoʊs/ diagnose the problem 诊断问题 perfdiag 性能诊断
ship n.船，舰  v.运输，运送 /ʃɪp/ ship them to existing platform 传输到现有系统
summary  n.adj.总结，概要，概括 /ˈsʌməri/
squash n.壁球，南瓜，果汁饮料  v.挤进，挤压，粉碎，制止，打断  /skwɑːʃ/  --squash argument 压缩参数
combine  v.结合，联合，合并  n.联合收割机，集团 /kəmˈbaɪn , ˈkɑːmbaɪn/ combine newly build 结合新构建
reference n.参考，参照，参阅，编号，索引 vt.提及，附加 adj.参考的 /ˈrefrəns/ reference Docker container images 引用Docker镜像
sequential adj.顺序的，按次序的，连续的 /sɪˈkwenʃl/ multiple sequential step 多个连续步骤
chaos  n.混乱，紊乱/ˈkeɪɑːs/ chaos engineering 混沌工程
behave v.表现，有礼貌 /bɪˈheɪv/   how app will behave 软件将会有什么表现
approach  n.方法，方式  v.接近 /əˈproʊtʃ/ 
algorithm n.算法 /ˈælɡərɪðəm/ recommendation algorithm 推荐算法
gradually  adv.逐渐地 /ˈɡrædʒuəli/ gradually enable 逐渐启用
overhead  n.开销，开支 adj.高架，头顶上/ˌoʊvərˈhed , ˈoʊvərhed/ minimize operational overhead 减少运营开销
annotate vt.注释， 注解 /ˈænəteɪt/
bind  v.绑定，结合  n.窘境 /baɪnd/ bind service account 绑定服务账号
emit vt.发出，射出，散发 /iˈmɪt/ emit logs in JSON format发出JSON格式的日志
trigger vt.触发，引起 n.触发器 /ˈtrɪɡər/  triggered by Pub/Sub message 被消息队列触发
regression  n.回归，倒退，退化 /rɪˈɡreʃn/ regression test回归测试
reserve  n.保留，储备，储存量，后备军 v.保留，预定，预约/rɪˈzɜːrv/  reserve hotle 预定酒店
immediate adj.立即的，立刻的 ，直系的，直接的 /ɪˈmiːdiət/ immediate confirmation 立即确认
console vt.安慰，慰藉  n.控制台，操作台/kənˈsoʊl , ˈkɑːnsoʊl/
periodic adj.周期的，定期的/ˌpɪriˈɑːdɪk/ priodic check 定期检查
revoke vt.撤销，取消，废除 n.废弃/rɪˈvoʊk/ revoke document 撤销文档
impersonate vt.模仿，冒充，假冒 adj.人格化的/ɪmˈpɜːrsəneɪt/ service account impersonate 服务账号模拟
excessive adj.多度的，过多的 /ɪkˈsesɪv/ excessive request 过多的请求
rate n.率，速度，价格，比例 v.评价，评估 /reɪt/ rate limit速率限制
generate vt.产生，生成，引起/ˈdʒenəreɪt/ generate high loads生成高负载
corporate adj.公司的，法人的 n.合伙公司 /ˈkɔːrpərət/ corporate laptop 公司笔记本电脑
exfiltration n.渗出，泄露 data exfiltration 数据泄露
pattern n.图案，模式，方式 vt.构成图案 /ˈpætərn/ traffic patterns 流量模式
provenance n.出处，起源，发源地/ˈprɑːvənəns/ Build provenance构建来源
orchestrate vt.编排，策划/ˈɔːrkɪstreɪt/ orchestrate the step 编排步骤
utilitie n.使用，使用程序，效用/juˈtɪlətiz/  utilitie tools实用工具
conduct n.行为，举止， v.实施，传导，安排，引导  /kənˈdʌkt , ˈkɑːndʌkt/ conduct research 实施进行研究
nest n.巢，篮网 v.嵌套 /nest/ nested list 嵌套列表
query n.v.查询，询问，疑问，问号 /ˈkwɪri/ 
integrate v.整合，合并，集成/ˈɪntɪɡreɪt/ integrate with security team's processes. 与安全团队流程相集成。
deny v.否认，拒绝 /dɪˈnaɪ/ 403 Permission Denied 403拒绝许可
offload vt.卸（包袱），转移，减轻/ˌɔːfˈloʊd/ offload SSL 卸载SSL
bulletin n.公告，简报/ˈbʊlətɪn/ security bulletins 安全公告
coincide vi.重合，相符，重叠，同时发生/ˌkoʊɪnˈsaɪd/ coincides with spikes 与峰值重合。
optimal adj.最佳的/ˈɑːptɪməl/ optimal performace最佳性能
ephemeral adj.短暂的，瞬息的/ɪˈfemərəl/ ephemeral disk 临时磁盘
flame n.火焰，激情，火舌，橘红色 v.燃烧 /fleɪm/ flame graph 火焰图
reside vi.居住在，定居于，驻留 /rɪˈzaɪd/ reside in the country.驻留在国家
variable n.变量，可变因素，可变情况/ˈvɛriəbəlz/ environment variables 环境变量
obtain v.获得，存在，赢的/əbˈteɪn/ securely obtain 安全地获取
SSL Secure Socket Layer 安全套接字层
component n.组成部分，成分，不见 adj.成分，构成/kəmˈpoʊnənt/ use profiler as a component by use maven 使用maven将Profiler当成组件
spanner n.扳手 /ˈspænər/
plain n.平原 adj.简单，朴素，直接的 /pleɪn/ plain text 纯文本
perimeter n.周长，边缘，边界/pəˈrɪmɪtər/ same perimeter 相同的边界 security perimeter 安全边界
ingress n.进入，进入权/ˈɪnɡres/
route n.路线，路径，v.路由,按路线发送/ruːt/  route req to backend 路由请求到后端
tunel n.隧道，地道 /ˈtʌnl/ VPN tunels VPN隧道
daemon set 守护进程集
duty n.责任，职责，义务，任务/ˈduːti/ follow the "separation of duties" 遵循职责分离
rapidly  adv. 迅速，高速/'ræpɪdlɪ/ rapidly deploy 快速部署
explicitly adv.明确的，明白的/ɪkˈsplɪsətli/ explicitly commit 显示提交
exponential adj.指数，幂的 /ˌekspəˈnenʃl/  exponential backoff 指数回退
loosely adv.宽松的，松散的，不精确的/ˈluːsli/
coupled v.连接，结合 adj.耦合 couple的过去分词/ˈkʌpld/ loosely coupled 松散耦合
serial n.连续的，串行的/ˈsɪriəl/ serial port 串行端口
ratio n.比率，比例/ˈreɪʃioʊ/  
incompatible adj.不相容的，不兼容的，互斥/ˌɪnkəmˈpætəbl/  backward incompatible 向后不兼容
bastion n.军事堡垒，防御工程/ˈbæstiən/ bastion host 堡垒主机
registry 网络，注册表，登录/ˈredʒɪstri/ Artifact registry 工件注册表。
tenant n.房客，租户/ˈtenənt/ multi-tenant 多租户
graceful adj.优雅的，优美的，雅致的/ˈɡreɪsfl/ graceful shutdown 优雅的关机
porting  网络.移植/ˈpɔːrtɪŋ/ porting app 移植应用
aware adj.知道，意识到 /əˈwer/  identity aware proxy 身份感知代理
credit n.信用，贷款，学分，积分/ˈkredɪt/ add credit to acount balance 添加积分要用户余额。
digest v.消化 n.摘要ˈdaɪdʒest/ use the digest of docker image.使用docker镜像摘要
usage n.使用/ˈjuːsɪdʒ/ CPU usage CPU利用率
against prep.反对 ，违反，靠，应对，对/əˈɡenst/  excutes queries aginst a dataset 对数据集进行查询
plot n.情节  v.绘制  /plɑːt/ Monitoring plot query executed time. 监控绘制查询时间
scope n.范围/skoʊp/ drive.file scope  drive.file范围  
omit v.省略，忽略/əˈmɪt/ omit display when error 错误时忽略显示
surge v.涌，汹涌  n.电流浪涌，急剧上升/sɜːrdʒ/ max surge 最大浪涌
stale n.不新鲜的，陈旧的/steɪl/ stale read 陈旧读取
liveness n.活力，活跃度
readiness n.准备就绪，愿意/ˈredinəs/
probe v.探查，探究/proʊb/ readiness probe 就绪探查
absence  n.缺席，缺乏，不存在，不在/ˈæbsəns/  metric absence指标缺席

#### DevOps  美中时差  5AM-6PM PST +16   9PM-10AM     百度AI10PM-9AM不可信，ChatGPT才对
concerned adj.关注的，担心的，忧虑的 /kənˈsɜːrnd/  your concerned 你的关注
binary /ˈbaɪnəri/ binary files 二进制文件
merchandise n.商品，货品  v.推销 /ˈmɜːtʃəndaɪs , ˈmɜːtʃəndaɪz/ merchandiser 商人
profiler n.轮廓仪，分析器，分析工具/ˈproʊˌfaɪlər/
repository v.仓库，存放处 /rɪˈpɑːzətɔːri/ Artifact repository 工件存放处
fan n.风扇，粉丝/fæn/  fanout 扇出
exempt v.vt.豁免，免除  n.被免除，免税人/ɪɡˈzempt/ exempted any container images that are not deploy to prod 豁免任何未部署到生产的容器镜像。
intent n.意图，目的，计划 adj.专注/ɪnˈtent/
  Communicate your intent to operater 与运维交流你的意图
retention n.保留，保持 /rɪˈtenʃn/
proportion n.比例 /prəˈpɔːrʃn/ as the proportion of report  in a successful response. 作为导致成功响应的报表的比例
vulnerability 网络.脆弱性，漏洞 /ˌvʌlnərə'bɪləti/ vulnerability analysis 漏洞分析
slid v.滑行，滑动 /slɪd/ slid window 滑动窗口
sink v.下沉，降低，挖，掘/sɪŋk/ 日志水槽
slot  n.节目表中的位置，时间，机会，狭槽  v.插入，装入，塞进，投放/slɑːt/
taint vt.污染/teɪnt/  taint the node is no useful for cordon and drain 污染节点对于隔离和排空节点无用
attestor n.证明者
leverage  n.影响力 v.利用/ˈlevərɪdʒ/ gRPC leverage protocal buffers gRRC 利用协议缓冲区
preemptible 网络 可抢占   leverage preemptible VM 利用抢占型虚拟机
redact vt.编辑
rely v.依赖，依靠/rɪˈlaɪ/ rely on 依靠，信赖
relay vt.转发，转播 n.中继设备/ˈriːleɪ/ relay router 中继路由器  relay log 中继日志
manner n.方式 /ˈmænər/ timely manner 及时的方式
breach vt.违反 /briːtʃ/ security breach 违反安全
synthetic adj.合成的 /sɪnˈθetɪk/ synthetic client 合成客户端
instrumentation n.仪器，仪表,检测 /ˌɪnstrəmenˈteɪʃn/ instrumentation coded 编码检测
specify vt.指定，具体说明  /ˈspesɪfaɪ/ specify a paricular version 指定一个特定版本
determine  v.确定，测定，决定/dɪˈtɜːrmɪn/ determine whether an incresed 确定是否增加
pipeline n.管道 /ˈpaɪplaɪn/
remediation n.补救，补习/rɪˌmiːdiˈeɪʃn/ action remedidation 实施补救。
tier n.层，级，等级，阶层 v.层叠 /tɪr/ standard tier 标准层级
exhausted  adj.精疲力竭，耗尽 v.耗尽/ɪɡˈzɔːstɪd/
paremeter n.参数，范围 /pəˈræmɪtər/
cordon n.警戒，封锁，v.分隔，隔离 /ˈkɔːrdn/ cordon the node and drian分隔该节点然后排空
portal n.门户网站，入口站点 /ˈpɔːrtl/
helm  n.舵轮 vt.指挥，带上头盔/helm/
constant n.常量，恒定的，不断的/ˈkɑːnstənt/ heap usage grows constantly 堆使用不断增长
necessary n.必需品 adj.必要的，必须的，不可避免的/ˈnesəseri/ necessary agent 必要的代理
overlay vt.覆盖 /ˌoʊvərˈleɪ , ˈoʊvərleɪ/  overlay directores 不同目录
drift  v.漂流，飘逸 n.偏航 /drɪft/  avoid configuration drift 避免配置偏航
reconcile  vt.调和，协调/ˈrekənsaɪl/ reconcile periodically 定期协调
downtime n.停工期，停机时间/ˈdaʊntaɪm/ with no downtime 不停机
rotate v.旋转，转动 /ˈroʊteɪt/ rotate  every 24 hours  每24小时轮转
attestation n.证明  crate a attestation of workload 创建一个工作负载证明
drain  v.排水，排空  n.排水管，下水道/dreɪn/ drain traffic 引流  drain the node 排空节点
enforce vt.执行，强制执行，强迫 /ɪnˈfɔːrs/ enforce servral constraint templates 强制执行多个约束模板
negotiate v.谈判，协商，通过 /nɪˈɡoʊʃieɪt/ negotiate with the team 与团队协商
exceed vt.超过，超越 /ɪkˈsiːd/ exceeded the error budget 超过错误预算
evaluation n.评价，评审，估计/ɪˌvæljuˈeɪʃn/ evaluation method 评估方法
ingestion  n.摄入 /ɪnˈdʒɛstʃən/ ingestion data 摄取数据
anticipate vt.预料，预见 /ænˈtɪsɪpeɪt/  want to anticipate 想预测
predict v.预测，预报 /ˈnævɪɡeɪt/ unpredictable 不可预测
navigate v.导航，航行 /ˈnævɪɡeɪt/
initiative n.倡议，主动性，积极性/ɪˈnɪʃətɪv/
burn_out n.燃尽，烧尽
burnout n.精疲力竭，过度劳累/ˈbɜːrnaʊt/
eliminate vt.消除，排除，消灭，干掉/ɪˈlɪmɪneɪt/  eliminate toil 消除苦工
stage n.阶段，状态，领域 vt.组织，使发生/steɪdʒ/  staging 试运行、预发布、暂存
encounter n.vt.遭遇，遇到 /ɪnˈkaʊntər/ You encounter a large of outage 你遭遇了大量停机
dedicate  vt.奉献/ˈdedɪkeɪt/  dedicate others achive myself 奉献别人成就自己
dedicated adj.专用的，献身的 v.奉献 /ˈdedɪkeɪtɪd/  dedicated IP 专用IP
extends v.扩展，延长，扩大 /ɪkˈstendz/ extends funtionality 扩展功能
minimize vt.减少，最小化/ˈmɪnɪmaɪz/  minimizing costs 最小化成本
quota  n.配额，定额，指标，定量/ˈkwoʊtə/ project quota 项目配额
capacity n.容量 adj.充满的 /kəˈpæsəti/  plan for capacity 规划容量
consist v.包括，由组成 /kənˈsɪst/
consistent adj.一致的 /kənˈsɪstənt/ inconsistent 不一致
privilege n.特权，荣幸，荣耀，权利，权限
least  adv.最小，最少 adj.小的 /liːst/ principle of least privilege 最小权限原则
perform  v.执行，演奏，表演/pərˈfɔːrm/
performance n.表演，演出，表现，性能  adj.性能卓越的/pərˈfɔːrməns/
identify vt.识别，确认，发现，鉴定 /aɪˈdentɪfaɪ/  identify the machine type 识别机器类型
revision n.修订，修改，复习/rɪˈvɪʒn/ latest revision 最后修订
suspect n.犯罪嫌疑人 v.怀疑/səˈspekt , ˈsʌspekt/
adopt v.采用，采取，领养/əˈdɑːpt/
adapt v.适应 /əˈdæpt/ adapted to future change 适应将来的变化
trunk   n.树干，主干，主题  adj.主干的  v.把放入行李箱/trʌŋk/
trunk-based   基于主干
idle adj.空闲的，闲置的 v.空转，无所事事 /ˈaɪdl/ idle instances  空闲实例
gauge  vt.测量，判定 n.事实，依据，尺度，标准/ɡeɪdʒ/
critical  adj.关键的，批评的  /ˈkrɪtɪkl/ business-critical 业务关键   .批判性精神是关键的创新精神的第一步。
criteria n.标准 /kraɪ'tɪriə/
premise 	n.前提，假定  v.假定，引导 /ˈpremɪs/  on-premise 内部部署，本地部署
velocity n.速度，高速，快速 /vəˈlɑːsəti/  deployment velocity 部署的速度
indicator  n.指示器，指标，标志/ˈɪndəˌkeɪtər/
appropriately adv.合适的，适当的/ə'proprɪrtlɪ/  appropriately indicator 合理的指标
minigate vt.减轻，缓和/ˈmɪtɪɡeɪt/
outage n.停电期间，停机 /ˈaʊtɪdʒ/
entry  n.条目，进入，参与/ˈentri/ log entries 日志条目
leak v.漏，泄露 n.漏洞，透漏，裂缝，缝隙/liːk/ tiktok leak 抖音泄露
telephone  n.电话 /ˈtelɪfoʊn/  /ˈtelefoʊn/
telemetry  n.远距离测量，遥测  /təˈlemətri/ OpenTelemetry 开放遥测
trace vt.追踪，追溯，发现，找到 n.痕迹，微量，轨迹 /treɪs/
failure n.失败，故障，倒闭，未做/ˈfeɪljər/  you trace the failure  你追踪故障
policy n.政策，方针，原则，保险但/ˈpɑːləsi/
cannary  n.金丝雀，淡黄色/kəˈneri/
lag v.滞后,落后于，发展缓慢 n.滞后/læɡ/
latency n.延迟,潜伏，潜在因素/'leɪtənsɪ/
legacy n.遗产，遗留，后遗症  adj.已停产的/ˈleɡəsi/
ingress n.进入，进入权，入境权 /ˈɪnɡres/
postmortem n.验尸， 事后分析，事后检讨/poʊstˈmɔrtɛm/ 
tail n.尾 ，尾巴，尾部  vt.跟踪，尾随 /teɪl/  to tail the log file  	去跟踪日志文件

provision  n.提供 ，规定，条款 vt.为...提供所需物品 /prəˈvɪʒn/ provision a shared VPC 提供一个共享的VPC
terraform  v.将行星 地球化/ˈterəfɔːrm/  terraform is a provision tool .  terraform是一个规定条款工具

### Interview


### System Design
tolerant adj.宽容的  /ˈtɑːlərənt/
avoid  vt.避免,防止 /əˈvɔɪd/  avoid any feature loss  避免任何特性损失
demonstrate v.证明，演示，示范，论证，表现 /ˈdemənstreɪt/
bottleneck n.瓶颈,障碍 v.阻塞，堵塞/ˈbɑːtlnek/
chaos n.混乱，紊乱，杂乱/ˈkeɪɑːs/

### Test
mock v.嘲弄，嘲笑，讥笑 adj.模拟，演戏  n.嘲笑  adv.假装的 /mɑːk/  mock data 模拟数据
anonymous adj.匿名的，不具名的/əˈnɑːnɪməs/   anonymous organization 匿名组织

### Evengrande
lack  n.缺乏，匮乏，短缺， v.缺乏，没有 /læk/
clue  n.线索，迹象，解答提示 v.提示，提供线索/kluː/  lack of clues 缺乏线索

### Term  术语/tɜːrm/
#### 数量
several det./pron 几个，一些，数个 adj.不同的，各种各样的/ˈsevrəl/
integer	n.整数 /ˈɪntɪdʒər/
integration n.整合,一体化，结合,集成/ˌɪntɪˈɡreɪʃn/


#### 时间
millisecond  n.毫秒，千分之一秒/ˈmɪlisekənd/




### consistency models 一致性模型
single 单例
strict serializable 严格可序列化
serializeble  序列化
repeatable read	可重复读
snapshot isolation 快照隔离
cursor stablility 游标稳定性
monotonic atomic view 单调原子视图
read committed	 读已提交
read uncommited  读未提交

distribute 分布式
linearizable	线性化
sequential	顺序的
causal 因果
PRAM 
writes follow reads  写跟随读
monotonic reads 单调读
monotonic writes 单调写
read your writes 读几所写

unavailable 不可用
sticky available 粘性可用
total available 完全可用


## Tell me about your self tips

essential adj.本质上，基本上/ɪˈsenʃəli/  The essentails of GCP  GCP基础


## Senior Software Enginner interview

achieve 实现əˈtʃiːv
activities 活跃ækˈtɪvətiz
actual 实际ˈæktʃuəl

advisor 顾问/ædˈvaɪzər
affect n.影响,使感染，假装/əˈfekt/
effect n.影响，外观，声响，效果，效应，结果 vt.使发生，实现，引起/ɪˈfekt/

archive  归档 ˈɑːrkaɪv
associations 协会əˌsoʊsiˈeɪʃənz
atmosphere 气氛ˈætməsfɪr       how would you describe your working atmosphere and some people with whom your working with
auto n.汽车 adj.与汽车相关的/ˈɔːtoʊ/  new energy auto 新能源汽车
automat  自动售货机/ˈɔːtəmæt/
automated 自动化ˈɔːtəmeɪtɪd
automatically 自动ˌɔtəˈmætɪkli/
areas 地区，地域ˈɛriəz

basis 基础 ˈbeɪsɪs/
budget	预算ˈbʌdʒɪt
career 职业kəˈrɪr
certain 确定/某些sɜːrtn   uncertainties不确定ənˈsɜrtəntiz


complex 复杂的 kəmˈpleks
compliance n.遵从，合规性/kəmˈplaɪəns/  config compliance 配置合规性
contact 接触，联络ˈkɑːntækt
continuous 连续的 kənˈtɪnjuəs
countless 不可计算ˈkaʊntləs

defined 定义/明确dɪˈfaɪnd
deliver 交付dɪˈlɪvər	deliverable 可交付的dɪˈlɪvərəbl
depth	深度depθ
device 设备 dɪˈvaɪs
digest	消化 ’daɪdʒes
discover 发现 dɪˈskʌvər

elaborate adj.v.复杂的，详尽的，精心制作的 /ɪˈlæbəreɪt/
electrical 用电的 /ɪˈlektrɪkl/
elegant 优雅的，简洁的/ˈelɪɡənt/

evaluate vt.评价，评估/ɪˈvæljueɪt/
eventual 最终/ɪˈventʃuəl/
evolving 进化/iˈvɑːlvɪŋ/
executives 主管/ɪgˈzɛkjətɪvz/	
expectations 期望/ˌɛkspɛkˈteɪʃənz/
expert 专家/ˈɛkspərt/
exploring	探索/ɪkˈsplɔːrɪŋ/

field /领域fiːld/
foreman 领班/fɔːrmən/
frustrated 沮丧，无效/ˈfrʌstreɪtɪd/

gain 获取/ɡeɪn/
guide 指导/ɡaɪd/   guidelines 准则/ˈgaɪˌdlaɪnz/

implement 实施/执行/ˈɪmplɪment /
industry 行业/ˈɪndəstri/
innovative 创新/ˈɪnəveɪtɪv/
federal adj.联邦的 n.同盟/ˈfedərəl/
institute n.机构、研究所/ˈɪnstɪtuːt/  federal correctional institute california	 加州联邦惩戒所
intermediary  中间人/ˌɪntərˈmidiˌeri/
internal 内部的/ɪnˈtɜːrnl/
involved 参与/ɪnˈvɑːlvd/
iterration 迭代ˌ/ɪtəˈreɪʃn/
incorrect 不正确的/ˌɪnkəˈrekt/

labs 实验室/læbz/
latest 最新的，最晚的/ˈleɪtɪst/
loop 循环/luːp/

maintanance 维护/ˈmeɪntənəns/
maintain	保持，维护/meɪnˈteɪn/	maintainer保持器 retaine 医保持器
maintainability 可维护性/meɪnˌteɪnəˈbɪlɪti/
flexible	灵活的 /ˈfleksəbl/
scalability  可拓展，可伸缩/skeɪləˈbɪlɪti/
reliability 可靠性 /rɪˌlaɪə'bɪləti/		rəˌlīəˈbilədē
robustness	健壮性，鲁棒性/roʊˈbʌstnəs/

manufacture 制造业 /ˌmænjuˈfæktʃər/
mechanical 机械的/ məˈkænɪk/

nevertheless 然而/ˌnevərðəˈles/

occurring 发生/əˈkɜːrɪŋ/
organizations 组织/ˌɔrgənəˈzeɪʃənz/
oriented 面向的/ˈɔːrientɪd/

pleased 高兴，乐于 /pliːzd/
pace 步伐、速度peɪs
perspectives n.视角/pərˈspɛktɪvz/   in your perspectives  在你的视角
portfolio n.文件夹,公事包/pɔːrtˈfoʊlioʊ/	dont forget bring your portfolio 别忘记带你的公文包	   open a folder 打开文件夹

prior 先前的，占先的/ˈpraɪər/    come back prior 返回前面
prototypes 原型/ˈproʊtəˌtaɪps/	 ask ui did she finish her prototypes  问一下UI完成原型了吗？

recommend 推荐/ˌrekəˈmend/		what organizations do you want to recommend?  有哪个机构想推荐的？
release 发布,释放/rɪˈliːs/		tonight we gonna release the new version	今晚将发布新版本
reveal 揭示/rɪˈviːl/			real history will reveal the Turth	 真实的历史将揭露真相

scenario 方案 /səˈnærioʊ/		
scenarios 方案/情节/sɪˈnɛrioʊz/		vendor should provide two scenarios at least 供应商至少提供两种方案
scenes	场景 /sinz/				at this scenes 在这个场景下。
since	自从 /sɪns/				
sing	唱歌/ sɪŋ /杏
simplification n.简化/ˌsɪmplɪfɪˈkeɪʃn/	 that is simplification scenario. 这是一个简化方案
solve v.解决	/sɑːlv/				solve problem 解决问题
specific adj.具体的,特定的，明确的; n.特性，细节，特征/spəˈsɪfɪk/			
stakeholders n.受益者/ˈsteɪkˌhoʊldərz/
states n.国家、州/状态	/ steɪts/
stress n.压力/stres/				under low stress 在低压力下；

verification n.验证,验收/vɛrəfəˈkeɪʃən/    captha mean website's verification code; captcha是网页验证码 
captcha n.验证码/ˈkæptʃə/
versus v.对比 vs /ˈvɜːrsəs/		doubao versus chatGPT 豆包vsGPT
vision n.视野/ˈvɪʒn/			coolvision is a good vision . 酷视野是一个好的视野

within adv.之内；prep.在...之内；n.内部/wɪˈðɪn/    
workable adj.可行的/ˈwɜːrkəbl/
whom  谁 huːm  与who同义，作为动词或介词的宾语) To whom should I write


## CTF

miscellaneous	adj. 各种各样，混杂 /ˌmɪsəˈleɪniəs/  misc 杂项   
reverse	 v.颠倒，反转  n.背面，反面	adj.反向的，逆向/rɪˈvɜːrs/     reverse string 反转字符串
crypto	n.加密货币，秘密成员，密码学/ˈkrɪptoʊ/	
Trojan n.特洛伊人，木马/ˈtroʊdʒən/
intercept	vt.拦截  n.拦截/ˌɪntərˈsept/        packet capture mean intercept browser's request  抓包意味着拦截浏览器请求
payload n.有效载荷/ˈpeɪloʊd/  
emulator  n.仿真器，模拟器/ˈemjuleɪtər/   wine is not emulator.
assert v.断言，生效，维护权益，坚持主张/əˈsɜːrt/ 
encode vt.编码  /ɪnˈkoʊd/
decode vt.解读，解码 /ˌdiːˈkoʊd/
fuzz n.茸毛，绒毛 /fʌz/  laoling got a lot of fuzz on his hand.老凌手上有一堆（法子）绒毛
cypher n.密码，暗号 /ˈsaɪfər/
cyber adj.电脑网络的 /'saɪbə/ cyber peace 网络太平
Unicode n.统一码
linux n.一种计算机操作系统/ˈlinʊks/ 
linus 莱纳斯/ˈlaɪnəs/
bash v.猛击,严厉批评，猛撞  n.猛击，重击/bæʃ/
clash n.冲突；矛盾，交锋，分歧 v.冲突，比赛 /klæʃ/

# scenario 2  Daily life  日常生活
regard  vt.认为，看待  n.注意，关注，尊重,致意，问候 /rɪˈɡɑːrd/   best regard 最好的问候
regardless adv.不管，不顾，不加理会  adj.不留心的，毫无价值的，不尊重的  /rɪˈɡɑːrd/  regardless of country .不管国家
manner n.方式，方法，礼貌   /ˈmænər/  good manner 好的行为举止
peer n.同龄人，同辈,同行，对等  vt.仔细看，端详/pɪr/  VPC peering VPC对等连接
recognize  vt.认识，承认，认可，接受，赞成/ˈrekəɡnaɪz/  I dont recognize ccp, because I did not vote or election ever
election  	n.选举，当选 /ɪˈlekʃn/

## clothing 衣服/ˈkloʊðɪŋ/
jersey n.运动衫/ˈdʒɜːrzi/
hoodie n.连帽衫，连帽夹克/ˈhʊdi/


## dental
remain	v.留下，逗留，停留，保持，保持不变，n.剩余的 /rɪˈmeɪn/ 
retainer n.保持器 /rɪˈteɪnər/
tooth n.牙齿 v.使具齿状/tuːθ/  复数teeth
appointment n.约会，委任，预约，任命，职位，约定 /əˈpɔɪntmənt/
dental adj.牙齿的，牙科 n.齿音/ˈdentl/   I've got a dental appointment at 3 o'clok. 我约了3点看牙医

## geography 地理/dʒiˈɑːɡrəfi/
countryside 郊野
hill	小山
mountain	高山
valley	n.山谷，流域，溪谷/ˈvæli/
wood	植林
forest	森林/ˈfɔːrɪst/
field   原野
meadow	n.草地 /ˈmedoʊ/
plain	n.平原 /pleɪn/
moor	n.荒野/mʊr/
bog		n.沼泽/bɑːɡ/
swamp	n.沼泽地/swɑːmp/
fence	n.栅栏/fens/
ditch	n.沟渠/dɪtʃ/
desert	沙漠
glacier	n.冰川/ˈɡleɪʃər/
jungle	n.丛林/ˈdʒʌŋɡl/
rainforest	雨林
volcano	火山/vɑːlˈkeɪnoʊ/
stream	溪流
canal	运河/kəˈnæl/
pond	n.池塘/pɑːnd/
reservoir 水库/ˈrezərvwɑːr/
dam		水坝/dæm/
peak  n.高峰，顶峰/piːk/

ocean	大洋/ˈoʊʃn/
sea		海洋
coast/shore	海岸 /koʊst/ /ʃɔːr/
beach	海滩
cliff	断崖/klɪf/
island	岛屿/ˈaɪlənd/
peninsula	半岛/pəˈnɪnsələ/
tide	潮汐/taɪd/
wave	海浪
pier	码头/pɪr/
lighthouse	灯塔
harbour		n.港口,港湾，海湾/ˈhɑːrbər/
gulf  n.海湾，沟壑/ɡʌlf/

aurora n.极光，曙光/ɔː'rɔːrə/

## food

wine n.葡萄酒； v.喝酒/waɪn/   grab some wine. 喝点小酒
meat n.肉类 /miːt/  meat ball 肉球
bread n.面包，钱 vt.撒面包屑/bred/


## family guy
waste vt.浪费，白费  n.废物，浪费，垃圾/weɪst/
mandarin n.普通话，柑橘/ˈmændərɪn/
delicate adj.精致的，微妙的 n.精美的衣物，精美的食物/ˈdelɪkət/
normal adj.正常的，一般的，典型的，精神正常/ˈnɔːrml/
pardon 	n.原谅，赦免，宽恕，特赦 int.对不起，(请重复说一次)什么，再说一遍 vt.赦免，原谅/ˈpɑːrdn/  IPA /ˈpɑːrdən/
gossip	n.流言蜚语，闲聊， vi.说三道四/ˈɡɑːsɪp/
roast	烤，嘲讽 /roʊst/
toast	烤的面包，吐司，敬酒，祝酒/toʊst/
steak 	牛排，肉排，鱼排，肉块/steɪk/  
stake 桩，股份，赌注，重大利益/steɪk/	stakeholder 受益人
form  n.表格，形式，类型 v.构成，形成，出现，产生 英/fɔːm/ 美/fɔːrm/
formal	adj.正式的,庄重的 n.礼服的社交集会，夜礼服/ˈfɔːrml/   formal speech  正式的演讲
former  n.模型，样板,创造者，构成者 adj.前，前者，昔日的/ˈfɔːrmər/Former is used to describe someone who used to have a particlular job昔日的工作
grade   等级/ɡreɪd/ second grade
occasionally 偶尔/əˈkeɪʒnəli/
profit	利润/ˈprɑːfɪt/
profile  轮廓/ˈproʊfaɪl/

competition 竞争，竞赛，对手/ˌkɑːmpəˈtɪʃn/
match 匹配，比赛/mætʃ/
race 比赛，种族，角逐/reɪs/
racism n.种族歧视/ˈreɪsɪzəm/


innovation 创新，改革/ˌɪnəˈveɪʃn/   
motivation	动机，积极/ˌmoʊtɪˈveɪʃn/
positive	积极性，乐观的/ˈpɑːzətɪv/
live 居住，直播/lɪv , laɪv/

surround 包围，环绕/səˈraʊnd/
surrender 投降，屈服/səˈrendər/

subject 主题/ˈsʌbdʒɪkt/
object 对象，反对/ˈɑːbdʒekt/
subjective 主观的/səbˈdʒektɪv/
objective	客观的/əbˈdʒektɪv/

grand 宏伟的/ɡrænd/	grandfather
grande	宏大的/grɑnd/
merry 愉快的/ˈmeri/
marry  结婚/ˈmæri/
roam 漫步/roʊm/

pause 暂停/pɔːz/
resume n.简历，v.恢复继续,中断后继续/rɪˈzuːm/   pause then resume.暂停后开始
original	原始的，原来的,独创的/əˈrɪdʒənl/
ordinary 普通的/ˈɔːrdneri/
common	常见的，共同的，普通的/ˈkɑːmən/
comment 评论/ˈkɑːment/
traditional 传统的/trəˈdɪʃənl/
ancestors 祖先/ˈænˌsɛstərz/
reality		现实/riˈæləti/

treasure	宝藏，财富/ˈtreʒər/
trust	信任/trʌst/
medal	n.奖章，勋章/ˈmedl/
metal	n.金属/ˈmetl/  flap t make metal sound same with medal  flap t让金属和奖章发音一样
material	材料/məˈtɪriəl/
silver	银/ˈsɪlvər/
bronze 铜质/ˌbrɑːnz /
bachelor	单身汉，学士/ˈbætʃələr/

mosquito	蚊子/məˈskiːtoʊ/
mosques   清真寺/mɑsks/

mentally  精神上，思想上adv/ˈmentəli/
spirit	精神,灵魂n/ˈspɪrɪt/
sprite	雪碧/spraɪt/
steel 钢铁/stiːl/
steal	偷/stiːl/
buck n.美元，雄鹿/bʌk/
liquid	液体，液态/ˈlɪkwɪd/
solid	固态/ˈsɑːlɪd/
fries	油炸，炸薯条/fraɪz/
smelly	臭的/ˈsmeli/

invent	vt.发明/ɪnˈvent/   innovation means invent something new. 创新意味发明新东西
inventor  n.发明者，发明家 /ɪnˈventər/  inventor of rice farming  水稻发明者
invest  v.投资/ɪnˈvest/
pure	adj.纯的，纯净的，完全的 /pjʊr/  白话飘er

rule  规则/ruːl/
rude  粗鲁/ruːd/

templ 寺庙，神殿，太阳穴/ˈtempl/
temp  n.临时的,临时工/temp/ temp table 临时表
tempo	节奏，拍子/ˈtempoʊ/
ryhthm	节奏，韵律/ˈrɪðəm/
order 	顺序n，命令v /ˈɔːrdər/
sequence  序列，顺序，顺序排列/ˈsiːkwəns/

influence	影响，作用/ˈɪnfluəns/
fluently  流利的/ˈfluəntli/
option	n.选项，选修  vt.选择，调用球员/ˈɑːpʃn/  solution option 方案选择
dump	v.n. 倾倒，转储(内存信息)，倾销/dʌmp/  dump files 转储内存信息文件
stock  n.股票,库存 vt.存货，储备/stɑːk/		dump stock 抛售股票/库存；
inventory	n.库存，存货，家具/财产清单  vt.开列清单 /ˈɪnvəntɔːri/

author n.作者，作家 vt.编写，著作，写作 /ˈɔːθər/  author of this book. 这本书的作者
authorize  vt.授权，批准/ˈɔːθəraɪz/   author authorize to you . 作者授权给你
reputation n.名誉，名声/ˌrepjuˈteɪʃn/
fortune n.财富，命运  vt.给与财富偶然发生 /ˈfɔːrtʃən/
fancy	想要，认为v; 想象; 花哨，昂贵;/ˈfænsi/   fancy life	奢华的生活；
commercial	adj.商业的;n.广告		
tremendous	巨大的，惊人的/trəˈmendəs/  It's really tremendous 真令人震惊；

fart 放屁/fɑːrt/   Peter just fart 皮特放了个屁
gross	adj 毛的，总的，令人恶心的/ɡroʊs/		that's gross  这令人恶心； gross profit 毛利润
vibe 	n 气氛，感应，环境/vaɪb/		English vibe	英语氛围
taste	n 味道，滋味，品味  v 吃 喝 品尝/teɪst/    he really got taset 真有品味
consent	n.同意，允许,准许，赞同 vt.同意，允许/kənˈsent/
decline  n.减少,下降，衰退 v.下降，婉言拒绝 /dɪˈklaɪn/

suppose v. 假设/səˈpoʊz/  suppose be good luck	假设是好运呢	
assume v.假定，认为/əˈsuːm/ a lot of people wrongly assume 大多数人错误的假设 
pretend v.假装，模拟 /prɪˈtend/

discipline n.纪律，训练 v.训练，处罚，严格律己/ˈdɪsəplɪn/	we got discipline
term n.学期，期限，任期，项，术语/tɜːrm/  in terms of 在...方面
item n. 项目，一则/ˈaɪtəm/


complain	v.抱怨，发牢骚，埋怨/kəmˈpleɪn/		stop complain 停止抱怨
explain	v.解释，说明/ɪkˈspleɪn/		

flare	v.(火光)闪耀 n.照明弹/fler/		cloudflare 云闪
mean	adj.平均的，卑鄙的，低劣的； v.意味，意欲/miːn/
question	n.问题 v.问，质疑/ˈkwestʃən/
quest	n.追求 v.探索/kwest/	quest crew
dive 	n.v.潜水/daɪv/ dive into  深入

valley  n.山谷，流域，溪谷/ˈvæli/  silicon valley 硅谷
village n.村庄，村民/ˈvɪlɪdʒ/  	small village 小村庄

bit  n.一点，比特/bɪt/  a little bit 一点点
bite  n.v. 药/baɪt/   street sharks bite 鲨鱼侠咬
bitter n.苦的，严寒的  vt.使变苦  /ˈbɪtər/

calm  adj.vt.n 平静的，使平静/kɑːm/   calm down 冷静
contribute v.贡献，捐助 /kənˈtrɪbjuːt/
community n.社区 /kəˈmjuːnəti/    contribute our community 贡献我们的家园
communist  n.共产主义/ˈkɑːmjənɪst/   china communist party 

grab  v.抓住，取，吃，喝，拿 /ɡræb/  grab a cup of coffee 喝咖啡
rope n.绳子 vt.套，捆 /ɡræb/  miss the rope  没抓住绳子
traitor  n.叛徒，卖国贼 /ˈtreɪtər/   proud American traitor 骄傲的美国叛徒
medium  n.媒体，媒介，介质  adj.中等的，中间的，半熟的 /ˈmiːdiəm/	medium soft toothbrush 中软牙刷
middle  n.中间，中部，中心，中央	adj.中间的 /ˈmɪdl/    middle school 中学
fusion  n.融合；结合，核聚变/ˈfjuːʒn/   cold fusion was stable diffusion 冷核聚变稳定扩散
diffusion  n.扩散，漫射，传播 /dɪˈfjuʒən/	stable diffusion 稳定扩散
gather v.聚集，搜集，采集 n.聚集，收缩，衣褶 /ˈɡæðər/    gather information  聚集信息
universal adj.普遍的，共同的，全世界的  n.一般性/ˌjuːnɪˈvɜːrsl/
primer n.底漆，初级读本，入门启蒙书 /ˈpraɪmər/  universal primer 通用启蒙

cannal  n.运河，灌溉渠，导管 v.开运河，疏导/kəˈnæl/  ali cannal 阿里运河项目  pinglu cannal 平陆运河
close v.关门，关闭，缩小，接近，终止  n.结束，死胡同  adj.密切的 adv.接近，靠近/kloʊz , kloʊs/   close the door 关门
closer adv.接近，靠近 adj.接近，密切的   n.终止 /kloʊz , kloʊs/  closer asean 接近东盟
brief  adj.简明的，短暂的  n.指示 vt.介绍情况 /briːf/ a brief summary 一个简短的总结
doggie n.狗狗 /ˈdɔgi/
puppy	n.小狗，傲慢自负的青年小子/ˈpʌpi/
doge n.神烦狗柴犬表情包/doʊdʒ/

ensure	v.确保，保证 /ɪnˈʃʊr/  ensure a smooth transfer 确保顺利交接
guarantee n.保证，担保 v.保证，保障 /ˌɡærənˈtiː/   he gave me a guarantee 他想我保证
assure	vt.保证，确保  /əˈʃʊr/ but i assure you i did not. 但我向你保证我不会。

### land /lænd/  n.土地

country	n.国家，向下/ˈkʌntri/   country music 乡村音乐
state  n.状态，国家，美国，政府，州  adj.州的	vt.规定，说明声明 /steɪt/
province  n.省份， 领域 /ˈprɑːvɪns/
city n.城市 /ˈsɪti/
district	n.区  v.把..分区/ˈdɪstrɪkt/
county  n.县，郡  adj.上流社会，世家子弟 /ˈkaʊnti/
avenue  n.大街，途径，选择，大道/ˈævənuː/
street	n.街道 /striːt/
suburb  n.郊区，城外/ˈsʌbɜːrb/    xiongan city was beijing suburb before
village n.乡村，村庄，村民/ˈvɪlɪdʒ/  	small village 小村庄
town  n.镇，城镇 /taʊn/
downtown  n.市中心 adj.闹市区/ˈdaʊntaʊn/   cbd is downtown usually  cbd通常在市中心


### movie
studio	n.工作室，演播室，电影公司，录音棚/ˈstuːdioʊ/   establish our actors/actress studio 成立我们的男女演员工作室 
supervisor	n.监督人，主管人，指导人/ˈsuːpərvaɪzər/ visual effects supervisor 特效指导，视觉效果总监


## phone	2024-10-31
stopwatch n.秒表，码表，跑表/ˈstɑːpwɑːtʃ/
spam 垃圾邮件电话/spæm/
snooze 打盹/snuːz/
volume	n.卷，体积，音量 adj.大量的 v.收集成卷/ˈvɑːljuːm/  Handles a high volum writes  处理大量写入
mute adj.沉默的，无声的/mjuːt/
gallery	画廊，相册/ˈɡæləri/		app gallery
junk	n.废旧物品，无用的东西 vt.废弃，丢弃/dʒʌŋk/
blurry  模糊不清的/ˈblɜːri/
widgets	小组件/ˈwɪdʒɪts/
launch  n.v 发起，发射/lɔːntʃ/


## ill

sweat  流汗/swet/
tough adj.艰难的，强硬的，严厉的，艰苦的 n.恶棍，暴徒 v.坚持，忍受，忍耐 adv.强硬的，顽强的 /tʌf/
last  det.最后的，末尾的，最近的 adv.最后，最终 n.末尾  v.持续，持久  adj.最后的，末尾的 /læst/  tough times never last. 艰难的时光不会太久

## wechat
exhaust adj.精疲力竭，耗尽的 v.耗尽，用完/ɪɡˈzɔːst/
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
collapse  n.崩溃,倒塌 v.昏倒，晕倒 /kəˈlæps/ my phone collapse 我的手机崩溃/晕倒了 
clap	鼓掌/klæp/
palm n.手掌,棕榈树/pɑːm/  facepalm 捂脸笑; palm tree 棕榈树
wirus 病毒/ˈvaɪrəs/
sticker  n.贴纸，粘贴标签/ˈstɪkər/
refund n.退款 v.退还/ˈriːfʌnd/
allow v.允许/əˈlaʊ/
quote n.v.引用/kwoʊt/  wechat allow quote another sentence in conversation。微信允许在对话中引用另一句话


## weather

cloudy 多云、阴天/ˈklaʊdi/
mode  n.模式，方法/moʊd/     design patterns has a lot of mode  设计策略有很多模式
model n.模型，设计，样本 v.复制 adj.规范的 /ˈmɑːdl/
modern adj.现代的，时髦的  n.现代人 /ˈmɑːdərn/
moderate 中等的，节制的  美/ˈmɑːdəreɪt/  英/ˈmɒdərət/
overcast 阴天 美/ˌoʊvərˈkæst/ 英/ˌəʊvəˈkɑːst/
shower 沐浴，小雨ˈʃaʊər
accompany v.伴随，陪伴/əˈkʌmpəni/
company n.公司，陪伴，宾客/ˈkʌmpəni/   our company we work for witch called evergrande.我们公司叫恒大



## alipay

addition 加法 /əˈdɪʃn/
asset 资产 /ˈæset/
balance 平衡，余额/ˈbæləns/
devision 除法 /dɪˈvɪʒn/
divide  除以 /dɪˈvaɪd/
debit 借记/ˈdebɪt/
debt  债务 /det/
equal to 等于/ˈiːkwəl/ tu

gross 总的，总收入，毛利率, adj. 令人恶心的/ɡroʊs/
wage n.工资，工钱  vt.开始，发动/weɪdʒ/
minus  减/ˈmaɪnəs/
minimun n.最小值，最少量 adj.最小的，最低的/ˈmɪnɪməm/ the minimun wage of 广州 is 2033 mybe 广州最低工资为2033

multi 多种/ˈmʌlti/
multiplication  乘法/ˌmʌltɪplɪˈkeɪʃn/
multiply by 乘以/ˈmʌltɪplaɪ baɪ/

of 属于/əv/


plus 加上 /plʌs/

stuff 东西 /stʌf/
subtraction  减法 /səbtrækʃən/
estimate	估计，估算/ˈestɪmət/

individual n.个人 adj.单独的，个别的，独特的 /ˌɪndɪˈvɪdʒuəl/   pay to individual 向个人支付

# scenario 3  youtube video 油管视频

theory n.理论，原理，看法，意见，推测/ˈθiːəri/
necessary n.必需品 adj.必要的，必须的，不可避免的/ˈnesəseri/  its necessary. 这是必要的，不可避免

forecast n.vt.预测，预报 /ˈfɔːrkæst/
broadcast v.广播，散布  n.广播节目 adj.播音的/ˈbrɔːdkæst/
premier n.总理，首相，地区总理 /prɪˈmɪr/ Hongkong HSBC is preimer of Asian. 香港HSBC是亚太区域总理
premium  n.保险费，额外费用，附加费 ；adj. 高级，优质的  /ˈpriːmiəm/  youtube premium 优质油管
advertise  v.做广告，展现，宣传，公布/ˈædvərtaɪz/
advertisement n.广告/ˌædvərˈtaɪzmənt/   commercial mean bussiness advertisement.  commercial 是商业广告

## post video

drag 拖拽/dræɡ/

clingy 紧身的，粘人的/ˈklɪŋi/
stray 迷路，流浪/streɪ/		  	feed the stray cat 喂养流浪猫
pregnant	怀孕的/ˈpreɡnənt/
caption n.说明文字，字幕,标题 v.给...加说明文字/ˈkæpʃn/		caption this short video , caption also means subtitle  给短视频加文字说明，caption也可以是字幕

strict 严格/strɪkt/
restrict n.v.限制/rɪˈstrɪkt/   this's a restrict area 这里是限制区域。

## Azerbaijin airline crash

anti	n.adj.反对/ˈænti/  
craft	n.手艺，飞行器/kræft/	anti aircraft   防空的/ˌænti ˈerkræft/
plane 	n.飞机 adj.平的	/pleɪn/
plane	n.计划，方案 /pleɪn/
exclusive adj.独家,排斥的，专有的；n.独家新闻/ɪkˈskluːsɪv/
extreme	n.极端,极限，完全相反 adj.极端的，严重的/ɪkˈstriːm/   extremely low
extract vt.提取，获得，得到 n.提取物，摘录，精，汁，节录/ˈekstrækt /  extract transform load ETL    
extra  adj.额外的，附加的，外加的 n.临时演员，群众演员  adv.额外的，特别，另外/ˈekstrə/    extra soft 超柔软
missile	n.导弹，飞弹 adj.导弹的/ˈmɪsl/  missile impact 导弹冲击
among	prep.在...中/əˈmʌŋ/		among the few survivors 在少数幸存者当中
few 	adj.有些，少数/fjuː/
take off v.起飞	Korea another plane failed when take off
land	n.土地，国家 v.着陆 /lænd/  Korea plane landing failed 韩国客机着陆失败

shield	n.盾牌，防护屏 v.保护某人某物，加防护/ʃiːld/  humman shield 人质，人体盾牌
pilot	n.飞行员 vt.试点，领航/ˈpaɪlət/  the pilot is white 飞行员是白人
fear n.v.害怕/fɪr/  fear free, i guess  恐惧自由，我猜想。
folk	n.人们/foʊks/ trust me folks, 大伙们，相信我。
dialog  n.访谈，对话/ˈdaɪəlɔːɡ/ 二者之间
conversation n.交谈，会话/ˌkɑːnvərˈseɪʃn/
terminate v.终止，结束，终点站/ˈtɜːrmɪneɪt/  this conversation is ternimated 。这个对话将终止。
marshal n.元帅，警官，警察局长，消防局长，空军元帅，司仪 v.组织，安排 /ˈmɑːrʃl/   US marshal美国警察局长。
agent n.代理人，特工，经济人/ˈeɪdʒənt/  virus criminal killed our agent 罪犯病毒杀了我们的探员

## black hawk down 黑鹰坠落
persian	波斯/ˈpɜːrʒn/
gulf	n.海湾，沟壑/ɡʌlf/        persian gulf war is a morden war 波斯海湾战争是一个现代化战争。
revenge n.v.报仇，复仇/rɪˈvendʒ/   	revenge league 复仇者联盟


## xinjiang

footage  n.镜头，影片，录像/ˈfʊtɪdʒ/   
episode 插曲，剧集/ˈepɪsoʊd/


## NBA

Buzzer Beater 绝杀ˈbʌzər ˈbiːtər/ 蜂鸣器
lead	n.v.领导,引领，指导 /liːd , led/
led 	v.起主导作用，引领，通往，引路/led/
strike	n.v.罢工，击打/straɪk/			union led strike 工会领导罢工， volleyball need strike the ball by palm 排球需要用手掌击打球。
league	n.联合会，联赛 v.结盟 /liːɡ/  revenge league 复仇者联盟
legend n.传奇，传说，非常有名的 /ˈledʒənd/
aggress  v.侵略		play aggressive  打得更有侵略性。 
aggressor n.侵略者，挑衅者 /əˈɡresər/



## Judge Mindy and accused booth

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


## How to be native english speaker

applause 掌声əˈplɔːz
accurate adj.精确的，准确的(射击等),正确无误的/ˈækjərət/
accuracy n.准确，精准/ˈækjərəsi/
accent n.口音，重音,强调 v.强调，突出，着重/ˈæksent , ækˈsent/
asset  n.资产，财产，优点，长处 /ˈæset/
clarity 清晰 ˈklærəti unclarity不明确
Eliminate your accent   消除ɪˈlɪmɪneɪt
Immersion  浸泡，沉浸ɪˈmɜːrʒn


## CoolVision  The USA city

### new york
avenue 大街/ˈævənuː/
tenant 租户，房客ˈtenənt
rent	租金，租用/rent

### shanghai
traffic 交通/ˈtræfɪk/    traffic jam 堵车	jam 果酱拥堵 /dʒæm/ 
garden	公园ˈɡɑːrdn
park	公园，园区，运动场 pɑːrk
lie		躺，撒谎laɪ
liar	撒谎者ˈlaɪər
lawyer	律师ˈlɔːjər
temple	寺庙ˈtempl/


# scenario 4  X  推特

reply n.v. 回答，答复/rɪˈplaɪ/
cast v.铸造,投,投票，扔	n.铸件，全体演员/kæst/  cast your mind back 回顾
shock n.震惊，震惊的事 v.使震惊/ʃɑːk/
reel n,卷轴，卷筒 vi.蹒跚，娘跄，感到震惊 /riːl/  if you are reeling from a shock    如果一件令人震惊的事让你感到震惊

# scenario 5 Iyrics of songs  歌曲


## viva la vida 

castle n.城堡,堡垒，车 v.把...置于城堡 ˈkæsl/  castle in the air 空中城堡 卡塞尔
pillar n.支柱，核心，基础 v.用柱子装饰，成为...的栋梁/ˈpɪlər/	Upon pillars of sand	在沙柱上



## lazy song

tone 语气，音调  /toʊn/	at the tone 在语音


# scenario 5 search frequently  常搜

## English speak fluently test 英语流利说

campus n.校园 /ˈkæmpəs/
negative adj.负面的，消极的/ˈneɡətɪv/   
passive	adj.被动的，消极的/ˈpæsɪv/
decree n.法令 v.颁布,判决/dɪˈkriː/  from high court decree 根据高等法院的法令
neglect  n.v.忽视，忽略/nɪˈɡlekt/   always neglect neglect mean 经常忽视忽视的意思
literal adj.字面意义的，缺乏想象力的，按原文/ˈlɪtərəl/    literal midnight  字面意义上的午夜
literally  adv.按字面，非常的/ˈlɪtərəli/	
chime n.钟声，铃声 v.报时，敲，鸣 /tʃaɪm/  please chime in 请参与（发表）进来

## vocabulary
rail n.轨道，栏杆 /reɪl/
attempt n.企图，尝试，试图  v.尝试，努力/əˈtempt/
tie n.领带，线，联系	v.连接，系/taɪ/
tide n.潮汐/taɪ/
tight adj.紧的，严密的 adv.紧紧的，牢固的/taɪd/
ever adv.曾经/ˈevər/
even adv.甚至，及时  adj.均匀的 v.平 n.黄昏/ˈiːvn/  even if/though 即使，纵然 加强尽管的语气
reduce v.减少，使还原，缩小，蒸发，减重，节食/rɪˈduːs/  reduce sth to sth 将什么减少为什么
reduction n.减少，降低，还原，折扣，缩减版/rɪˈdʌkʃn/  accent reduction 减少口音
attend v.出席，参加，注意，专心 /əˈtend/  if you attend a metting or other event ,you are present at it . 如果你参加一个会议或活动，你将会出席。
attention n.注意，关注 int.注意，立正 /əˈtenʃn/ listening or looking carefully , attention . 仔细听仔细看，注意。
blood n.血，血统 vt.让初试/bliːd/
bleed v.流血，出血，给放血，蕴散开 /bliːd/
stadium n.体育场，运动场/ˈsteɪdiəm/ in stadium 在体育场
arena n.竞技场，活动场所，竞争舞台，圆形运动场/əˈriːnə/ in arena 在竞技场
tip n.提示，尖端，小费，指点，内幕消息，顶端小部件 v.给小费，倾斜， /tɪp/  let the tip of your tongue 让你的舌尖

distinct adj.不同的，明显的，清晰的/dɪˈstɪŋkt/
distinguish v.区分，辨别，分清，使别于，使出众/dɪˈstɪŋɡwɪʃ/ If you can distinguish one thing from another.如果你能分清这些区别
though conj. 虽然，尽管，即使 adv.(句末补充说明)不过，可是，然后/ðoʊ/ she got a man and a son though 尽管她有老公和孩子
thought  n.想法，思考 v.思想，认为，思考/θɔːt/  think的过去分词和过去
through adv.通过，经过，完全，彻底 prep.穿过，贯穿 adj.直达，直通，联运/θruː/
throw	v.扔，丢 n.扔,抛/θroʊ/
throat  n.喉咙,嗓子 vt.嗓音/θroʊt/
pass v.通过，不知道，允许 n.通过，合格/pæs/
past adj.过去的，以往的，从前的 n.过去，昔日 prep.超过，在...之后 adv.过去，逝去，经过/pæst/
butt n.屁股，烟蒂，烟头 v.对头连接，平接 /bʌt/
button n.按钮，纽扣，扣子 v.纽扣...扣上 /ˈbʌtn/
bottom n.底部，底面 adj.底部的，最后的  v.降到最低/ˈbɑːtəm/  bottom teeth 下牙
bottle n.瓶子，一瓶，酒 vt.装入瓶中 /ˈbɑːtl/ half a bottle of whisky 半瓶威士忌
bucket n.水桶，桶，铲斗 v.挖掘铲斗，拼命划桨 /ˈbʌkɪt/ half a bucket of water 半桶水
high  adj.高的，很高的 n.最高竖屏，快感	 adv.在高处 /haɪ/ 复数：highs比较级：higher最高级：highest
highly adv.非常，大量的，高标准的 /ˈhaɪli/  highly scalability 高扩展性
height n.g高度，身高，高，高地 /haɪt/  your height and weight 你的身高和体重

internation n.国际/,ɪntɚ'næʃən/
intonation  n.语调/ˌɪntəˈneɪʃn/

browser 浏览器/ˈbraʊzər/

craft 工艺 /kræft/
crash n.崩溃，碰撞 v.心脏停止跳动/kræʃ/  airplane crash 飞机碰撞空难
credit 信用/ˈkredɪt/
channel 频道，海峡/ˈtʃænl/

demestic  国内的、家庭的 /dəˈmestɪk/

fluent 流利/ˈfluːənt/
frequently 频繁/ˈfriːkwəntli/

hit v.打，击中，达到，撞击 n.打，击中 /hɪt/  I am gonna hit the jail 我将要去坐牢
hint  n.v.提示，暗示 /hɪnt/  give me some hint 给我点提示
prompt v.提示，鼓励，提醒，促使，导致  adj.迅速的，及时的  n.提示符 /prɑːmpt/

hotspot 热点/ˈhɑːt spɑːt/


immature 幼稚ˌ/ɪməˈtʃʊr/
immediately  立即，马上/ ɪˈmiːdiətli/

mainland 大陆/ˈmeɪnlænd/

previous 前一个/ˈpriːviəs/
principal adj.主要的,最重要的/ˈprɪnsəpl/ reputation principal 荣誉校长
principle n.原则,原理，规范，信条，法则，观念  /ˈprɪnsəpl/  


priority 优先/ praɪˈɔːrəti/
private 私人/ˈpraɪvət/
province 省/ˈprɑːvɪns/
proxy 代理 /ˈprɑːksi/
pronunciation  发音 /prəˌnʌnsiˈeɪʃn/
presentation 演示，提交，出示/ˌpriːzenˈteɪʃn/		present n.目前，出席，adj.现存  vt.提出，显式/ˈpreznt /  in present 到目前

register  注册/ˈredʒɪstər/
refer v.参考，指，描述提及 /rɪˈfɜːr/ Writers often refer to a dictionary。 作家经常参考字典
reference n.参考，参照，查阅 vt.提及，附参考 adj.参考的，基准的 /ˈrefrəns/  She made no reference to her illness 她没有提及她的病

sentence 句子，判决/ˈsentəns/
stuck adj.卡主，困于 v.粘贴，黏住  cousin i am stuck 表哥，我卡住了
stuff n.东西，物品  v.塞进，使充满/stʌf/ 
staff n.工作人员，职工，管理人员  vt.任职于，雇员 adj.职员的， 雇员的/stæf/

tablet 平板 /ˈtæblət/



vocabulary 词汇 /vəˈkæbjəleri/
essay  n.散文，文章，尝试，论说问，企图  vt.企图 /ˈeseɪ , eˈseɪ/   write essay by vocabulary.  用词汇写散文

# scenario 6 IPA pronuciation 音标发音

## souds american
stretch v.伸展/stretʃ/
scratch n.划痕,刮，擦  v.挠/skrætʃ/    from scratch 从零开始，白手起家
slightly adv.稍微/ˈslaɪtli/


### neutral and tense vowels souds
neutral n.中性的，中立的，中立国，持平的，无倾向性的，不含褒贬义的  n.空挡，中立国，中立者
tense	adj.紧张的；紧的；拉紧的；绷紧的 n.时，时态 v.肌肉拉紧，紧绷/tens/
Mnemonic n.记忆术，助记符/nɪˈmɑːnɪk/  Mnemonic phrase 助记短语

### æ
audio	音频 录音/ˈɔːdiəʊ/
letter  n.字母,信 v.用字幕标明/ˈletər/
alphabet  n.字母表，全部字母/ˈælfəbet/   alphabet means all letters. 阿尔法贝意味着所有的字母。
vowels n.元音，韵母 /ˈvaʊəl/
consonants n辅音 adj.一致的，子音 /ˈkɑnsənənt/
surd  n.清辅音/sɜːrd/
sonant n.浊辅音
voiceless adj.清音的/ˈvɔɪsləs/
voice n.嗓音，噪音,发言权，浊音 vt.表示，表达/vɔɪs/

jaw	下巴，下颌 /dʒɔː/
chin 下巴/tʃɪn/
chain 链子/tʃeɪn/
distort	扭曲，失真/dɪˈstɔːrt/
backed 支持，后退，后援/bækt/  backed you  ，you 发 朱，是舌尖抵上颚原因。 would you

pleasure n.快乐，愉悦 v.使高兴/ˈpleʒər/  it's my pleasure 这是我的荣幸。
precious n.珍贵宝贵  adv.极少/ˈpreʃəs/  treasure   resource is precious
dialect	方言/ˈdaɪəlekt/
### ɛ/ 
phonetic 拼音/fənetɪk/

### ə/ /ɑ 	
instructions 指令，教导  /ɪnstrʌkʃ(ə)n/
compromise n.妥协，折中，和解 v.让步，折中，违背/ˈkɑːmprəmaɪz/
promise		承诺/ˈprɑːmɪs/
brand new  adj. 崭新的/ˌbrænd ˈnuː/
similar	相似的 /ˈsɪmələr/
familiar 熟练的，密友 /fəˈmɪliər/
family	家人/ˈfæməli/
prolong vt.延长 /prəˈlɔːŋ/


### t/ 
biology n.生物学，生理/baɪˈɑːlədʒi/  Biology is the science 生物科学
pathologist	病理学家/pəˈθɑːlədʒɪst/
flap n.拍打，飞机襟翼 v.摆动，闪 /flæp/
vanish v.消失，使不见 n.消失音/ˈvænɪʃ/
vanishing 消失的，绝迹ˈvænɪʃɪŋ/
glottal	声门，喉音/ˈɡlɑːtl/


### rhythm
syllables	音节/ˈsɪləbəlz/
pitch	投手，音高/pɪtʃ/
nouns	名词/naʊnz/
verbs	动词/vɜːrb/
adjectives	形容词/ˈædʒɪktɪvz/
adverbs	 副词/ˈædvərbz/
intonation	语调/ˌɪntəˈneɪʃn/
dictation	听写/dɪkˈteɪʃn/
dictionary	字典/ˈdɪkʃəneri/
phrasal		短语的/ˈfreɪzl/
Abbreviations	缩写/əˌbriviˈeɪʃənz/
emphasis	强调，重读n /ˈemfəsɪs/
comma	逗号/ˈkɑːmə/

exggerate v.夸张，夸大/ɪɡˈzædʒəreɪt/


## sentence phrasal  句子，短语

grammar		n.语法/ˈɡræmər/    learn sentence require we know grammar.学习句子需要我们懂语法。 ps:非重读a发音ə，重读为æ
academic	adj.学术的，学业的/ˌækəˈdemɪk/  univerity professor more like academic，company professor more like Application oriented. 大学教授更像学术型， academic word 学术名词

post script  n.附言，补充说明/poʊst skrɪpt/  缩写PS
estimate time of arrive n.预计到达时间    缩写ETA
versus n.相比，对抗 /ˈvɜːrsəs/  缩写vs
laugh out loud n.大声笑 /ˌlæf aʊt ˈlaʊd/  缩写lol

A country filled with lies
as in  就像 as in the words that

in terms of 在...方面，按照，根据，从....角度看
in your perspective  你的观点

phrasal adj.短语的/ˈfreɪzl/ phrasal verbs	动词短语
compund n.化合物，混合物 vt.混合  adj.复合的 /kəmˈpaʊnd/ compound nouns	符合名词

弱化
and /ənd , ænd/
am /əm/
are /ɑːr , er/





