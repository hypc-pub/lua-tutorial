# break语句

break语句用来退出当前循环（for、repeat、while）。在循环外部不可以使用。

Lua语法要求break只能出现在block的结尾一句（也就是说：作为chunk的最后一句，或者在end之前，或者else前，或者until前）。

有时候为了调试或者其他目的需要在block的中间使用break，可以显式的使用`do..end`来实现。

```lua
a = 10
while a < 20 do
    print(a)
   a = a + 1
   if a > 15 then
      break
   end
end
--[[执行结果如下：
10
11
12
13
14
15
]]
```
