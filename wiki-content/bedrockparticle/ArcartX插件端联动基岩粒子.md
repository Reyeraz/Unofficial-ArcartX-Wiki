# ArcartX插件端联动基岩粒子

[二次开发]BedrockParticle
# ArcartX插件端联动基岩粒子
ArcartX插件端联动基岩粒子
愚昧无知是一切痛苦之源。
## ArcartX插件端联动
  * `ArcartX插件端` 内提供了联动`BedrockParticle MOD`的MM语句以及API，使用方式非常简单：


### MM语句
    
    bedrockParticle{id=bedrockparticle:bedrockparticle/magic.particle.json}
### API
  * 这里直接复制MM语句的实现作为示例


    
    override fun castAtEntity(skillMetadata: SkillMetadata, abstractEntity: AbstractEntity): SkillResult {
        val entity = BukkitAdapter.adapt(abstractEntity)
        bukkitPlugin.ensureMainThread {
            entity.doWithSeenBy() { player ->
                player.arcartXHandler?.spawnBedrockParticle(id, entity.location.x, entity.location.y, entity.location.z, entity.location.yaw, entity.location.pitch)
            }
        }
     
        return SkillResult.SUCCESS
    }
[Previous在ArcartX的基岩模型中生成粒子](/docs/bedrockparticle/2_model)
