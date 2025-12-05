# Packet:网络数据包

ArcartX工具集目录

# Packet:网络数据包

Packet网络数据包工具集

天才与疯子只有一线之隔

## `Packet.send(type, ...data)`

  * 发送自定义网络数据包

  * **参数** ：
    * `type`: 字符串类型(数据包类型)
    * `data`: 可变参数(数据包内容)，可以是字符串或字符串列表
  * **返回值** ：无
  * **调用示例**

    
    // 发送无数据的数据包
    Packet.send("test")
     
    // 发送单个数据的数据包
    Packet.send("test", "data")
     
    // 发送多个数据的数据包
    Packet.send("test", "data1", "data2", "data3")
     
    // 发送多个数据的数据包（另一种方式）
    Packet.send("test", ["data1", "data2", "data3"])
注意：数据包的发送应遵循服务器的协议规范，确保数据格式正确。

[PreviousName:名称获取](/docs/shimmer/3_arcartx/1_functions/9_name)[NextPlaceholder:变量处理](/docs/shimmer/3_arcartx/1_functions/11_papi)

