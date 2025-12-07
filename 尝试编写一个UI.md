## 尝试编写一个UI

  * 经过那么多个章节，终于到了实战教学环节，下面我们将创建一个替换原版生存模式背包的UI

### 1.资源文件准备

  * 首先准备好我们的资源文件

![UI](https://wiki.arcartx.com/ui2.png)

### 2.创建UI配置文件

  * 在服务端创建UI配置文件

![UI](https://wiki.arcartx.com/ui3.png)

### 3.编写UI配置文件

  * 设置UI属性，这里其余属性都用默认值就行了，只需要配置`match`，在替换匹配里加一个原版背包界面的ID

    
    ui:
      match:
        - InventoryScreen
  * 保存，重载，这个时候重载然后打开背包已经可以发现啥也没有了，因为我们还没有创建控件内容，这个时候打开背包发现是空的说明操作正确

![UI](https://wiki.arcartx.com/ui4.png)

### 4.编写基础控件

  * 然后我们开始创建控件，我们将所有组件放在自适配布局控件下，这样就省的根据窗口大小做适配了

    ```yaml
    ui:
      match:
        - InventoryScreen
    controls:
      adaptive:
        type: adaptive
        attribute:
          point: ~middle_center
          width: 1920
          height: 1080
    ```
    
    
    
  * 继续往下写，我们把背景图控件加上

    ```yaml
    ui:
      match:
        - InventoryScreen
    controls:
      adaptive:
        type: adaptive
        attribute:
          point: ~middle_center
          width: 1920
          height: 1080
        children:
          background:
            type: Texture
            attribute:
              point: ~middle_center
              width: 1270
              height: 650
              normal: ~inventory/bg.png
    ```
    
    
    
  * 然后保存重载，就可以看到背景已经渲染了

![UI](https://wiki.arcartx.com/ui5.png)

  * 再然后顺便把实体也塞进去


    # 上文省略
    ```yaml
    player:
      type: Entity
      attribute:
        x: 200
        y: 60
        scale: 5
        hideTag: true
        followMouse: true
    ```

    ![UI](https://wiki.arcartx.com/ui6.png)

  * 基本可以说是初见端倪，接下来做物品栏位，这部分我们上点强度，毕竟都有脚本了肯定不能手动创建几十个槽位
  * 这里我们利用网格布局控件来帮助我们排列槽位控件的位置，并且使用语句复制槽位并设置槽位id

    
    # 上文省略
    ```yaml
    slots:
      type: Grid
      attribute:
        x: 420
        y: 60
        spaceBetweenY: 60
        spaceBetweenX: 10
        column: 9
      action:
        create: |-
          // 创建背包栏位的槽位
          for(i in range(1,26)){
            slot = self['slot0'].copy('slot' + i)
            slot.id = 9 + i
          }
      children:
        slot0:
          type: slot
          attribute:
            width: 80
            height: 80
            normal: ~inventory/item.png
            hover: ~inventory/item_.png
            itemScale: 0.5
            id: 9
    ```
    
    
    

![UI](https://wiki.arcartx.com/ui7.png)

  * 基本上可以看到背包的雏形， 下面的快捷栏槽位也是以此类推，不过用的是横向布局控件。

![UI](https://wiki.arcartx.com/ui8.png)

  * 如此便是基本完成了一个背包UI，剩下的护甲和副手槽位我就不写了，作为示例来讲足够了
  * 来看看完整配置内容

    ```yaml
    ui:
      match:
        - InventoryScreen
    controls:
      adaptive:
        type: adaptive
        attribute:
          point: ~middle_center
          width: 1920
          height: 1080
        children:
          background:
            type: Texture
            attribute:
              point: ~middle_center
              width: 1270
              height: 650
              normal: ~inventory/bg.png
            children:
              player:
                type: Entity
                attribute:
                  x: 200
                  y: 60
                  scale: 5
                  hideTag: true
                  followMouse: true
              slots:
                type: Grid
                attribute:
                  x: 420
                  y: 60
                  spaceBetweenY: 60
                  spaceBetweenX: 10
                  column: 9
                action:
                  create: |-
                    // 创建背包栏位的槽位
                    for(i in range(1,26)){
                      slot = self['slot0'].copy('slot' + i)
                      slot.id = 9 + i
                    }
                children:
                  slot0:
                    type: slot
                    attribute:
                      width: 80
                      height: 80
                      normal: ~inventory/item.png
                      hover: ~inventory/item_.png
                      itemScale: 0.5
                      id: 9
              hot_slots:
                type: HStack
                attribute:
                  x: 100
                  y: 530
                  spaceBetween: 40
                action:
                  create: |-
                    for(i in range(1,8)){
                      slot = self['slot0'].copy('slot' + i)
                      slot.id = 36 + i
                    }
                children:
                  slot0:
                    type: slot
                    attribute:
                      width: 80
                      height: 80
                      normal: ~inventory/item.png
                      hover: ~inventory/item_.png
                      itemScale: 0.5
                      id: 36
    ```
    
    
    
  * UI方面的教学差不多到这就完事了，虽然看起来有11个章节，但是其实多上手试试并不难。
  * 多尝试几次相信您也可以写出精美的UI。

[Previous控件变量以及函数](/docs/core/8_ui/10_controls_shimmer)[NextBossBar使用说明](/docs/core/8_ui/12_bossbar)

