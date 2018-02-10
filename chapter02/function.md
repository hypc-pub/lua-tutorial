# Function

函数是第一类值（和其他变量相同），意味着函数可以存储在变量中，可以作为函数的参数，也可以作为函数的返回值。
这个特性给了语言很大的灵活性：一个程序可以重新定义函数增加新的功能或者为了避免运行不可靠代码创建安全运行环境而隐藏函数，
此外这特性在Lua实现面向对象中也起了重要作用。

Lua可以调用lua或者 实现的函数，Lua所有标准库都是用C实现的。标准库包括string库、table库、I/O库、OS库、算术库、debug库。

```lua
-- function_test.lua
function factorial1(n)
    if n == 0 then
        return 1
    else
        return n * factorial1(n - 1)
    end
end
print(factorial1(5))
factorial2 = factorial1
print(factorial2(5))
```

脚本执行结果是：

```bash
$ lua function_test.lua
120
120
```

function可以以匿名函数（anonymous function）的方式通过参数传递：

```lua
-- function_test2.lua
function testFun(tab,fun)
    for k ,v in pairs(tab) do
        print(fun(k,v));
    end
end

tab={key1="val1",key2="val2"};
testFun(tab,
function(key,val)
    return key.."="..val;
end
);
```

脚本执行结果如下：

```bash
$ lua function_test2.lua
key1 = val1
key2 = val2
```
