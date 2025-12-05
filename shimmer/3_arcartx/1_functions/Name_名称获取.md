# Name:名称获取

ArcartX工具集目录

# Name:名称获取

Name命名工具集

怀疑是通向真理的第一步

## `Name.getEntityName(uuid)`

  * 根据UUID获取实体名称

  * **参数** ：`uuid`: 字符串类型(实体的UUID)
  * **返回值** ：字符串类型
  * **调用示例**

    
    Name.getEntityName("550e8400-e29b-41d4-a716-446655440000")
  * **示例返回值**

    
    "Steve"
## `Name.getBlockName(x, y, z)`

  * 获取指定坐标方块的名称

  * **参数** ：
    * `x`: 整数类型(X坐标)
    * `y`: 整数类型(Y坐标)
    * `z`: 整数类型(Z坐标)
  * **返回值** ：字符串类型
  * **调用示例**

    
    Name.getBlockName(0, 64, 0)
  * **示例返回值**

    
    "Stone"
[PreviousMessage:消息展示](/docs/shimmer/3_arcartx/1_functions/8_message)[NextPacket:网络数据包](/docs/shimmer/3_arcartx/1_functions/10_packet)

