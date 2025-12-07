## UI属性

  * UI我们先不着急渲染空间，先来了解一下UI自身的属性。
  * UI分为两种类型，一个是`Menu`即打开之后会弹出鼠标的那种UI，另一个是`HUD`即常驻于屏幕上的UI。
  * 这两种类型引用同一个配置，但是所生效的属性是不一样的，来看一下整体长啥样。
  * 注：如果不需要更改默认值可以不存在对应配置项。

    ```yaml
    ui:
      match: []
      hide: []
      transfer: "false"
      itemSize: "16"
      through: "false"
      escClose: "true"
      background: "true"
      closeDied: "true"
      show: "true"
      jei: "false"
      level: "0"
      isHud: "false"
      defaultOpen: "true"
      action:  # 这个后面讲
      packetHandler: # 这个后面讲
    ```
    
    
    
### UI属性值详解

**match**

  * **脚本支持:** 否
  * **生效对象:** Menu类型
  * **默认值:** 无
  * **说明:** 比如您想要替换掉某些原版的界面，在这里填写对应的原版界面ID即可。
  * 当然了，您可能压根不知道原版界面ID是啥，打开客户端日志查看即可，您每打开一个界面便会显示对应的ID。

![UI](https://wiki.arcartx.com/ui1.png)

**hide**

  * **脚本支持:** 否
  * **生效对象:** Menu类型、HUD类型
  * **默认值:** 无
  * **说明:** 如果您希望在某个UI存在的时候隐藏某些HUD，则可以在这里设置。
  * 对于ArcartX自定义的HUD，填对应的ID即可。
  * 对于原版HUD的名称，如下所示：
  * `vignette` `spyglass` `helmet` `frostbite` `portal` `hotbar` `crosshair`
  * `boss_event_progress` `player_health` `armor_level` `food_level` `air_level`
  * `mount_health` `jump_bar` `experience_bar` `item_name` `sleep_fade`
  * `potion_icons` `debug_text` `fps_graph` `record_overlay` `title_text` `subtitles`
  * `scoreboard` `chat_panel` `player_list`
  * `recipe_toast` `system_toast` `advancement_toast` `tutorial_toast` （这几个是右上角那个弹出消息）

**transfer**

  * **脚本支持:** 是
  * **生效对象:** Menu类型
  * **默认值:** false
  * **说明:** 鼠标、键盘事件是否传递到HUD上，如果您希望打开一个Menu类型UI的时候可以和HUD交互，那么开启这个选项即可。

**itemSize**

  * **脚本支持:** 是
  * **生效对象:** Menu类型
  * **默认值:** 16
  * **说明:** 当您点击物品槽位时候拿起来一个物品到鼠标指针上的时候渲染的物品大小。

**through**

  * **脚本支持:** 是
  * **生效对象:** Menu类型、HUD类型
  * **默认值:** false
  * **说明:** 是否开启穿透点击，比如两个组件重叠，如果为true，点击的时候会同时触发两个组件的点击事件，反之只触发显示在上层的组件的点击事件。

**escClose**

  * **脚本支持:** 是
  * **生效对象:** Menu类型
  * **默认值:** true
  * **说明:** 是否允许按下ESC关闭这个UI。

**background**

  * **脚本支持:** 是
  * **生效对象:** Menu类型
  * **默认值:** true
  * **说明:** 是否渲染背景（就是原版那个每次打开UI后面半透明黑不拉几的背景）

**closeDied**

  * **脚本支持:** 是
  * **生效对象:** Menu类型
  * **默认值:** true
  * **说明:** 如果玩家死亡，UI是否关闭，除非您替换的是原版的死亡界面，否则请保持默认值。

**show**

  * **脚本支持:** 是
  * **生效对象:** Menu类型、HUD类型
  * **默认值:** true
  * **说明:** UI是否渲染

**jei**

  * **脚本支持:** 是
  * **生效对象:** Menu类型
  * **默认值:** false
  * **说明:** UI打开的时候是否需要渲染JEI的侧边栏（如果有JEI MOD的话）

**level**

  * **脚本支持:** 是
  * **生效对象:** HUD类型
  * **默认值:** 0
  * **说明:** HUD渲染的优先级，数字越大就越先渲染，也就是数字越大显示的越靠后。

**isHud**

  * **脚本支持:** 否
  * **生效对象:** HUD类型
  * **默认值:** false
  * **说明:** 如果这个UI是作为HUD类型，那么设置为true

**defaultOpen**

  * **脚本支持:** 否
  * **生效对象:** HUD类型
  * **默认值:** true
  * **说明:** 当UI作为HUD时，是否加载后立刻打开，如果不自动打开则使用指令/a screen open 或者API进行启动/关闭

