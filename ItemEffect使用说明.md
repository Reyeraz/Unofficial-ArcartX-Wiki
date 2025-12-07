# ItemEffect使用说明

UI篇

# ItemEffect使用说明

ItemEffect使用说明

对于人类来说，生存本身就是旅行。

## ItemEffect使用说明

  * ItemEffect是作用于UI的Slot中的物品效果，用于渲染物品的一些额外信息。
  * 比如你想在ui的slot中通过读取nbt或者某个lore来渲染物品强化等级，
  * 比如你想通过某个说明来显示一个物品品质背景...
  * 以上需求我们便可以通过ItemEffect来实现，不过注意，这个功能只有在ArcartX的UI中才有效果。

## 配置说明

  * ItemEffect的配置位于ArcartX根目录下的`item_effect`目录中，您可以创建多个ItemEffect配置。
  * 值得注意的是，ItemEffect的组件和UI是没有任何关联的，而是专属于ItemEffect的组件，且只有两种类型：texture和text。
  * 虽然ItemEffect的控件支持Shimmer，然而他们都是仅用于语句执行而 **无对象上下文** ，也就是说这个控件无法访问UI的上下文数据。也没有self相关的定义。
  * 它可访问`val.itemStack`这个变量，指代slot中的物品（这个物品不会是空气或者null，因为没有物品的时候ItemEffect压根不会渲染）
  * 配置格式说明

    
    # 显示在物品之前
    before:
      texture:
        type: text # 可用类型 texture | text
        attribute:
          xr: 0
          yr: 0
          text: ~啊啊啊啊啊啊
          mode: 0 # 0: 左对齐, 1: 居中, 2: 右对齐
          shadow: true
          visible: true
    # 显示在物品之后
    after:
      texture:
        type: texture # 可用类型 texture | text
        attribute:
          xr: 0
          yr: 0
          wr: 1
          hr: 1
          visible: true
          texture: ~255,255,255
## 组件属性说明

  * Texture组件
    * `xr`：X位置比例，（实际渲染时会乘以slot的渲染宽度）
    * `yr`：Y位置比例，（实际渲染时会乘以slot的渲染高度）
    * `wr`：宽度比例，（实际渲染时会乘以slot的渲染宽度）
    * `hr`：高度比例，（实际渲染时会乘以slot的渲染高度）
    * `visible`：是否可见
    * `texture`：纹理路径，支持rgba颜色值和图片路径
  * Text组件
    * `xr`：X位置比例，（实际渲染时会乘以slot的渲染宽度）
    * `yr`：Y位置比例，（实际渲染时会乘以slot的渲染高度）
    * `text`：文本内容
    * `mode`：文本对齐方式，0: 左对齐, 1: 居中, 2: 右对齐
    * `shadow`：是否显示阴影
    * `visible`：是否可见
    * 值得注意的是，text的字号是根据Slot的设定来的

[PreviousBossBar使用说明](/docs/core/8_ui/12_bossbar)[Next自定义聊天栏](/docs/core/8_ui/14_chat)

