# Chunks

Lua执行的每一段代码，例如文件或交互模式下的单行代码，都是一个块。更具体地说，块是简单的一系列语句。

```lua
a = 1
b = a*2

a = 1;
b = a*2;

a = 1 ; b = a*2

a = 1   b = a*2    -- ugly, but valid
```

一个Chunk可以是一个语句，也可以是一系列语句的组合，还可以是函数，Chunk可以很大，在Lua中几个MByte的Chunk是很常见的。

## 交互式编程

可以通过使用`lua -i`或`lua`命令开启交互式命令行：

```
Lua 5.2.4  Copyright (C) 1994-2015 Lua.org, PUC-Rio
>
```

在命令行中，输入以下命令：

```
> print("Hello World!")
```

按回车后，得到执行结果如下：

```
> print("Hello World!")
Hello World!
>
```

## 脚本式编程

我们可以将lua代码保存到`.lua`结尾的文件中，然后执行，例如，将以下内容保存到`hello.lua`文件中：

```lua
print("Hello World!")
```

使用lua执行脚本，得到结果如下：

```
> lua hello.lua
Hello World!
```

我们也可以将上面脚本修改成以下形式：

```lua
#!/usr/bin/env lua

print("Hello World!")
```

我们可以给`hello.lua`添加执行权限`chmod a+x hello.lua`，然后执行它：

```
> ./hello.lua
Hello World!
```
