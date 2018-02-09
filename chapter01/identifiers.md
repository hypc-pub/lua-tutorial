# 标志符及关键字

## 标志符

标示符：字母或者下划线开头的字母、下划线、数字序列。

最好不要使用下划线加大写字母的标示符，因为Lua的保留字也是这样的。

Lua不允许使用特殊字符如`@`、`$`和`%`来定义标示符。Lua是一个区分大小写的编程语言。

以下列出了一些正确的标志符：

```
mohd        zara        abc         move_name   a_123
myname50    _temp       j           a23b9       retVal
```

## 关键字

Lua有以下关键字，它们不能用于定义关键字：

```
and         break       do          else        elseif
end         false       for         function    if
in          local       nil         not         or
repeat      return      then        true        until
while
```
