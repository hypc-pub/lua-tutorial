# 数据类型

Lua是动态类型语言，变量不需要类型定义，使用时直接赋值即可。

Lua有8个基本数据类型：`nil`、`boolean`、`number`、`string`、`function`、`userdata`、`thread`、`table`

数据类型                  |描述
------------------------|-------------------------------------------------------------------
[nil](nil.md)           |这个最简单，只有值nil属于该类，表示一个无效值（在条件表达式中相当于false）
[boolean](boolean.md)   |包含两个值：false和true。
[number](number.md)     |表示双精度类型的实浮点数
[string](string.md)     |字符串由一对双引号或单引号来表示
[function](function.md) |由 C 或 Lua 编写的函数
[userdata](userdata.md) |表示任意存储在变量中的C数据结构
[thread](thread.md)     |表示执行的独立线路，用于执行协同程序
[table](table.md)       |Lua 中的表（table）其实是一个"关联数组"（associative arrays），数组的索引可以是数字或者是字符串。在 Lua 里，table 的创建是通过"构造表达式"来完成，最简单构造表达式是{}，用来创建一个空表。

我们可以使用`type`函数测试给定变量或者值的类型：

```lua
print(type("Hello world"))      --> string
print(type(10.4*3))             --> number
print(type(print))              --> function
print(type(type))               --> function
print(type(true))               --> boolean
print(type(nil))                --> nil
print(type(type(X)))            --> string
```
