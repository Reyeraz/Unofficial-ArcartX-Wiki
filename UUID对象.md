# UUID对象

内置对象及用法

# UUID对象

UUID对象以及函数

谦逊基于力量，高傲基于无能

UUID是一段随机的ID，你也可以通过包含参数的方式进行实例化

## 实例化方式

### `UUID`无参实例化

  * **描述** ：创建一个随机的 `UUID` 实例。
  * **调用示例** ：

    
    UUID // 虽然可以没有括号 但是为了可读性建议带着括号，以免和工具集混淆
    // 或者
    UUID()
### `UUID`含参数实例化

  * **描述** ：通过指定的字符串创建一个 `UUID` 实例。如果字符串无效，将生成一个随机的UUID。
  * **参数** ：`uuidString`：文本类型，表示UUID字符串。
  * **调用示例** ：

    
    UUID('123e4567-e89b-12d3-a456-426614174000')
## 函数

### `getMostSignificantBits()`

  * 获取UUID的最高有效位

  * **参数** ：无
  * **返回值** ：长整型
  * **调用示例**

    
    UUID().getMostSignificantBits()
### `UUID.getLeastSignificantBits()`

  * 获取UUID的最低有效位

  * **参数** ：无
  * **返回值** ：长整型
  * **调用示例**

    
    UUID().getLeastSignificantBits()
### `UUID.version()`

  * 获取UUID的版本号

  * **参数** ：无
  * **返回值** ：整数类型
  * **调用示例**

    
    UUID().version()
### `UUID.variant()`

  * 获取UUID的变体号

  * **参数** ：无
  * **返回值** ：整数类型
  * **调用示例**

    
    UUID().variant()
[Previous字典类型函数](/docs/shimmer/2_builtIn/2_object/4_dict)[NextLerp-
线性插值](/docs/shimmer/2_builtIn/3_animation/1_lerp)

