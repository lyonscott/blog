### 游戏玩法机制的Lua实现

``` ecs.lua
---@class world_t
---@field entities table
---@field systems table
---@field add_system fun(w:world_t,sys:system_t)
---@field add_entity fun(w:world_t,e:entity_t)
---@field rm_system fun(w:world_t,sys:system_t)
---@field rm_entity fun(w:world_t,e:entity_t)
---@field update fun(w:world_t)
---@field destroy fun(w:world_t)

---@class entity_t
---@field __dirty bool
---@field __world world_t
---@field add_component fun(e:entity_t,k,v)
---@field rm_component fun(e:entity_t,k)

---@class system_t
---@field __id number
---@field __entities table
---@field __world world_t
---@field __active bool
---@field __dirty bool
---@field init fun(sys:system_t)
---@field filter fun(e:entity_t)
---@field join fun(sys:system_t,e:entity_t)
---@field exit fun(sys:system_t,e:entity_t)
---@field refresh fun(sys:system_t)
---@field pre_update fun(sys:system_t)
---@field update fun(sys:system_t)
---@field post_update fun(sys:system_t)
---@field destroy fun(sys:system_t)
```
