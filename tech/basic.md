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
* 应用层(http/ws/smtp/ftp/ssh/rpc)

### Elasticsearch
* 反向索引又叫倒排索引，是根据文章内容中的关键字建立索引。
* 搜索引擎原理就是建立反向索引。
* Elasticsearch 在 Lucene 的基础上进行封装，实现了分布式搜索引擎。
* Elasticsearch 中的索引、类型和文档的概念比较重要，类似于 MySQL 中的数据库、表和行。
* Elasticsearch 也是 Master-slave 架构，也实现了数据的分片和备份。
* Elasticsearch 一个典型应用就是 ELK 日志分析系统。

### epoll 原理

### 文件描述符

### Unix Domain Socket 与 TCP Socket
> [初步了解 Nginx unix domain socket 与 TCP socket](https://www.dazhuanlan.com/2019/11/18/5dd2b468f1db0/?__cf_chl_jschl_tk__=bc1f95a32cccf488c28fcfc5dc794799da3de1db-1589726205-0-AalNVny-tpKpuB62YYQbQIRK07vAZSW1r4XgLCo8DbLcZHT3Wxzq4s1FFoE2-hXoEiqqMsTFTGoZy5MxvzhaAOw3zP4-fsZfG8rwqrChiv3HS9s9CBsX4MLJxXYxangRhbZMvlI57nIB9qOwPwGoc0RzWM5HSbosqsXo_pp5oHG-Myd1lyMDyAGtECTf6mHgDgbS-8NHlXU5QoH2jw5P5C5JmGKkXbr-LTaKuxC-GOU_mRNa4E55Q0nvEo1BehdCGdCQ5ILq2VXNJTySziAa17BNFG-nM0aUgSsTDyMegVAj2-xNpieZTA1HLbPj1L5Zhg)

### Unix IO模型
* [IO模型及select、poll、epoll和kqueue的区别](https://www.cnblogs.com/linganxiong/p/5583415.html)
* [unix IO模型](https://wenchao.ren/2019/03/unix-IO%E6%A8%A1%E5%9E%8B/)