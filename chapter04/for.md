# for语句

Lua中有两种for循环：

* 数值for循环
* 泛型for循环

## 数值for循环

语法如下：

```lua
for var=exp1,exp2,exp3 do
    statements
end
```

for将exp3作为exp1到exp2的步长，其中exp3可以忽略，默认步长是`1`。

#### 注意

##### 三个表达式只会执行一次。

```lua
for i=1,f(x) do         -- f(x)只会执行一次
    print(i)
end

for i=10,1,-1 do
    print(i)
end
```

##### 控制变量var是局部变量会被自动声明，且只在循环内部有效。如果需要保留var的值，则需要在循环中将其保存。

```lua
local found = nil
for i=1,10 do
    if i == 9 then
        found = i
        break
    end
end
print(found)            --> 9
```

##### 循环过程中不要改变控制变量的值，那样做的结果是不可预知的。如果要退出循环，使用`break`语句。

## 泛型for循环

语法如下：

```lua
for i,v in ipairs(t) do         -- 遍历数组
    statements
end

for k,v in pairs(t) do          -- 遍历table
    statements
end
```

实例：

```lua
days = {"Suanday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"}
for i,v in ipairs(days) do
    print(i, v)
end
--[[执行结果如下：
1       Suanday
2       Monday
3       Tuesday
4       Wednesday
5       Thursday
6       Friday
7       Saturday
]]

a = {a=1, b=2}
for k,v in pairs(a) do
    print(k, v)
end
--[[执行结果如下：
b       2
a       1
]]
```
