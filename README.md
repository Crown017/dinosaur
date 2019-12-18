# DRpc the rpc  framework based on  Netty and Zookeeper


![avatar](https://camo.githubusercontent.com/78c42a3e3d50b3dc363b3a76335f52f9f53a2b93/68747470733a2f2f67772e616c697061796f626a656374732e636f6d2f7a6f732f6e656d6f7061696e7465725f70726f642f63656365666661382d643062662d346132612d613537612d3239393835343462336438612f736f6661737461636b2d736f66612d7270632d656e5f55532f7265736f75726365732d686f6d655f312e706e67)


### 自定义协议


- magic 魔数
- heartbeat是否是心跳的包
- mType协议的类型 响应还是请求
- status状态
- length协议报文长度
- 报文体

```
+----------+-----------+--------+--------+--------------+---------------------------------------------------------------+
| magic    | heartbeat |  mType |status  | length       |content                                                        |
| 2字节    |  1 字节    | 1 字节 | 4字节   | 4字节        |                                                               |
+----------------------+--------+--------+------------------------------------------------------------------------------+
```

### 不足之处 :
- 熔断等降级措施
- 版本灰度
- 扩展性


### 未来将提供
- 基于Protobuf的序列化


