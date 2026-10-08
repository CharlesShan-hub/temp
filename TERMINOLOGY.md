# Apache Pulsar in Action 翻译术语表

> 用途：保证 239 个文件分批翻译时术语一致。翻译过程中如遇新术语，追加到本表并沿用。
> 原则：专有名词、API 名、配置项、命令名一律不译；通用技术词采用中文社区通行译法。

## 一、Pulsar 核心概念

| English | 中文 | 说明 |
|---|---|---|
| Apache Pulsar | Apache Pulsar | 产品名，不译 |
| tenant | 租户 | 逻辑隔离的最高层级 |
| namespace | 命名空间 | 租户下的逻辑分组 |
| topic | 主题 | 分 persistent / non-persistent |
| persistent topic | 持久化主题 | |
| non-persistent topic | 非持久化主题 | |
| partitioned topic | 分区主题 | |
| subscription | 订阅 | |
| subscription type | 订阅类型 | |
| exclusive | 独占（订阅） | 订阅类型之一，不译作"排他的" |
| failover | 灾备（订阅） | 订阅类型之一 |
| shared | 共享（订阅） | 订阅类型之一 |
| key_shared | 按 Key 共享（订阅） | 订阅类型之一 |
| producer | 生产者 | |
| consumer | 消费者 | |
| broker | broker | 不译，避免与 message broker 混淆 |
| bookie | bookie | BookKeeper 存储节点，不译 |
| BookKeeper | BookKeeper | 不译 |
| Apache ZooKeeper | Apache ZooKeeper | 不译 |
| ledger | ledger | BookKeeper 存储单元，不译 |
| segment | 分片 | 分区内的存储分段 |
| entry | entry | ledger 内的记录单元，不译 |
| cursor | 游标 | 订阅的消费位置 |
| backlog | 积压 | 未消费消息堆积量 |
| backlog quota | 积压配额 | |
| message retention | 消息保留 | |
| message expiration | 消息过期 | |
| message acknowledgment | 消息确认 | 缩写 ack 保留原文 |
| acknowledgment | 确认 | |
| cumulative acknowledgment | 累积确认 | |
| individual acknowledgment | 单独确认 | |
| negative acknowledgment | 否定确认 | |
| dead letter topic | 死信主题 | |
| retry letter topic | 重试主题 | |
| tiered storage | 分层存储 | |
| geo-replication | 跨地域复制 | 不译作"地理复制" |
| schema registry | schema 注册表 | schema 不译 |
| schema | schema | 不译 |
| offloader | 卸载器 | 分层存储组件 |

## 二、消息语义

| English | 中文 | 说明 |
|---|---|---|
| publish-subscribe | 发布-订阅 | |
| pub-sub | 发布-订阅 | 缩写形式 |
| message queuing | 消息队列 | |
| point-to-point | 点对点 | |
| fan-out | 扇出 | |
| at-most-once | 至多一次 | |
| at-least-once | 至少一次 | |
| effectively-once | 有效一次 | Pulsar 官方用法，不译作"恰好一次" |
| exactly-once | 恰好一次 | |
| delivery semantics | 投递语义 | |
| ordering guarantee | 顺序保证 | |
| message deduplication | 消息去重 | |
| idempotent | 幂等 | |
| message key | 消息键 | |
| message payload | 消息负载 | 不译作"载荷" |
| message metadata | 消息元数据 | |
| batching | 批量发送 | |
| chunking | 消息分块 | |
| compression | 压缩 | |
| serialization | 序列化 | |
| deserialization | 反序列化 | |

## 三、计算与 IO

| English | 中文 | 说明 |
|---|---|---|
| Pulsar Functions | Pulsar Functions | 组件名，不译 |
| Pulsar IO | Pulsar IO | 组件名，不译 |
| connector | 连接器 | |
| source connector | source 连接器 | source 不译 |
| sink connector | sink 连接器 | sink 不译 |
| push source | push source | 不译 |
| function | 函数 | 指 Pulsar Function 时保留大写 |
| stateful function | 有状态函数 | |
| stateless function | 无状态函数 | |
| SerDe | SerDe | 序列化/反序列化器，不译 |
| window function | 窗口函数 | |
| stream processing | 流处理 | |
| stream-native processing | 流原生处理 | |
| micro-batching | 微批 | |
| traditional batching | 传统批处理 | |
| event time | 事件时间 | |
| processing time | 处理时间 | |
| watermark | 水位线 | |
| context | context | Pulsar Function 的 Context 对象不译 |
| user-defined function | 用户自定义函数 | |

