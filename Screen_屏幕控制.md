# Screen:屏幕控制

ArcartX工具集目录

# Screen:屏幕控制

Screen屏幕控制工具集

历史总是重复两次,第一次是悲剧,第二次是闹剧

## 屏幕尺寸

### `Screen.getWidth()` / `Screen.getHeight()`

  * 获取游戏窗口的宽度/高度

  * **参数** ：无
  * **返回值** ：双精度浮点数类型
  * **调用示例**

    
    Screen.getWidth()  // 返回窗口宽度
    Screen.getHeight() // 返回窗口高度
## 菜单控制

### `Screen.open(name)`

  * 打开指定ID的UI

  * **参数** ：
    * `name`: 字符串类型(ID)
  * **调用示例**

    
    Screen.open("settings")  // 使用默认命名空间
### `Screen.close(name)`

  * 关闭当前或指定的菜单界面

  * **参数** ：
    * `name`: 字符串类型(可选，ID)
  * **调用示例**

    
    Screen.close()  // 关闭当前界面
    Screen.close("settings")  // 关闭指定UI
[PreviousPotion:药水效果](/docs/shimmer/3_arcartx/1_functions/13_potion)[NextShader:着色器控制](/docs/shimmer/3_arcartx/1_functions/15_shader)

