# MythicMobs额外投掷物

MythicMobs篇

# MythicMobs额外投掷物

MythicMobs额外投掷物指南

要真正体验生命，你必须站在生命之上。

## MythicMobs额外投掷物

  * 对于某些投掷物，我们可能想要它以模型的样子显示从而完成一些特别的特效类型投掷物。
  * 此时我们便可以用ArcartX自带的模型投掷物类型。
  * 注意，由于MythicMobs没有注册投掷物的接口，这个投掷物是反射注册的，不一定所有MythicMobs版本通用。

    
    示例模型子弹:
      Conditions:
      Skills:
      - projectile{
        v=5;
        i=1;
        hR=0.5;
        vR=0.5;
        Maxduration=200;
        MaxRange=99;
        hnp=true;
        hp=false;
        hO=0;
        sE=false;
        sB=true;
        hs=false;
        hfs=0;
        syo=1.5;
        tyo=1.5;
        bullet=model;
        mid=test;
        s=1;
        onEnd=[
        ];
        onHit=[
        ];
        onBounceSkill=[
        ]} @Forward{f=15;y=0}
  * 不难发现这个和正常使用投掷物的方式差不多。
  * 只是`bullet`参数为`model`,然后有个额外的`mid`参数用来设置`模型id`,以及`s`参数来设置`模型缩放`

[PreviousMythicMobs额外配置项](/docs/core/7_mythicmobs/2_config)[Next开始](/docs/core/8_ui/1_start)