## 四、安全

| English | 中文 | 说明 |
|---|---|---|
| authentication | 认证 | authentication=你是谁 |
| authorization | 授权 | authorization=你能做什么 |
| authentication provider | 认证提供方 | |
| TLS | TLS | 不译 |
| token | token | 不译 |
| JWT | JWT | 不译 |
| OAuth 2.0 | OAuth 2.0 | 不译 |
| Kerberos | Kerberos | 不译 |
| mutual TLS | 双向 TLS | mTLS |
| role | 角色 | |
| grant | 授权 | 动词 |
| superuser | 超级用户 | |
| proxy | proxy | 不译 |
| encryption | 加密 | |
| at-rest encryption | 静态加密 | |
| in-transit encryption | 传输加密 | |

## 五、运维与监控

| English | 中文 | 说明 |
|---|---|---|
| cluster | 集群 | |
| instance | 实例 | |
| standalone | 单机模式 | Pulsar standalone 不译 |
| deployment | 部署 | |
| deployment mode | 部署模式 | |
| Kubernetes | Kubernetes | 不译 |
| Helm | Helm | 不译 |
| operator | operator | K8s operator 不译 |
| load balancer | 负载均衡器 | |
| bundle | bundle | namespace bundle，不译 |
| unpacking | 拆分 | bundle 拆分 |
| ownership | 归属 | broker 对 bundle 的归属 |
| throughput | 吞吐量 | |
| latency | 延迟 | |
| publish latency | 发布延迟 | |
| end-to-end latency | 端到端延迟 | |
| rate in / rate out | 入速率 / 出速率 | |
| message rate | 消息速率 | |
| Prometheus | Prometheus | 不译 |
| Grafana | Grafana | 不译 |
| metrics | 指标 | |
| health check | 健康检查 | |
| rolling upgrade | 滚动升级 | |
| quota | 配额 | |
| throttling | 限流 | |
| rate limiting | 限流 | |
| autoscaling | 自动扩缩容 | |

## 六、通用技术词

| English | 中文 | 说明 |
|---|---|---|
| enterprise messaging system (EMS) | 企业消息系统 | 首次出现时可括注 EMS |
| message-oriented middleware (MOM) | 面向消息的中间件 | |
| enterprise service bus (ESB) | 企业服务总线 | |
| remote procedure call (RPC) | 远程过程调用 | |
| microservice | 微服务 | |
| distributed system | 分布式系统 | |
| scalability | 可扩展性 | |
| elasticity | 弹性 | |
| fault tolerance | 容错 | |
| high availability | 高可用 | |
| resilience | 韧性 | 不译作"弹性"，与 elasticity 区分 |
| replication | 复制 | |
| replica | 副本 | |
| quorum |  quorum | 不译 |
| consistency | 一致性 | |
| durability | 持久性 | |
| eventual consistency | 最终一致性 | |
| strong consistency | 强一致性 | |
| IIoT | 工业物联网 | Industrial Internet of Things |
| edge analytics | 边缘分析 | |
| telemetric data | 遥测数据 | |
| univariate analysis | 单变量分析 | |
| multivariate analysis | 多变量分析 | |
| feature vector | 特征向量 | |
| feature store | 特征存储 | |
| neural net | 神经网络 | |
| machine learning model | 机器学习模型 | |
| batch processing | 批处理 | |
| near-real-time | 近实时 | |
| fraud detection | 欺诈检测 | |
| connected car | 联网汽车 | |
| use case | 用例 | 不译作"使用案例" |
| out of the box | 开箱即用 | |
| trade-off | 权衡 | |
| boilerplate | 样板代码 | |

## 七、不译清单

以下一律保留英文原文，不出现在中文里：

- 所有命令名：`pulsar-admin`、`pulsar-client`、`pulsar-perf`、`pulsarctl`
- 所有配置项与参数名：`--num-partitions`、`retentionPolicies`、`brokerServiceUrl`
- 所有包名与类名：`org.apache.pulsar.client.api.Producer`、`PulsarAdmin`
- 所有方法名：`newMessage()`、`sendAsync()`、`acknowledge()`
- 所有文件名、路径、URL、镜像名
- 所有代码标识符、变量名、字符串字面量
- 语言标注：`java`、`python`、`go`、`bash`、`json`、`yaml`、`xml`
