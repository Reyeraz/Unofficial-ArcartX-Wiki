# Message:消息展示

ArcartX工具集目录
# Message:消息展示
Message消息控制工具集
最美好的音乐是最美好的智慧
## `Message.chat(message)`
  * 发送聊天消息


  * **参数** ：`message`: 字符串类型
  * **返回值** ：无
  * **调用示例**


    
    Message.chat("Hello World!")
## `Message.actionBar(message)`
  * 在动作栏显示消息


  * **参数** ：`message`: 字符串类型
  * **返回值** ：无
  * **调用示例**


    
    Message.actionBar("Action message")
## `Message.title(title, subtitle, fadeIn, stay, fadeOut)`
  * 显示标题和副标题


  * **参数** ：
    * `title`: 字符串类型(主标题文本)
    * `subtitle`: 字符串类型(副标题文本)
    * `fadeIn`: 整数类型(淡入时间，单位为tick)
    * `stay`: 整数类型(停留时间，单位为tick，默认为60)
    * `fadeOut`: 整数类型(淡出时间，单位为tick)
  * **返回值** ：无
  * **调用示例**


    
    Message.title("Main Title", "Sub Title", 10, 60, 10)
[PreviousKeyboard:键盘控制](/docs/shimmer/3_arcartx/1_functions/7_keyboard)[NextName:名称获取](/docs/shimmer/3_arcartx/1_functions/9_name)
