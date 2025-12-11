# Player:玩家信息

ArcartX工具集目录
# Player:玩家信息
Player玩家信息工具集
人生来是自由的,却无往不在枷锁之中
## 基本信息
### `Player.getName()`
  * 获取玩家名称


  * **参数** ：无
  * **返回值** ：字符串类型


    
    Player.getName() // 返回 "Steve"
### `Player.getUUID()`
  * 获取玩家UUID


  * **参数** ：无
  * **返回值** ：字符串类型


    
    Player.getUUID() // 返回 "550e8400-e29b-41d4-a716-446655440000"
### `Player.getOnlinePlayersDict()`
  * 获取在线玩家列表


  * **参数** ：无
  * **返回值** ：字典类型(Key为玩家名，Value为UUID)


    
    Player.getOnlinePlayersDict() // 返回 {"Steve": "uuid1", "Alex": "uuid2"}
## 状态信息
### `Player.getHealth()` / `Player.getMaxHealth()`
  * 获取玩家当前/最大生命值


  * **参数** ：无
  * **返回值** ：浮点数类型


    
    Player.getHealth() // 返回 20.0
    Player.getMaxHealth() // 返回 20.0
### `Player.getLevel()` / `Player.getExp()`
  * 获取玩家等级/经验值


  * **参数** ：无
  * **返回值** ：整数/浮点数类型


    
    Player.getLevel() // 返回 30
    Player.getExp() // 返回 0.75
## 位置信息
### `Player.getPosX()` / `Player.getPosY()` / `Player.getPosZ()`
  * 获取玩家X/Y/Z坐标


  * **参数** ：无
  * **返回值** ：双精度浮点数类型


    
    Player.getPosX() // 返回 100.5
    Player.getPosY() // 返回 64.0
    Player.getPosZ() // 返回 -200.5
### `Player.getYaw()` / `Player.getPitch()`
  * 获取玩家偏航角/俯仰角


  * **参数** ：无
  * **返回值** ：浮点数类型


    
    Player.getYaw() // 返回 180.0
    Player.getPitch() // 返回 45.0
## 状态检测
### `Player.isFlying()` / `Player.isInWater()` / `Player.isOnGround()`
  * 检测玩家飞行/在水中/在地面状态


  * **参数** ：无
  * **返回值** ：布尔值类型


    
    Player.isFlying() // 返回 false
    Player.isInWater() // 返回 false
    Player.isOnGround() // 返回 true
## 其他属性
### `Player.getFood()` / `Player.getAir()` / `Player.getArmor()`
  * 获取玩家饥饿值/氧气值/护甲值


  * **参数** ：无
  * **返回值** ：整数类型


    
    Player.getFood() // 返回 20
    Player.getAir() // 返回 300
    Player.getArmor() // 返回 20
### `Player.getCurrentItem()`
  * 获取当前选中物品栏位置


  * **参数** ：无
  * **返回值** ：整数类型(0-8)


    
    Player.getCurrentItem() // 返回 0
### `Player.isFallFlying()`
  * 检测玩家是否正在滑翔


  * **参数** ：无
  * **返回值** ：布尔类型


    
    Player.isFallFlying() // 返回 true | false
### `Player.respawn()`
  * 重生玩家


  * **参数** ：无
  * **返回值** ：无


    
    Player.respawn()
### `Player.getMainHandItem()`
  * 获取玩家主手物品


  * **参数** ：无
  * **返回值** ：ItemStack对象


    
    Player.getMainHandItem() // 返回 ItemStack对象
[PreviousPlaceholder:变量处理](/docs/shimmer/3_arcartx/1_functions/11_papi)[NextPotion:药水效果](/docs/shimmer/3_arcartx/1_functions/13_potion)
