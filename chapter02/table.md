# Table

最简单构造表达式是`{}`，用来创建一个空表。也可以在表里添加一些数据，直接初始化表：

```lua
local tab1 = {}
local tab2 = {"Hello", "World", "!"}
```

Lua中的table其实是一个"关联数组"（associative arrays），数组的索引可以是数字或者是字符串。

```lua
-- table_test.lua
a = {}
a["key"] = "value"
a[10] = 20

for k, v in pairs(a) do
    print(k .. " : " .. v)
end
```

脚本执行结果是：

```bash
$ lua table_test.lua
10 : 20
key : value
```

与其他语言不同的是，lua中的table下标不是从0开始，而是从1开始：

```lua
-- table_test2.lua
a2 = {"Hello", "World", "!"}
for k, v in pairs(a2) do
    print(k .. " : " .. v)
end
```

脚本执行结果如下：

```bash
$ lua table_test2.lua
1 : Hello
2 : World
3 : !
```

table不会固定长度，有新数据添加时，table长度自动增长，没有初始的table都是`nil`：

```lua
a3 = {}
for i = 1, 10 do
    a3[i] = i
end
a3["k"] = "v"

print(a3[1])        --> 1
print(a3[10])       --> 10
print(a3[11])       --> nil
print(a3["k"])      --> v
print(a3["k2"])     --> nil
```
