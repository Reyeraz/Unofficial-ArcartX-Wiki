# ItemStack:物品对象

ArcartX对象及用法
# ItemStack:物品对象
ItemStack:物品对象
在自己身上，克服这个时代。
## `getType()`
  * 获取物品类型


  * **参数** ：无
  * **返回值** ：字符串类型
  * **调用示例**


    
    物品对象.getType()
## `getCount()`
  * 获取物品数量


  * **参数** ：无
  * **返回值** ：整数类型
  * **调用示例**


    
    物品对象.getCount()
## `getName()`
  * 获取物品名称


  * **参数** ：无
  * **返回值** ：字符串类型
  * **调用示例**


    
    物品对象.getName()
## `getLore()`
  * 获取物品描述


  * **参数** ：无
  * **返回值** ：字符串列表类型
  * **调用示例**


    
    物品对象.getLore()
## `getNBT(path)`
  * 获取物品NBT数据（多层级属于用`.`分割）


  * **参数** ：`path`（NBT路径）
  * **返回值** ：字符串类型
  * **调用示例**


    
    物品对象.getNBT("model")
## `getNBTList(path)`
  * 获取物品NBT数据（多层级属于用`.`分割）


  * **参数** ：`path`（NBT路径）
  * **返回值** ：列表类型
  * **调用示例**


    
    物品对象.getNBTList("xxx")
## `getNBTMap(path)`
  * 获取物品NBT数据（多层级属于用`.`分割）


  * **参数** ：`path`（NBT路径）
  * **返回值** ：字典类型
  * **调用示例**


    
    物品对象.getNBTMap("xxx")
[PreviousTip:工具提示](/docs/shimmer/3_arcartx/1_functions/23_tip)[NextPotionEffect:药水效果](/docs/shimmer/3_arcartx/2_object/2_potion)
