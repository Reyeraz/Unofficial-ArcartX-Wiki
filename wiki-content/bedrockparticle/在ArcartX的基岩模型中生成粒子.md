# 在ArcartX的基岩模型中生成粒子

[二次开发]BedrockParticle
# 在ArcartX的基岩模型中生成粒子
在ArcartX的基岩模型中生成粒子
人类唯有生长在爱中，才得以创造出新的事物。
## 在ArcartX的基岩模型中生成粒子
  * 如果您同时安装了`BedrockParticle`和`ArcartX`,`BedrockParticle`MOD会注册监听`ArcartX`的模型粒子帧。
  * 使用方式如图所示

![BedrockParticle](https://wiki.arcartx.com/bp8.png)
  * 文字版


    
    bedrock:particle{id=bedrockparticle:bedrockparticle/magic.particle.json;mode=look}
  * 参数说明
    * `id`: 粒子ID（log输出的ID）
    * `mode`: 旋转模式（可空 默认为`look`)
      * `look`: 实体头朝向
      * `body`: 实体身体朝向
      * `world`: 根据世界坐标旋转
    * `yaw`: 偏航角附加（可空 默认为0）
    * `pitch`: 俯仰角附加（可空 默认为0）


[Previous关于BedrockParticle](/docs/bedrockparticle/1_start)[NextArcartX插件端联动基岩粒子](/docs/bedrockparticle/3_arcartx)
