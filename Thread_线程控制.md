# Thread:线程控制

ArcartX工具集目录

# Thread:线程控制

Thread线程控制工具集

存在先于本质

## `Thread.sleep(time)`

  * 使当前线程暂停执行指定的毫秒数

  * **参数** ：
    * `time`: 整数类型(暂停时间，单位为毫秒)
  * **返回值** ：整数类型(始终返回0)
  * **调用示例**

    
    Thread.sleep(1000) // 暂停1秒
注意事项：

  * 如果传入的时间小于或等于0，将自动调整为1毫秒
  * 该方法会阻塞当前线程的执行
  * 通常用于实现定时或延迟操作

[PreviousSound:音效控制](/docs/shimmer/3_arcartx/1_functions/17_sound)[NextTime:时间工具](/docs/shimmer/3_arcartx/1_functions/19_time)

