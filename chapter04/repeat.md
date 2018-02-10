# repeat语句

与while和for不同的是，repeat语句的条件判断表达式在后面，这就意味着repeat语句至少要执行一次。

repeat语法如下：

```lua
repeat
    repeatpart
until conditions
```

实例：

```lua
-- repeat_test.lua
a = 10
repeat
    print("a is: " .. a)
    a = a + 1
until a > 20
```

执行结果如下：

```bash
$ lua repeat_test.lua
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
a is: 20
```
