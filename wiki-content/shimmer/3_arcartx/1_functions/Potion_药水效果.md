# Potion:药水效果

ArcartX工具集目录
# Potion:药水效果
Potion药水效果工具集
哲学家们只是用不同的方式解释世界,问题在于改变世界
## `Potion.getActivePotionEffects()`
  * 获取玩家当前所有激活的药水效果


  * **参数** ：无
  * **返回值** ：药水效果实例列表(`List<EffectValue>`)
  * **调用示例**


    
    Potion.getActivePotionEffects()
  * **示例返回值**


    
    [EffectValue]
注意事项：
  * 如果玩家不存在（例如未进入游戏），将返回空列表
  * 返回的列表包含每个药水效果的类型、持续时间和效果等级


[PreviousPlayer:玩家信息](/docs/shimmer/3_arcartx/1_functions/12_player)[NextScreen:屏幕控制](/docs/shimmer/3_arcartx/1_functions/14_screen)
