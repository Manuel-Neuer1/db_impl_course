# 数据库系统实现 db_impl_course

数据库系统原理与实现是华东师范大学数据学院开设一门数据库系统课程。 授课人胡卉芪

课程主要内容是当下数据库内核实现中的关键技术，主要包括存储，查询，事务，高可用四个方面。


课程内容：

| Time | Content|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |Time|Content| |
|------|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|------|------|
|W1| 课程介绍| Reading: [课程简介、系统研究关注的内容、性能指标、课程要求](https://github.com/dase314/dase314.github.io/blob/main/files/w1-overview.pdf) <br/>[**Lab 1(W1):配置实验环境、编译并调试代码**](https://www.notion.so/dase314/Lab1-86faf4dfacb34f7797727b06e7867c5f?pvs=4)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |W10| 事务-异常与隔离级别 | Reading:[Serializablity（i)](http://www.mathcs.emory.edu/~cheung/Courses/554/Syllabus/7-serializability/serializability.html), [Serializablity（ii)](http://www.mathcs.emory.edu/~cheung/Courses/554/Syllabus/7-serializability/serializability1.html)，[Conflict Serializable](http://www.mathcs.emory.edu/~cheung/Courses/554/Syllabus/7-serializability/conflict-serial.html), [Recoverability-Emory](http://www.mathcs.emory.edu/~cheung/Courses/554/Syllabus/8-recv+serial/recoverable.html)， [Transaction Anomaly,Isolation Levels](https://github.com/dase314/dase314.github.io/blob/main/files/IsolationLevels.pdf), [分布式一致性与隔离级别的关系](https://github.com/dase314/dase314.github.io/blob/main/files/%E9%9A%94%E7%A6%BB%E7%BA%A7%E5%88%AB%E4%B8%8E%E4%B8%80%E8%87%B4%E6%80%A7.pdf)            |
|W2|存储-传统数据库| Reading: [KVS的接口与设计需求](https://github.com/dase314/dase314.github.io/blob/main/files/W2-KVS%E6%8E%A5%E5%8F%A3.pptx)，[B+tree](https://www.geeksforgeeks.org/introduction-of-b-tree/?ref=lbp),  [COW-B+tree](http://www.bzero.se/ldapd/btree.html)，[Page Structure，Database Buffer](https://github.com/dase314/dase314.github.io/blob/main/files/W4-BufferPool.pptx), [Cache Policy (i](https://www.geeksforgeeks.org/page-replacement-algorithms-in-operating-systems/)[,ii)](http://www.mathcs.emory.edu/~cheung/Courses/355/Syllabus/9-virtual-mem/SC-replace.html),[Implement LRU—Cache](https://github.com/dase314/dase314.github.io/blob/main/files/LRU.pdf) <br/> [**Lab 2-1:实现数据库Drop Table功能**](https://spiky-sugar-cac.notion.site/Lab2-Drop-Table-DATE-7580ea9d0cf748459d8ce327baee6384) |W11|事务-并发控制（一） | Reading: [2PL，S2PL，Basic Timestamp](https://github.com/dase314/dase314.github.io/blob/main/files/%E5%B9%B6%E5%8F%91%E6%8E%A7%E5%88%B6%E7%AE%97%E6%B3%95(%E4%B8%80).pdf) <br/>[**Lab 5-2(W10-W11):2PL算法实现**](https://confirmed-mink-e71.notion.site/Lab5-2-2PL-798e96d2bb4a4e6e9da7ce322974edca)   |
|W3|存储-Bitcast结构| Reading:  [Bitcast](https://github.com/dase314/dase314.github.io/blob/main/files/W2-Bitcast.pptx), [Log-structured store](http://blog.notdot.net/2009/12/Damn-Cool-Algorithms-Log-structured-storage) <br/> [**Lab 2-2:向数据库中增加DATE字段**](https://spiky-sugar-cac.notion.site/Lab2-Drop-Table-DATE-7580ea9d0cf748459d8ce327baee6384)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |W12| 事务-并发控制（二）|Reading:[OCC， MVCC，Snapshot Isolation](https://github.com/dase314/dase314.github.io/blob/main/files/%E5%B9%B6%E5%8F%91%E6%8E%A7%E5%88%B6%E7%AE%97%E6%B3%95(%E4%BA%8C).pdf) <br/>[**Lab 5-3(W12):OCC算法实现**](https://confirmed-mink-e71.notion.site/Lab5-3-OCC-43527334dc4d495bbe3b780fdc6f3d2d)  |
|W4|存储-LSM-tree架构存储| Reading:[Skiplist-LevelDB](https://github.com/dase314/dase314.github.io/blob/main/files/skiplist-leveldb.pdf),[LSM-tree structure & LevelDB](https://github.com/dase314/dase314.github.io/blob/main/files/W2-LSM-tree.pptx),[More about Compaction](https://github.com/dase314/dase314.github.io/blob/main/files/MoreAboutCompaction.pdf) <br/> [**Lab 3-1:在缓冲区中实现LRU淘汰算法**](https://spiky-sugar-cac.notion.site/Lab3-LRU-d0438c03f465463e86d456dd33e01706)<br/> [**Lab 3-2:实现缓存管理器**](https://spiky-sugar-cac.notion.site/Lab3-LRU-d0438c03f465463e86d456dd33e01706)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |W13| 事务-日志管理|Reading:[日志与缓冲区关系](https://github.com/dase314/dase314.github.io/blob/main/files/WAL-Log.pdf),[ARIES](https://github.com/dase314/dase314.github.io/blob/main/files/n12-Recovery.pdf)<br/> [**实现 Order By 功能**](https://lightning-cheque-89b.notion.site/Project-Order-By-d6c36b6884f841c9996c1a8c6d3e6c33)   |
|W5|存储-并发索引| Reading: [Memory Consistency Model](https://en.wikipedia.org/wiki/Linearizability)，[Concurrent Linklist（Lock coupling，Optimistic Read,Lazy Delete)](https://github.com/dase314/dase314.github.io/blob/main/files/W6-CC4OLL-new.pdf), [Concurrent Index](https://github.com/dase314/dase314.github.io/blob/main/files/w6-index.pdf)<br/>  [**Lab 5-1(W8):并发链表实现**](https://github.com/advancedalgebra/CC4OLL)                                                                                                                                                                                                                                                                                                                                                                                          |W14|高可用-数据库备份，Raft（一） |Reading:[Raft](https://github.com/dase314/dase314.github.io/blob/main/files/Raft2023.pptx)， [Raft Paper](https://web.stanford.edu/~ouster/cgi-bin/papers/raft-atc14) |
|W6|存储-其他 | Reading：[Memory Allocation](https://github.com/dase314/dase314.github.io/blob/main/files/memory_allocator.pdf)，[Snapshot](https://github.com/dase314/dase314.github.io/blob/main/files/snapshot.pdf), [Bloomfilter](https://en.wikipedia.org/wiki/Bloom_filter#:~:text=A%20Bloom%20filter%20is%20a,a%20member%20of%20a%20set.)，[Second Index](https://github.com/dase314/dase314.github.io/blob/main/files/secondaryIndex.pdf)，[Compression](https://devopedia.org/database-compression#:~:text=While%20most%20compression%20algorithms%20are,techniques%20used%20in%20database%20applications.), [Design Considerations for Database storage](https://github.com/dase314/dase314.github.io/blob/main/files/DesignConsideration.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |W15|高可用-Raft（二）|Reading: 见上 <br/> [**Lab 6(W14-W17):实现Raft算法**](https://abaft-linseed-b4c.notion.site/Raft-f082488bed0942f4a7ec2abf80d9e065?pvs=4)|
|W7|查询-执行引擎| Reading:[SQL执行过程](https://github.com/dase314/dase314.github.io/blob/main/files/query_overview.pdf)，[火山模型](https://github.com/dase314/dase314.github.io/blob/main/files/Vocano%20Model.pdf) <br/> [**Lab 4-1(W6): 实现多表查询功能**](https://lightning-cheque-89b.notion.site/890c1ff52ba84a2e80d78def3d95dbf9)<br/> [**Lab 4-2(W7): 聚合函数**](https://lightning-cheque-89b.notion.site/2ae475e71b884e3895e7009ae56de168)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |W16|高可用-分布式一致性与Basic Paxos（一）|Reading: [Distributed consensus revised-Heidi Howard](https://github.com/dase314/dase314.github.io/blob/main/files/W16-BasicPaxos.pdf)|
|W8|查询-算子实现| Reading:[Join Algorithms，Grace Join，External Sort](https://github.com/dase314/dase314.github.io/blob/main/files/db_impl_joins.pdf)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |W17|高可用-分布式一致性与Basic Paxos(二）|Reading: 见上|
|W9|查询-查询优化器| Reading: [Query Optimization](https://github.com/dase314/dase314.github.io/blob/main/files/query_queryopt.pdf)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |W18|分布式数据库主要技术扩展（MPP、分布式事务等）|Reading:|



扩展内容： 可选

| Time | Content|                                                                                                                                                                                                                                                                                                                                                                                                                                                              |Time|Content| |
|------|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|------|------|
|E1| Distributed Database Architecture | Reading: Share-noting, Share-data. Cloud Database                                       |E2| Storage| Reading: Data Partition, Consistent Hashing|     
|E3| Storage | Reading: More On LSM-tree     |E4| Transaction| Reading: Distributed Concurrency Control|  
|E5| Transaction | Reading: Atomic Commit     |E6|Consensus| Reading: There is more on consensus|  
|E7|  Transaction+Consensus | Reading: Paxos Commit     |E8| Query| Reading: Exchange, Map-Reduce, Massive Parallel Execution|  



Reading List: 

PingCap整理的数据库论文：https://github.com/pingcap/awesome-database-learning
