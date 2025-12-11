# Skybox:天空盒控制

ArcartX工具集目录
# Skybox:天空盒控制
Skybox天空盒纹理控制工具集
吾生也有涯,而知也无涯
## `Skybox.set(path)`
  * 设置天空盒纹理


  * **参数** ：
    * `path`: 字符串类型(纹理资源路径)
  * **调用示例**


    
    Skybox.set("textures/environment/night_sky.png")
## `Skybox.clear()`
  * 清除当前天空盒纹理，恢复默认天空盒


  * **调用示例**


    
    Skybox.clear()
注意事项：
  * 确保纹理资源路径正确且文件存在
  * 纹理文件需符合天空盒贴图格式要求
  * 清除天空盒后将恢复到游戏默认天空效果


[PreviousShader:着色器控制](/docs/shimmer/3_arcartx/1_functions/15_shader)[NextSound:音效控制](/docs/shimmer/3_arcartx/1_functions/17_sound)
