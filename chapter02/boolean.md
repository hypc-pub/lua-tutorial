# Boolean

boolean类型只有两个值：`true`和`false`。

```lua
print(type(true))       --> boolean
print(type(false))      --> boolean
print(type(nil))        --> nil
```

在做条件判断时，Lua把`false`和`nil`都看成是`false`：

```lua
-- test.lua
if false or nil then
    print('at least one of them is false')
else
    print('both of them are false')
end
```

执行结果如下：

```bash
> lua test.lua
both of them are false
```
