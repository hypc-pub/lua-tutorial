# 起步

按照传统，第一个程序从**Hello World**开始：

```lua
print("Hello World!")
```

假设你将上面语句保存到文件`hello.lua`中，那么你可以在命令行执行：

```bash
lua hello.lua
```

来看一个稍微复杂的例子，下面的程序定义了一个函数来计算给定数字的阶乘，询问用户一个数字，并打印它的阶乘：

```lua
-- defines a factorial function
function fact (n)
    if n == 0 then
        return 1
    else
        return n * fact(n-1)
    end
end

print("enter a number:")
a = io.read("*number")          -- read a number
print(fact(a))
```
