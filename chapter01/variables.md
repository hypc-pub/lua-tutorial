# 变量

变量在使用前，必须在代码中进行声明，即创建该变量。

编译程序执行代码之前编译器需要知道如何给语句变量开辟存储区，用于存储变量的值。

Lua变量有三种类型：全局变量、局部变量、表中的域。

Lua中的变量全是全局变量，那怕是语句块或是函数里，除非用`local`显式声明为局部变量。

局部变量的作用域为从声明位置开始到所在语句块结束。

变量的默认值均为`nil`。

```lua
-- test.lua
a = 5               -- global variables
local b = 5         -- local variables

function joke()
    c = 5           -- global variables
    local d = 6     -- local variables
end

joke()
print(c, d)         --> 5 nil

do
    local a = 6     -- local variables
    b = 6           -- global variables
    print(a, b);    --> 6 6
end

print(a, b)         --> 5 6
```

## 赋值语句

赋值是改变一个变量的值和改变表域的最基本的方法。

```lua
a = "hello"
t.n = t.n + 1
```

也可以对多个变量同时赋值：

```lua
a, b = 1, 2     -- 等价于：a = 1; b = 2
print(a, b)     --> 1 2
a, b = b, a     -- 交换a和b的值
print(1, b)     --> 2 1
```

当变量个数和值的个数不一致时，lua执行以下两条规则：

* 变量个数 > 值的个数：按变量个数补足`nil`
* 变量个数 < 值的个数：忽略多余的值
