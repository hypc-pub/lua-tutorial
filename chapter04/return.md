# return语句

return用来从函数返回结果，当一个函数自然结束结尾会有一个默认的return。

Lua语法要求return只能出现在block的结尾一句（也就是说：作为chunk的最后一句，或者在end之前，或者else前，或者until前）。

有时候为了调试或者其他目的需要在block的中间使用return，可以显式的使用`do..end`来实现：

```lua
function foo ()
    do return end
    statements
end
```
