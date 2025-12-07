# Time:时间工具

ArcartX工具集目录

# Time:时间工具

Time时间处理工具集

人是自由的,但又注定要自由

## `Time.currentTime()`

  * 获取当前时间戳（毫秒）

  * **参数** ：无
  * **返回值** ：长整型数字(毫秒时间戳)
  * **调用示例**

    
    Time.currentTime()
  * **示例返回值**

    
    1707051600000  // 实际返回值会随当前时间变化
## `Time.currentTimeFormat([timestamp], [format])`

  * 格式化时间戳为可读字符串

  * **参数** ：
    * `timestamp`: 长整型数字(可选，毫秒时间戳)
    * `format`: 字符串类型(可选，时间格式模板)
  * **返回值** ：字符串类型(格式化后的时间字符串)
  * **调用示例**

    
    // 不带参数，使用当前时间和默认格式
    Time.currentTimeFormat()
     
    // 指定时间戳
    Time.currentTimeFormat(1707051600000)
     
    // 指定时间戳和格式
    Time.currentTimeFormat(1707051600000, "MM-dd HH:mm")
  * **示例返回值**

    
    "2024-02-04 20:00:00"  // 默认格式
    "02-04 20:00"          // 自定义格式
注意事项：

  * 默认时间格式为："yyyy-MM-dd HH:mm:ss"
  * 不传参数时使用当前系统时间
  * 时间格式支持Java的SimpleDateFormat语法

[PreviousThread:线程控制](/docs/shimmer/3_arcartx/1_functions/18_thread)[NextWeb:网页控制](/docs/shimmer/3_arcartx/1_functions/20_web)

