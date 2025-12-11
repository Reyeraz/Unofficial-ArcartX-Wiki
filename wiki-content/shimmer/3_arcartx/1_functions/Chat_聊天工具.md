# Chat:聊天工具

ArcartX工具集目录
# Chat:聊天工具
Chat工具集
我只知道我一无所知
## `Chat.open([message])`
  * 打开聊天界面，可选择是否预填充消息


  * **参数** ：`message`: 字符串类型（可选）
  * **返回值** ：无
  * **调用示例**


    
    Chat.open("Hello world!")
## `Chat.setMessage(message)`
  * 设置聊天框的内容


  * **参数** ：`message`: 字符串类型
  * **返回值** ：无
  * **调用示例**


    
    Chat.setMessage("Hello Minecraft!")
## `Chat.addMessage(message)`
  * 在当前聊天框内容后追加文本


  * **参数** ：`message`: 字符串类型
  * **返回值** ：无
  * **调用示例**


    
    Chat.addMessage(" World!")
## `Chat.getMessage()`
  * 获取当前聊天框的内容


  * **参数** ：无
  * **返回值** ：字符串类型
  * **调用示例**


    
    Chat.getMessage()
  * **示例返回值**


    
    "Hello Minecraft!"
## `Chat.say(message)`
  * 发送一条聊天消息


  * **参数** ：`message`: 字符串类型
  * **返回值** ：无
  * **调用示例**


    
    Chat.say("Hello everyone!")
## `Chat.getEventMessage()`
  * 获取当前事件的聊天消息


  * **参数** ：无
  * **返回值** ：字符串类型
  * **调用示例**


    
    Chat.getEventMessage()
  * **示例返回值**


    
    "Player joined the game"
## `Chat.getLastMessage()`
  * 获取最后一条聊天消息


  * **参数** ：无
  * **返回值** ：字符串类型
  * **调用示例**


    
    Chat.getLastMessage()
  * **示例返回值**


    
    "Last chat message"
[PreviousCast:类型转换](/docs/shimmer/3_arcartx/1_functions/1_cast)[NextDisplay:窗口显示](/docs/shimmer/3_arcartx/1_functions/3_display)
