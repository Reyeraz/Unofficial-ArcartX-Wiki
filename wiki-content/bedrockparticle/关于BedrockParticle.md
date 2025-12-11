# 关于BedrockParticle

[二次开发]BedrockParticle
# 关于BedrockParticle
关于
凡是不愿意看别人长处的人，总是一眼就看到别人不如自己之处。
## BedrockParticle 简介
  * BedrockParticle是一个独立MOD，由于懒得起名所以直接以功能名作为MOD的名称。
  * 它可以用来加载和渲染基岩版粒子，当客户端安装ArcartX时，会根据ArcartX的模型特效帧生成渲染基岩粒子。
  * 且会监听ArcartX的CustomPacket事件进行粒子生成。
  * 开源地址 <https://github.com/17Artist/BedrockParticle>
  * 二进制下载地址 <https://arcartx.com/resources/bedrockparticle.12/>


## 如何加载粒子文件
  * 本模组通过资源包进行粒子加载，我们先创建一个资源包文件夹。

![BedrockParticle](https://wiki.arcartx.com/bp1.png)
  * 然后按照正常资源包格式创建文件。

![BedrockParticle](https://wiki.arcartx.com/bp2.png)
  * 根据图中红框创建文件目录结构。

![BedrockParticle](https://wiki.arcartx.com/bp3.png)
  * 然后做个粒子或者直接下载个粒子文件,编辑器地址<https://snowstorm.app/>
  * 粒子文件放在`bedrockparticle` 文件夹下。

![BedrockParticle](https://wiki.arcartx.com/bp4.png)
  * 然后我们需要放置贴图。

![BedrockParticle](https://wiki.arcartx.com/bp5.png)
  * 随后打开粒子文件，修改贴图路径。

![BedrockParticle](https://wiki.arcartx.com/bp6.png)
  * 随后这个资源包便可以使用了，将该资源包加载到mc中，在日志中可以看到输出的粒子ID。

![BedrockParticle](https://wiki.arcartx.com/bp7.png)
  * PS: 如果你使用了ArcartX，可以使用强制资源包加载功能进行加载资源包或者加密资源包。


[PreviousShimmer开发者文档](/docs/shimmer/api/api)[Next在ArcartX的基岩模型中生成粒子](/docs/bedrockparticle/2_model)
