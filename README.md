# Lua Tutorial

[Lua][] 是一种轻量小巧的脚本语言，用标准C语言编写并以源代码形式开放， 其设计目的是为了嵌入应用程序中，从而为应用程序提供灵活的扩展和定制功能。

[Lua][] 是巴西里约热内卢天主教大学（Pontifical Catholic University of Rio de Janeiro）里的一个研究小组，由Roberto Ierusalimschy、Waldemar Celes 和 Luiz Henrique de Figueiredo所组成并于1993年开发。

## 设计目的

其设计目的是为了嵌入应用程序中，从而为应用程序提供灵活的扩展和定制功能。

## Lua 特性

* **轻量级**: 它用标准C语言编写并以源代码形式开放，编译后仅仅一百余K，可以很方便的嵌入别的程序里。

* **可扩展**: Lua提供了非常易于使用的扩展接口和机制：由宿主语言(通常是C或C++)提供这些功能，Lua可以使用它们，就像是本来就内置的功能一样。

* **其它特性**:

    - 支持面向过程(procedure-oriented)编程和函数式编程(functional programming)；

    - 自动内存管理；只提供了一种通用类型的表（table），用它可以实现数组，哈希表，集合，对象；

    - 语言内置模式匹配；闭包(closure)；函数也可以看做一个值；提供多线程（协同进程，并非操作系统所支持的线程）支持；

    - 通过闭包和table可以很方便地支持面向对象编程所需要的一些关键机制，比如数据抽象，虚函数，继承和重载等。

## Lua 应用场景

* 游戏开发

* 独立应用脚本

* Web 应用脚本

* 扩展和数据库插件如：MySQL Proxy 和 MySQL WorkBench

* 安全系统，如入侵检测系统


[lua]: https://www.lua.org/