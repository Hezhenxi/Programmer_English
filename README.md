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
------------preface 序言/ˈprefəs/-------------------------------
summary	摘要，总结/ˈsʌməri/
scale	刻度，大小，规模/skeɪl/
intensive	密集的/ɪnˈtensɪv/
architecture	建筑的，架构/ˈɑːrkɪtektʃər/
safari	游猎，长途旅行/səˈfɑːri/

------------chapter 1 可靠性reliability，可拓展性scalability，可维护性maintainability-------------------------------
reliable	可靠性，可信赖/rɪˈlaɪəbl/
tolerating	容忍，容错性/ˈtɑːləreɪtɪŋ/
hardware & sofeware
faults	故障，过错/fɔːlts/
human error

scalable	可拓展性，可伸缩/ˈskeɪləbl/		resilience 能复原的，弹力/rɪˈzɪliəns/ 	  	flexible 灵活的/ˈfleksəbl/		feasiblity	可行性/ˌfizəˈbɪləti/
measure	测量，措施/ˈmeʒər/
load	负载，加载/loʊd/
performance	演出，性能，表现，执行/pərˈfɔːrməns/	perform 执行，表演/pərˈfɔːrm/
latency	延迟/'leɪtənsɪ/
percentiles	百分位数/pərˈsentaɪl/
throughput	吞吐量/ˈθruːpʊt/		throughout 始终，遍及

maintainable	可维护性，保持/meɪnˈteɪn/
operability	可操作性/ˌɑpərəˈbɪlɪti/
simplicity	简易性/sɪmˈplɪsəti/
evolvability	可进化性 evolving 进化/iˈvɑːlvɪŋ/

data-intensive	数据密集型
compute-intensive	计算密集
database	数据库
cache	缓存/kæʃ/
search indexes	搜索索引
stream processing	流处理
batch processing	批处理
data system	数据系统

(API	application programming interface 应用程序编程接口
client requests 	application code	first check if data is cached	read requests	in-memory cache		invalidate or update cache	application code
cache misses and writes		primary database	capture changes to data
asynchronous tasks	message queue	application code 	send email	outside world
search requests		full-text indexes	apply updates to search index)

reliability
scalability
maintainability

fault 故障
fault-tolerant	容错
resilient	韧性
failure	失效、失败

hardware faults 	硬件故障
MTTF,mean time to failure	平均无故障时间
AWS,amazon web services	亚马逊网络服务
prevent error	阻止预防错误
flexibility	灵活性
elasticity	弹性

systematic error	系统性错误
discrepancy	差异/dɪsˈkrepənsi/

decouple	分离，解耦/diːˈkʌpl/
sandbox		沙箱
corner case		边缘场景
telemetry	远距离测量术/təˈlemətri/
degradation		降级，恶化/ˌdeɡrəˈdeɪʃn/
load parameters		负载参数
fan-out		扇出/fæn/

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
legacy 		遗留，遗产/ˈleɡəsi/

operability		可操作性/ˌɑpərəˈbɪlɪti/		opera 歌剧/ˈɑːprə/	operation 操作/ˌɑːpəˈreɪʃn/
simplicity	简易性/sɪmˈplɪsəti/
complexity	复杂度/kəmˈpleksəti/
extensibility	可拓展性
modifiability	可修改性
plasticity		可塑性	plastics	塑料/ˈplæstɪks/

visibility	可见性/ˌvɪzəˈbɪləti/
accidental	意外的/ˌæksɪˈdentl/
abstraction	抽象/æbˈstrækʃn/
directly	直接的/dəˈrektli/
agile	敏捷的/ˈædʒl/
TDD,test-driven development
refactoring	重构/ˌriˈfæktərɪŋ/
evolvability	可演化性

functional requirements	功能需求
nonfunctional	非功能性
processing capacity	/kəˈpæsəti/处理容量	 capability	能力，才能/ˌkeɪpəˈbɪləti/

------------chapter 2 data mode & query language-------------------------------
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

nosql,not only sql
polyglot persistence 混合持久化	通晓多种语言/ˈpɑːliɡlɑːt/ 持久化，坚持不懈/pərˈsɪstəns/
impedance mismatch	阻抗不匹配	阻抗/ɪmˈpiːdns/
ORM,object-relational mapping	对象关系映射
locality	局部性，地点/loʊˈkæləti/
duplication	副本/ˌduːplɪˈkeɪʃn/
normalization	规范化/ˌnɔrməlɪˈzeɪʃən/
hierarchical model	层次模型	等级的/ˌhaɪəˈrɑːrkɪkl/  /ˈmɑːdl/
relational model	关系模型
network model		网络模型
access path 访问路径/ˈækses/	/pæθ/
schemaless	无模式
schema-on-read	读时模式
schema-on-writes	写时模式
multi-table index cluster tables	多表索引集群表
column-family	列簇
vertices	顶点/ˈvɜːtɪsiːz/  pyramid vertices	金字塔尖
edges	边缘/ˈedʒɪz/
arcs	弧，电弧/ɑːrks/
vertex	顶点/ˈvɜːrteks/
outgoing edges	出边
ingoing edges	入边
tail vertex		尾顶
head vertex		头顶


------------chapter 3 storage /ˈstɔːrɪdʒ/	& retrieve-------------------------------
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
