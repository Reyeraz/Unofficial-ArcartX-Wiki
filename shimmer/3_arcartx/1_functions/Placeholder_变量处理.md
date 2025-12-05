# Placeholder:变量处理

ArcartX工具集目录

# Placeholder:变量处理

Placeholder变量解析工具集

健康不是一切,但没有健康一切都是零

## `Placeholder.parse(placeholder)`

  * 解析服务器变量占位符

  * **参数** ：`placeholder`: 字符串类型(变量占位符)
  * **返回值** ：字符串类型(解析后的变量值)
  * **调用示例**

    
    Placeholder.parse("%player_name%")
  * **示例返回值**

    
    "Steve"
注意：

  * 如果变量不存在，将返回空字符串
  * 变量解析会在下一游戏刻更新

[PreviousPacket:网络数据包](/docs/shimmer/3_arcartx/1_functions/10_packet)[NextPlayer:玩家信息](/docs/shimmer/3_arcartx/1_functions/12_player)

