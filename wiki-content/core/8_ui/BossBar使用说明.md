# BossBar使用说明

UI篇
# BossBar使用说明
BossBar使用说明
在困厄颠沛的时候坚定不移，着就是一个真正令人钦佩的人的不凡之处。
## BossBar 使用说明
  * Bossbar的配置格式和UI差不多，但是Bossbar是属于"零散的UI"，它是通过`BossBars`控件自动创建到UI中，而不是直接在UI中创建的。
  * 如果你跳过了前面的UI教学， _请不要尝试强行理解该章节_ 。
  * 本章节涉及两个控件： BossBars 和 BossBar，具体说明请查看本篇的控件类型。


## 简单示例
  * Bossbar的配置位于ArcartX配置目录下的`boss_bar`文件夹，您可以创建多个BossBar配置。


    
    bossbar:
      match:
        - "boss" # 这里填写匹配生物名，不需要填写颜色代码
    root_control: # 填写控件片段，注意，如果你的载体BossBars控件已经使用了自适应布局控件作为父级，这里不需要再套一层
      type: canvas
      attribute:
        width: 1000
        height: 60
      children:
        name:
          type: text
          attribute:
            center: true
            x: 500
            y: 5
            fontSize: 32
            texts: self.parent.entityName  # 生物名会作为变量加入到该血条的根控件中
        bar:
          type: bossbar
          attribute:
            width: 1000
            height: 20
            y: 30
            textures: # 这里填写每层的贴图 填多少个就会分为多少层
              - ~255,0,0
              - ~0,255,0
              - ~0,0,255
    
    
  * 似乎是没什么好详细讲的，随后一切都是ArcartX _自行处理_ ，
  * 当玩家交互/攻击实体时，匹配到生物名，ArcartX会在所有正在渲染的UI中的BossBars控件中自动创建血条控件，在实体死亡后或者从世界移除将会删除。
  * 您只需要在UI中创建一个BossBars控件即可。下面提供一个UI示例，您可以把这个复制到ui目录，然后把上面的复制到boss_bars目录，生成一个名为boss的实体，然后打一下这个实体就可以看到效果


    
    ui:
      isHud: true
    controls:
      adaptive:
        type: adaptive
        attribute:
          point: ~top_center
          width: 1920
          height: 1080
        children:
          bossBars:
            type: bossBars
            attribute:
              point: ~top_center
[Previous尝试编写一个UI](/docs/core/8_ui/11_try)[Next自定义聊天栏](/docs/core/8_ui/13_chat)
