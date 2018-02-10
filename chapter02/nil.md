# Nil

Lua中特殊的类型，他只有一个值：`nil`；一个全局变量没有被赋值以前默认值为`nil`；给全局变量负`nil`可以删除该变量。

```lua
print(type(a))      --> nil
print(a == nil)     --> true
```
