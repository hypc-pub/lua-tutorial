# 注释

Lua中分单行注释和多行注释：

* 单行注释：以`--`开头，一直到行尾结束
* 多行注释：以`--[[`开始，以`]]`结束，中间的内容都是注释，有些时候习惯以`--]]`结束注释

例如：

```lua
-- 这是单行注释

--[[
    这里
    是
    多行注释
]]
```
