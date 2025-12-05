# Shimmer:输出

内置工具集目录

# Shimmer:输出

Shimmer工具集

眼睛可望天，理论从注视天空开始

### `Shimmer.println(text)`

  * 用于在控制台输出指定文本内容，并在输出后自动换行。

  * **参数** ：`text`：可以为字符串类型（用来输出具体的文字信息等），也可以是其他基本数据类型（会自动转换为对应的字符串形式进行输出），例如数字、布尔值等。
  * **返回值** ：无返回值（此方法主要作用是输出内容到控制台，不返回具体的数据）。
  * **调用示例**

    
    Shimmer.println("Hello, World!")
    Shimmer.println(123)
    Shimmer.println(true)
  * **示例返回值**

    
    在控制台依次输出：
    Hello, World!
    123
    true
    （每个输出内容独占一行，因为会自动换行）
### `Shimmer.print(text)`

  * 用于在控制台输出指定文本内容，但输出后不会自动换行。

  * **参数** ：`text`：和 `Shimmer.println` 中的参数要求类似，可为字符串、数字、布尔值等多种基本数据类型，其会按相应规则转换为字符串进行输出。
  * **返回值** ：无返回值（主要执行输出操作，不返回具体的数据）。
  * **调用示例**

    
    Shimmer.print("Hello")
    Shimmer.print(" World")
  * **示例返回值**

    
    在控制台输出：Hello World（两个内容紧挨着输出，不会换行，因为此方法不会自动换行）
[Previous对象](/docs/shimmer/1_base/2_flow/4_object)[NextMath:数学运算](/docs/shimmer/2_builtIn/1_functions/2_math)

