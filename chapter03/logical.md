# 逻辑运算符

> `and`(与) `or`(或) `not`(非)

逻辑运算符认为`false`和`nil`是`false`，其他为真，`0`也是`true`。

`and`和`or`的运算结果不是`true`和`false`，而是和它的两个操作数相关。

`not`的结果一直返回`false`或者`true`。

```lua
print(4 and 5)          --> 5
print(nil and 13)       --> nil
print(false and 13)     --> false
print(4 or 5)           --> 4
print(false or 5)       --> 5
print(not nil)          --> true
print(not false)        --> true
print(not 0)            --> false
print(not not nil)      --> false
```
