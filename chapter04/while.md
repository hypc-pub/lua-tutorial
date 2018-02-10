# while语句

while语句用于循环，while语法如下：

```lua
while conditions do
    whilepart
end
```

实例：

```lua
-- while_test.lua
a = 10
while a < 20 do
    print("a is: " .. a)
    a = a + 1
end
```

执行结果如下：

```bash
$ lua while_test.lua
a is: 10
a is: 11
a is: 12
a is: 13
a is: 14
a is: 15
a is: 16
a is: 17
a is: 18
a is: 19
```
