# 第一章-Zig介绍

## 欢迎

[Zig](https://ziglang.org/) 诞生于2016年2月，是一种通用编程语言和工具链，用于维护**健壮**、**最佳**和**可重用**的软件。

**强大的**
- 即使对于恶劣情况（如内存不足）也是如此。
  
**最佳的**
- 让程序以最佳方式表现和执行
  
**可重用的**
- 相同的代码适用于具有不同约束的许多环境。
  
**可维护的**
- 将意图精确地传达给编译器和其他程序员。该语言对人阅读代码的开销较低，并且能够灵活应对不断变化的需求和环境。



作为新兴语言代表之一的[Rust](https://rust-lang.org/)，却早在2006年便出现，可见Zig实在非常的年轻，因此Zig仍然是不稳定的，不推荐在生产中使用（最新主要版本是0.9，还未达到1.0，而1.0预计在2025年发布）

要使用此书，我们假设您：

- 有C/C++，Rust或类似语言的编程基础（如果你会使用C#/Typescript并懂得底层编程知识也可以）
- 了解基础算法与数据结构

## 安装

本指南将保证你在最新的有版本号的Zig版本中可用，但是强烈推荐你使用夜间构建版本。因为，Zig的发布往往间隔很久，现阶段开发迅速，使用带版本号的Zig版本可能会过时。

1.从以下位置下载并安装Zig

[下载 ⚡ Zig Programming Language (ziglang.org)](https://ziglang.org/zh/download/)

2.将Zig所在路径添加到环境变量

3.验证安装

```
$ zig version
0.10.0-dev.2951+b9ed07227
```

4.(可选)安装ZLS和编辑器插件

[工具 ⚡ Zig Programming Language (ziglang.org)](https://ziglang.org/zh/learn/tools/)

## Hello World

创建一个Zig文件`main.zig`

```rust
const std = @import("std");

pub fn main() void {
    std.debug.print("Hello World.", .{});
    //std.log.info("Hello World.", .{});
}
```

###### （注意：请确保您的文件使用空格进行缩进，LF行尾和UTF-8编码！

使用命令编译程序到当前目录：`zig build-exe main.zig`
