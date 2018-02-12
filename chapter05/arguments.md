# 可变参数

Lua函数可以接受可变数目的参数，和C语言类似在函数参数列表中使用三点（`...`）表示函数有可变的参数。

可以通过`args = {...}`的方式将参数放在一个叫`args`的表中，另外可以通过`#args`获取参数个数。

```lua
function average(...)
    result = 0
    local args={...}
    for i,v in ipairs(args) do
        result = result + v
    end
    print("总共传入: " .. #args .. "个数")
    return result/#args
end

print("平均值为: " .. average(10,5,3,4,5,6))
--[[执行结果为：
总共传入: 6个数
平均值为: 5.5
]]
```

有时候我们需要几个固定参数和一些可变参数：

```lua
function select(n, ...)
    local args = {...}
    return args[n]
end

print(select(1, 1, 2, 3, 4))        --> 1
print(select(2, 1, 2, 3, 4))        --> 2
print(select(10, 1, 2, 3, 4))       --> nil
```
