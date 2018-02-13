# 函数 -- 进阶篇

Lua中的函数是带有词法定界（lexical scoping）的第一类值（first-class values）。

第一类值指：在Lua中函数和其他值（数值、字符串）一样，函数可以被存放在变量中，也可以存放在表中，可以作为函数的参数，还可以作为函数的返回值。

词法定界指：被嵌套的函数可以访问他外部函数中的变量。这一特性给Lua提供了强大的编程能力。

Lua中关于函数稍微难以理解的是函数也可以没有名字，匿名的。

既然函数是值，那么表达式也可以创建函数了，函数定义也可以写成一个赋值语句，将类型为`function`的变量赋给一个变量。

```lua
function foo(x) return 2 * x end    -- <--> foo = function(x) return 2 * x end
```

table标准库提供一个排序函数，接受一个表作为输入参数并且排序表中的元素。
这个函数必须能够对不同类型的值（字符串或者数值）按升序或者降序进行排序。
Lua不是尽可能多地提供参数来满足这些情况的需要，而是接受一个排序函数作为参数，排序函数接受两个排序元素作为输入参数，并且返回两者的大小关系。

```lua
network = {
    {name = "grauna", IP = "210.26.30.34"},
    {name = "arraial", IP = "210.26.30.23"},
    {name = "lua", IP = "210.26.23.12"},
    {name = "derain", IP = "210.26.23.20"},
}

-- 根据name排序
table.sort(network, function (a,b)
    return (a.name > b.name)
end)

-- 根据IP排序
table.sort(network, function (a,b)
    return (a.IP > b.IP)
end)
```
