# UI变量以及函数

UI篇

# UI变量以及函数

UI变量以及函数

我祈祷我的高傲陪伴我的智慧。

## UI变量以及函数

  * 这里列出UI中可用的Shimmer函数以及UI对象自身的变量。

## 元素

  * 通过ui对象自身，可通过元素访问语法来获取顶层控件对象
  * 比如我们获取顶层的`background`控件，则可以用`self['background']`来访问。

## 变量

  * `transfer` 是否传递交互（MENU类型含有）
  * `itemSize` 物品大小（MENU类型含有）
  * `through` 是否穿透（MENU类型、HUD类型含有）
  * `escClose` 是否按ESC关闭（MENU类型含有）
  * `background` 背景颜色（MENU类型含有）
  * `closeDied` 是否关闭时死亡（MENU类型含有）
  * `show` 是否显示（MENU类型、HUD类型含有）
  * `jei` 是否显示JEI（MENU类型含有）
  * `actions` 触发器字典[字典类型]（MENU类型、HUD类型含有）
  * `wheelValue` 滚轮值（MENU类型、HUD类型含有）
  * `currentKeyPress` 当前按键按下（MENU类型、HUD类型含有）
  * `currentKeyReleased` 当前按键释放（MENU类型、HUD类型含有）
  * `level` 渲染优先级（HUD类型含有）

## 函数

### `childrenCount()`

  * 获取顶层组件数量

  * **参数** ：无
  * **返回值** ：数字类型
  * **调用示例**

    `self.childrenCount()`
  * **示例返回值**

    `1`
### `close()`

  * 关闭当前UI

  * **参数** ：无
  * **返回值** ：无
  * **调用示例**

    `self.close()`
  * **示例返回值**

    `无`
### `getID()`

  * 获取当前UI的ID

  * **参数** ：无
  * **返回值** ：字符串类型
  * **调用示例**

    `self.getID()`
  * **示例返回值**

    `"exampleUI"`
### `removeControlWithMeta()`

  * 匹配控件元数据删除控件
  * 关于控件meta的操作直接举例似乎不太直观，这里详细说明一下。
  * 对于控件有一个固有常量：`meta` 调用方式是`val.控件.meta`
  * 其储存一个字典型数据，你可以在触发器中去写入元数据键值对。

  * **参数** ：`key` （元数据键）和`value`（元数据值，可选，如果不包含值则只要包含键即符合匹配）
  * **返回值** ：无
  * **调用示例**

    `self.removeControlWithMeta("exampleKey", "exampleValue")`
  * **示例返回值**

    `无`
### `getControlWithMeta()`

  * 匹配控件元数据获取控件
  * 关于控件meta的操作直接举例似乎不太直观，这里详细说明一下。
  * 对于控件有一个固有常量：`meta` 调用方式是`val.控件.meta`
  * 其储存一个字典型数据，你可以在触发器中去写入元数据键值对。

  * **参数** ：`key` （元数据键）和`value`（元数据值，可选，如果不包含值则只要包含键即符合匹配）
  * **返回值** ：列表
  * **调用示例**

    `self.getControlWithMeta("exampleKey", "exampleValue")`
  * **示例返回值**

    `[控件对象A,控件对象B...]`
### `getSlotItemStack()`

  * 获取指定槽位的物品

  * **参数** ：`slotName` （槽位名称）和`slotType`（槽位类型）
  * **返回值** ：物品堆
  * **调用示例**

    `self.getSlotItemStack("exampleSlot", "exampleType")`
  * **示例返回值**

    `// 会返回一个物品对象，如果为空会返回空气`
### `getOriginalName()`

  * 仅Menu类型包含
  * 获取UI的原始名称（如果该UI是作为替换原版UI渲染的）

  * **参数** ：无
  * **返回值** ：字符串类型
  * **调用示例**

    `self.getOriginalName()`
  * **示例返回值**

    `"原版UI名称"`
### `clickSlot()`

  * 仅Menu类型包含
  * 模拟点击容器槽位，比如您替换了原版的箱子菜单，可以模拟点击对应槽位触发原版的点击槽位事件。

  * **参数** ：`id` （槽位ID）和`type`（点击类型，可选，默认为"PICKUP"）
  * **可用点击类型** ：`PICKUP`, `QUICK_MOVE`, `SWAP`, `CLONE`, `THROW`, `QUICK_CRAFT`, `PICKUP_ALL`
  * **返回值** ：无
  * **调用示例**

    
    `self.clickSlot(0, "exampleType")`
  * **示例返回值**

    `// 无返回值`

