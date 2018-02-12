# 函数

函数有两种用途：

1. 完成指定的任务，这种情况下函数作为调用语句使用
2. 计算并返回值，这种情况下函数作为赋值语句的表达式使用

语法如下：

```lua
optional_function_scope function function_name(argument1, argument2, argument3..., argumentn)
    function_body
    return result_params_comma_separated
end
```

* **optional_function_scope**: 该参数是可选的制定函数是全局函数还是局部函数，
    未设置该参数默认为全局函数，如果你需要设置函数为局部函数需要使用关键字`local`。
* **function_name**: 指定函数名称。
* **argument1, argument2, argument3..., argumentn**: 函数参数，多个参数以逗号隔开，函数也可以不带参数。
* **function_body**: 函数体，函数中需要执行的代码语句块。
* **result_params_comma_separated**: 函数返回值，Lua语言函数可以返回多个值，每个值以逗号隔开。

函数调用时，需要使用`()`表明是函数调用。
但是有一个特例，当函数只有一个参数，并且这个参数是字符串或表构造时，`()`是可选的。

```lua
print "Hello World"     -- <--> print("Hello World")
dofile 'a.lua'          -- <--> dofile('a.lua')
f{x=10, y=20}           -- <--> f({x=10, y=20})
type{}                  -- <--> type({})
```

Lua也提供了面向对象方式调用函数的方法，`o:f(x)`与`o.f(o, x)`是等价的。

Lua使用的函数可以是Lua编写也可以是其他语言编写，对于Lua程序员来说用什么语言实现的函数使用起来都一样。

Lua函数实参和形参的匹配与赋值语句类似，多余部分被忽略，缺少部分用nil补足。

```lua
function f(a, b) return a or b end

f(3)                -- a=3, b=nil
f(3, 4)             -- a=3, b=4
f(3, 4, 5)          -- a=3, b=4 (5被忽略)
```
