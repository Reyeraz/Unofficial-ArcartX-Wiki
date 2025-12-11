# Sound:音效控制

ArcartX工具集目录
# Sound:音效控制
Sound音效控制工具集
关于那些无法言说的事物,我们必须保持沉默
## 音效播放
### `Sound.local(identifier, x, y, z, category, distance, pitch, duration)`
  * 在指定位置播放3D音效


  * **参数** ：
    * `identifier`: 字符串类型(音效资源路径)
    * `x`: 整数类型(X坐标)
    * `y`: 整数类型(Y坐标)
    * `z`: 整数类型(Z坐标)
    * `category`: 字符串类型(音效类别)
    * `distance`: 整数类型(音效传播距离)
    * `pitch`: 双精度浮点数类型(音调)
    * `duration`: 整数类型(持续时间)
  * **调用示例**


    
    Sound.local('xxx.ogg', 100, 64, 100, 'master', 16, 1.0, 20)
### `Sound.entity(identifier, target, category, distance, pitch, duration)`
  * 为指定实体播放3D音效


  * **参数** ：
    * `identifier`: 字符串类型(音效资源路径)
    * `target`: 字符串类型(目标实体UUID，使用"self"表示玩家自身)
    * `category`: 字符串类型(音效类别)
    * `distance`: 整数类型(音效传播距离)
    * `pitch`: 双精度浮点数类型(音调)
    * `duration`: 整数类型(持续时间)
  * **调用示例**


    
    Sound.entity('xxx.ogg', 'self', 'master', 16, 1.0, 20)
### `Sound.self(identifier, pitch, duration)`
  * 为客户端玩家自身播放音效（比如一些UI提示音等不涉及空间音效的）


  * **参数** ：
  * `identifier`: 字符串类型(音效资源路径)
  * `pitch`: 双精度浮点数类型(音调)
  * `duration`: 整数类型(持续时间)
  * **调用示例**


    
    Sound.self('xxx.ogg', 1.0, 20)
### `Sound.named(dentifier, pitch, duration,name)`
  * 为客户端玩家自身播放命名音效（命名音效可以被停止）


  * **参数** ：
  * `identifier`: 字符串类型(音效资源路径)
  * `pitch`: 双精度浮点数类型(音调)
  * `duration`: 整数类型(持续时间)
  * `name`: 字符串类型(音效名称)
  * **调用示例**


    
    Sound.named('xxx.ogg', 1.0, 20,'my_sound')
### `Sound.removeNamed(name)`
  * 停止播放命名音效


  * **参数** ：
  * `name`: 字符串类型(音效名称)
  * **调用示例**


    
    Sound.removeNamed('my_sound')
注意事项：
  * 音效类别可以是：master, music, record, weather, block, hostile, neutral, player, ambient, voice
  * 确保目标实体UUID正确，否则音效将不会播放
  * 当世界未加载时音效无法播放


[PreviousSkybox:天空盒控制](/docs/shimmer/3_arcartx/1_functions/16_skybox)[NextThread:线程控制](/docs/shimmer/3_arcartx/1_functions/18_thread)
