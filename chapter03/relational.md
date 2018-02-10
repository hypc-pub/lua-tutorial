# 关系运算符

> `==`(等于) `~=`(不等) `>`(大于) `<`(小于) `>=`(大于等于) `<=`(小于等于)

```lua
a = 10
b = 7
print(a == b)       --> false
print(a ~= b)       --> true
print(a > b)        --> true
print(a < b)        --> false
print(a >= b)       --> true
print(a <= b)       --> false
```

Lua比较数字时按数字大小进行，比较字符串时按字母顺序进行，但是字母顺序依赖本地环境。
