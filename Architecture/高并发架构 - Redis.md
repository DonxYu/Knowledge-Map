# 高并发架构 - Redis

- 支撑10万Qps的架构
Redis replication -> Redis主从架构 -> 读写分离架构 -> 支持水平扩展的读高并发架构


- 复制原理
异步复制
master生成一份rdb快照 并且将新数据备份到内存  rdb快照同步给slave slave持久化到磁盘，同步完之后发送内存中数据给slave

断点续传  backlog

- 压测
redis自带benchmark工具