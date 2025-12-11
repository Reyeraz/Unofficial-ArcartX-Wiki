# Keyboard:键盘控制

ArcartX工具集目录
# Keyboard:键盘控制
Keyboard键盘输入工具集
存在的理解是哲学的核心
## `Keyboard.isKeyDown(key)`
  * 检测指定按键是否被按下


  * **参数** ：`key`: 字符串类型(按键名称)
  * **返回值** ：布尔类型
  * **调用示例**


    
    Keyboard.isKeyDown("W")
  * **示例返回值**


    
    true
## `Keyboard.getKeyBindingKeyName(binding)`
  * 获取按键绑定的显示名称


  * **参数** ：`binding`: 字符串类型(按键绑定名称)
  * **返回值** ：字符串类型
  * **调用示例**


    
    Keyboard.getKeyBindingKeyName("forward")
  * **示例返回值**


    
    "W"
## `Keyboard.getKeyBindingKeyModifierName(binding)`
  * 获取按键绑定的修饰键名称 注意 Fabric没这玩意


  * **参数** ：`binding`: 字符串类型(按键绑定名称)
  * **返回值** ：字符串类型
  * **调用示例**


    
    Keyboard.getKeyBindingKeyModifierName("screenshot")
  * **示例返回值**


    
    "CONTROL"
## `Keyboard.setKeyBindingKeyName(binding, modifier, keyCode)`
  * 设置按键绑定 注意 Fabric没modifier 填了是无效的 但是要随便填个字符串参数进去


  * **参数** ：
    * `binding`: 字符串类型(按键绑定名称)
    * `modifier`: 字符串类型(修饰键名称)
    * `keyCode`: 整数类型(按键代码)
  * **返回值** ：无
  * **调用示例**


    
    Keyboard.setKeyBindingKeyName("forward", "NONE", 87)
## `Keyboard.keyPress(key, pressed)`
  * 模拟按键按下或释放


  * **参数** ：
    * `key`: 字符串类型(按键名称)
    * `pressed`: 布尔类型(是否按下)
  * **返回值** ：无
  * **调用示例**


    
    Keyboard.keyPress("W", true)
[PreviousGame:游戏控制](/docs/shimmer/3_arcartx/1_functions/6_game)[NextMessage:消息展示](/docs/shimmer/3_arcartx/1_functions/8_message)
