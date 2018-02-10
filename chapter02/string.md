# String

字符串由一对引号（双引号或单引号）括起来表示：

```lua
str1 = "this is string1"
str2 = 'this is string2'
```

也可以由两个方括号`[[]]`括起来表示：

```lua
html = [[
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>

</body>
</html>
]]
```

在字符串中可以使用转义字符`\`来进行转义，Lua包含以下转义字符：

```
\a bell
\b back space           -- 后退
\f form feed            -- 换页
\n newline              -- 换行
\r carriage return      -- 回车
\t horizontal tab       -- 制表
\v vertical tab
\\ backslash            -- "\"
\" double quote         -- 双引号
\' single quote         -- 单引号
\[ left square bracket  -- 左中括号
\] right square bracket -- 右中括号
```

运行时，Lua会自动在string和number之间转换，当一个string遇到算数运算符时，string会被转换成number，
反过来，当一个number遇到string连接符`..`时，会自动将number转换成string。

```lua
print("10" + 1)             --> 11
print("10 + 1")             --> 10 + 1
print("-5.3e - 10" * 2)     --> -1.06e-9
print("hello" + 1)          --> stdin:1: attempt to perform arithmetic on a string value
print(10 .. 20)             --> 1020
```

有些时候，我们需要显式对string或number进行相互转换，`tostring()`用于将number或其他类型转换成string，
`tonumber()`用于将string转换成number，当`tonumber()`遇到不能转换成number的参数时，它将返回`nil`。

```lua
print(type(tostring(1)))            --> string
print(type(tostring(nil)))          --> string
print(type(tostring(true)))         --> string

print(type(tonumber("1")))          --> number
print(type(tonumber("hello")))      --> nil
print(type(tonumber(true)))         --> nil
```
