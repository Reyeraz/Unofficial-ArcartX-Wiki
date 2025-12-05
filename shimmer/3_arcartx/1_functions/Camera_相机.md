# Camera:相机

ArcartX工具集目录

# Camera:相机

Camera相机工具集

我们常常只是想通过爱来掩饰嫉妒。

## `Camera.setCameraPosition(x, y, z, isFree)`

  * 设置相机位置

  * **参数** ：
  * `x`: 双精度浮点数类型(X坐标)
  * `y`: 双精度浮点数类型(Y坐标)
  * `z`: 双精度浮点数类型(Z坐标)
  * `isFree`: 布尔类型(是否自由视角)
  * **调用示例**

    
    Camera.setCameraPosition(0.0, 0.0, 0.0, true)
## `Camera.setThirdPerson(isThirdPerson)`

  * 设置第三人称视角

  * **参数** ：
  * `isThirdPerson`: 布尔类型(是否第三人称视角)
  * **调用示例**

    
    Camera.setThirdPerson(true)
## `Camera.setCameraPreset(preset)`

  * 设置相机预设

  * **参数** ：
  * `preset`: 字符串类型(预设名称)
  * **调用示例**

    
    Camera.setCameraPreset("default")
## `Camera.lockCameraMode(isLock)`

  * 锁定相机模式

  * **参数** ：
  * `isLock`: 布尔类型(是否锁定)
  * **调用示例**

    
    Camera.lockCameraMode(true)
## `Camera.setState(x, y, z, yaw, pitch, time)`

  * 设置状态相机位置
  * 状态相机是覆盖掉当前预设相机的xyz，而pitch和yaw是相对于玩家本体转向角度进行设置。
  * 该相机类型主要用于UI，比如一些UI需要应用自体相机位置变化的场景。

  * **参数** ：
  * `x`: 双精度浮点数类型(X坐标)
  * `y`: 双精度浮点数类型(Y坐标)
  * `z`: 双精度浮点数类型(Z坐标)
  * `yaw`: 浮点数类型(偏航角)
  * `pitch`: 浮点数类型(俯仰角)
  * `time`: 长整型(过渡时间)
  * **调用示例**

    
    Camera.setState(0.0, 0.0, 0.0, 0.0, 0.0, System.currentTimeMillis())
## `Camera.clearState()`

  * 清除状态相机位置

  * **参数** ：无
  * **返回值** ：无
  * **调用示例**

    
    Camera.clearState()
[PreviousMouse:鼠标](/docs/shimmer/3_arcartx/1_functions/21_mouse)[NextItemStack:物品对象](/docs/shimmer/3_arcartx/2_object/1_itemstack)

