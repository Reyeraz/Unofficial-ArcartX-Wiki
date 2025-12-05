# Shader:着色器控制

ArcartX工具集目录

# Shader:着色器控制

Shader着色器效果控制工具集

生命只能向后理解,但必须向前活

## `Shader.start(shaderName)`

  * 启动指定的着色器效果

  * **参数** ：
    * `shaderName`: 字符串类型(着色器名称)
  * **调用示例**

    
    Shader.start("blur")
## `Shader.update(shaderName, value)`

  * 更新指定着色器的参数值

  * **参数** ：
    * `shaderName`: 字符串类型(着色器名称)
    * `value`: 浮点数类型(着色器参数值)
  * **调用示例**

    
    Shader.update("blur", 0.5)
## `Shader.close()`

  * 关闭当前运行的着色器效果

  * **调用示例**

    
    Shader.close()
注意事项：

  * 所有着色器操作都在游戏主线程同步执行
  * 确保在使用前正确加载着色器资源
  * 过度使用复杂的着色器效果可能影响游戏性能

[PreviousScreen:屏幕控制](/docs/shimmer/3_arcartx/1_functions/14_screen)[NextSkybox:天空盒控制](/docs/shimmer/3_arcartx/1_functions/16_skybox)

