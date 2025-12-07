# Entity:实体操作

ArcartX工具集目录

# Entity:实体操作

Entity实体工具集

有些事情必须做到，即使它们是不可能的

## `Entity.isRendering(uuid)`

  * 检查指定UUID的实体是否正在渲染

  * **参数** ：`uuid`: 字符串类型(实体UUID)
  * **返回值** ：布尔类型
  * **调用示例**

    
    Entity.isRendering("550e8400-e29b-41d4-a716-446655440000")
  * **示例返回值**

    
    true
## `Entity.getMouseEntityName()`

  * 获取鼠标指向实体的名称

  * **参数** ：无
  * **返回值** ：字符串类型
  * **调用示例**

    
    Entity.getMouseEntityName()
  * **示例返回值**

    
    "Steve"
## `Entity.getMouseEntityDistance()`

  * 获取玩家与鼠标指向实体的距离

  * **参数** ：无
  * **返回值** ：双精度浮点类型
  * **调用示例**

    
    Entity.getMouseEntityDistance()
  * **示例返回值**

    
    3.5
## `Entity.getMouseEntityUUID()`

  * 获取鼠标指向实体的UUID

  * **参数** ：无
  * **返回值** ：字符串类型
  * **调用示例**

    
    Entity.getMouseEntityUUID()
  * **示例返回值**

    
    "550e8400-e29b-41d4-a716-446655440000"
## `Entity.getMouseEntityHealth()`

  * 获取鼠标指向实体的当前生命值

  * **参数** ：无
  * **返回值** ：双精度浮点类型
  * **调用示例**

    
    Entity.getMouseEntityHealth()
  * **示例返回值**

    
    20.0
## `Entity.getMouseEntityMaxHealth()`

  * 获取鼠标指向实体的最大生命值

  * **参数** ：无
  * **返回值** ：双精度浮点类型
  * **调用示例**

    
    Entity.getMouseEntityMaxHealth()
  * **示例返回值**

    
    20.0
## `Entity.isMouseEntityAdyeshach()`

  * 检查鼠标指向的实体是否为Adyeshach实体

  * **参数** ：无
  * **返回值** ：布尔类型
  * **调用示例**

    
    Entity.isMouseEntityAdyeshach()
  * **示例返回值**

    
    true
[PreviousDisplay:窗口显示](/docs/shimmer/3_arcartx/1_functions/3_display)[NextFog:雾效控制](/docs/shimmer/3_arcartx/1_functions/5_fog)

