### go get外网依赖


### TLS SSL SSH
> 证书验证（非对称加密） 数据传输（对称加密）SSH（应用层协议）

### CRT PEM KEY
> 公钥格式三者都行 私钥不能CRT

### base16(hex) base32 base64
> 大小分别为 2/1 8/5 4/3 base编码常用于不可见字符的编码

### csv excel
> 逗号分隔值有很多优势

### 大小端对UTF编码的影响
> UTF-8编码是以1个字节为单位进行处理的，不会受CPU大小端的影响；需要考虑下一位时就地址 + 1。
  
> UTF-16、UTF-32是以2个字节和4个字节为单位进行处理的，即1次读取2个字节或4个字节，这样一来，在存储和网络传输时就要考虑1个单位内2个字节或4个字节之间顺序的问题。

### BOM
> BOM是为UTF-16和UTF-32准备的，用户标记字节序（byte order）

### zlib gzip deflate
> deflate(RFC1951):一种压缩算法，使用LZ77和哈弗曼进行编码；

> zlib(RFC1950):一种格式，是对deflate进行了简单的封装，他也是一个实现库(delphi中有zlib,zlibex)

> gzip(RFC1952):一种格式，也是对deflate进行的封装。
  
> gzip = gzip头 + deflate编码的实际内容 + gzip尾

> zlib = zlib头 + deflate编码的实际内容 + zlib尾

### OSI
* 网络层(ip/icmp)
* 传输层(tcp/udp/quic/uds)
* 应用层(http/ws/smtp/ftp/ssh/rpc/rtmp)

### Elasticsearch
* 反向索引又叫倒排索引，是根据文章内容中的关键字建立索引。
* 搜索引擎原理就是建立反向索引。
* Elasticsearch 在 Lucene 的基础上进行封装，实现了分布式搜索引擎。
* Elasticsearch 中的索引、类型和文档的概念比较重要，类似于 MySQL 中的数据库、表和行。
* Elasticsearch 也是 Master-slave 架构，也实现了数据的分片和备份。
* Elasticsearch 一个典型应用就是 ELK 日志分析系统。

### epoll 原理

### 文件描述符
> 文件描述符（File descriptor）是计算机科学中的一个术语，是一个用于表述指向文件的引用的抽象化概念。

> 文件描述符在形式上是一个非负整数。实际上，它是一个索引值，指向内核为每一个进程所维护的该进程打开文件的记录表。当程序打开一个现有文件或者创建一个新文件时，内核向进程返回一个文件描述符。在程序设计中，一些涉及底层的程序编写往往会围绕着文件描述符展开。但是文件描述符这一概念往往只适用于UNIX、Linux这样的操作系统。

### Unix Domain Socket 与 TCP Socket
* [初步了解 Nginx unix domain socket 与 TCP socket](https://www.dazhuanlan.com/2019/11/18/5dd2b468f1db0/?__cf_chl_jschl_tk__=bc1f95a32cccf488c28fcfc5dc794799da3de1db-1589726205-0-AalNVny-tpKpuB62YYQbQIRK07vAZSW1r4XgLCo8DbLcZHT3Wxzq4s1FFoE2-hXoEiqqMsTFTGoZy5MxvzhaAOw3zP4-fsZfG8rwqrChiv3HS9s9CBsX4MLJxXYxangRhbZMvlI57nIB9qOwPwGoc0RzWM5HSbosqsXo_pp5oHG-Myd1lyMDyAGtECTf6mHgDgbS-8NHlXU5QoH2jw5P5C5JmGKkXbr-LTaKuxC-GOU_mRNa4E55Q0nvEo1BehdCGdCQ5ILq2VXNJTySziAa17BNFG-nM0aUgSsTDyMegVAj2-xNpieZTA1HLbPj1L5Zhg)
* [TCP / UDP / UDS](https://www.jianshu.com/p/2c0b8125b129?utm_campaign)

### Unix IO模型
* [IO模型及select、poll、epoll和kqueue的区别](https://www.cnblogs.com/linganxiong/p/5583415.html)
* [unix IO模型](https://wenchao.ren/2019/03/unix-IO%E6%A8%A1%E5%9E%8B/)

### ip
> ip分组/子网掩码/子网划分/MTU/NAPT/ICMP
* [IP 基础知识“全家桶”，45 张图一套带走](https://mp.weixin.qq.com/s?__biz=MzAxMTA4Njc0OQ==&mid=2651439718&idx=4&sn=31f024af2ff9da57092c83eaf42bd09b&chksm=80bb1c94b7cc95826620e3a78aca86878d8e78b2a6758675b80e38a6aeb3b28ec58bd3249469&scene=126&sessionid=1590419428&key=15bfe6e62683f6955e6696082c2a737bcc4d80f639d5b6f301b6c625071cd46fd00d96053671add1a7788bfdd995dd204a1d6893415be3821af7af5393e42961ad84b8d31762172d09f93cfde187b057&ascene=1&uin=MTExODQ5NTYyNA%3D%3D&devicetype=Windows+10+x64&version=62090070&lang=zh_CN&exportkey=A9OGkbnH5nl8iZ7k4LJPB%2Bk%3D&pass_ticket=OQ076dALfE8Wk9Cydw903qoVShisgge8VzqmrlwpTQxnpmRV2IyCqx8lZGcT1S2y)