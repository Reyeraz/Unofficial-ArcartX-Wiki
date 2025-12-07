# MythicMobs额外词条

MythicMobs篇

# MythicMobs额外词条

MythicMobs额外词条指南

我爱那一种人，他们不向星空的那边寻求没落和牺牲的理由，他们只向大地献身。

## MythicMobs额外词条

ArcartX提供了一系列MythicMobs语句支持:

    
    # 设置实体模型
    # m:模型ID s:缩放大小(默认1)
    model{m=model; s=1}
    
    # 播放动画
    # n:动作名 t:过渡时长(tick) s:播放速度 k:持续时间(-1为播放一次)
    animation{n=idle;t=5;s=1;k=-1}
    
    # 隐藏骨骼
    # b:骨骼名 h:开关隐藏
    hideBone{b=head;h=true}
    
    # 设置碰撞体积
    # w:宽度 h:高度
    hitbox{w=1;h=1}
    
    # 设置动作替换
    # s:状态 a:状态指向的动作
    defaultState{s=idle;a=idle2}
    
    # 播放3D音效
    # s:音频文件路径 c:音频类型 d:范围 p:音调 k:持续时间
    sound3d{s=[location]1.ogg;c=master;d=16;p=1;k=2000}
    
    # 在目标实体位置播放锤地特效（并同步给可以看到这个实体的玩家）
    # r:半径 d:深度 i:进入时间 k:持续时间 o:退出时间 m:动画类型（0 | 1 | 2）
    hammerEffect{r=3, d=0.3, i=10, k=40, o=20, m=0}
看到这您可能想说：我用了xxx，他和你的词条内容重复了，怎么办！
没关系，ArcartX提供了自定义字段，您可以在ArcartX的根目录下找到`mythicmobs/key_words.yml`
来修改词条名称（需要重启才会生效）

[Previous模型锤击效果](/docs/core/6_model/12_hammer)[NextMythicMobs额外配置项](/docs/core/7_mythicmobs/2_config)

