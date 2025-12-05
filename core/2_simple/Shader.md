# Shader

简单功能篇

# Shader

Shader指南

孤独，你配吗？

## Shader

  * 听到Shader这个词您可能有点陌生，其实它就是着色器，其工作模式就类似一个“滤镜”
  * 如果您曾经玩过1.7.10这个版本，那您也许在某个无聊的下午按下了esc发现了某个神秘的按钮，点了之后，您发现“唉唉唉我的世界的样子怎么变了!!!”
  * 这就是对于世界的着色器，比如我们耳熟能详的Blur，也是Shader实现的，其原理是将世界加了个模糊效果。
  * 如果您想在某些场景加上一些神奇的着色器来达到奇特的效果，Shader也是一种不错的选择。

## 使用

  * 首先，我们需要先准备好Shader的文件，Shader分为两个文件夹，一个是program一个是post。
  * 我们需要将这些文件放入ArcartX的resource/shader目录中，文件夹结构大概是这样的

![Shader文件夹](https://wiki.arcartx.com/shader1.png)

  * 我并不会写Shader文件，所以从1.7.10中提取了一些资源文件作为示例。
  * 我从1.7.10中取出了一个“pencil”的着色器，打开之后是长这样的

    
    {
        "targets": [
            "swap"
        ],
        "passes": [
            {
                "name": "arcartx:outline_soft",  // 这里需要修改资源域的id为arcartx
                "intarget": "minecraft:main",
                "outtarget": "swap"
            },
            {
                "name": "arcartx:blit",  // 这里需要修改资源域的id为arcartx
                "intarget": "swap",
                "outtarget": "minecraft:main"
            }
        ]
    }
  * 随后我们注意到这个shader包含两个passes，一个是outline_soft，一个是blit。
  * 一并将它们提取出来，并将资源域的id改成arcartx,大概改完是这样，修改的部分我稍微注释了一下。

    
    {
        "blend": {
            "func": "add",
            "srcrgb": "one",
            "dstrgb": "zero"
        },
        "vertex": "sobel",
        "fragment": "arcartx:outline_soft", // 这里需要修改资源域的id为arcartx
        "attributes": [ "Position" ],
        "samplers": [
            { "name": "DiffuseSampler" }
        ],
        "uniforms": [
            { "name": "ProjMat",   "type": "matrix4x4", "count": 16, "values": [ 1.0, 0.0, 0.0, 0.0, 0.0, 1.0, 0.0, 0.0, 0.0, 0.0, 1.0, 0.0, 0.0, 0.0, 0.0, 1.0 ] },
            { "name": "InSize",    "type": "float",     "count": 2,  "values": [ 1.0, 1.0 ] },
            { "name": "OutSize",   "type": "float",     "count": 2,  "values": [ 1.0, 1.0 ] },
            { "name": "LumaRamp",  "type": "float",     "count": 1,  "values": [ 16.0 ] },
            { "name": "LumaLevel", "type": "float",     "count": 1,  "values": [ 4.0 ] }
        ]
    }
    
    {
        "blend": {
            "func": "add",
            "srcrgb": "one",
            "dstrgb": "zero"
        },
        "vertex": "blit",
        "fragment": "arcartx:blit", // 这里需要修改资源域的id为arcartx
        "attributes": [ "Position" ],
        "samplers": [
            { "name": "DiffuseSampler" }
        ],
        "uniforms": [
            { "name": "ProjMat",    "type": "matrix4x4", "count": 16, "values": [ 1.0, 0.0, 0.0, 0.0, 0.0, 1.0, 0.0, 0.0, 0.0, 0.0, 1.0, 0.0, 0.0, 0.0, 0.0, 1.0 ] },
            { "name": "OutSize",    "type": "float",     "count": 2,  "values": [ 1.0, 1.0 ] }
        ]
    }
    
  * 随后将其对用的fsh文件和vsh文件也拿出来，放到对应的文件夹中，大概是这样的。

![Shader文件夹](https://wiki.arcartx.com/shader3.png)![Shader文件夹](https://wiki.arcartx.com/shader2.png)

  * 然后我们的准备工作就做完了，进入游戏，进行包含客户端资源的重载，接下来输入指令即可打开对应的着色器。(着色器的名称根据post里面的文件名来)
  * 比如上面的示例 则是`/a shader start [玩家ID] pencil`
  * 效果如下，（使用Shimmer和API也可以操作Shader）

![Shader文件夹](https://wiki.arcartx.com/shader4.png)

  * 对于Shader，我也没有太多的了解，ArcartX也只是通过原版的接口调用并且加载了Shader，如果想要了解更多，请千万不要问我。

[Previous自定义文字图标](/docs/core/2_simple/2_font_texture)[Next音效](/docs/core/2_simple/4_sound)

