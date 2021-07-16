# 介绍
Rust是用于替代C++的语言。不太可能替代C因为C还是更底层。

# 安装
在Windows下，安装rustup-init.exe，这个软件会自动下载安装rustc（编译器），cargo（包管理和build工具）。IDE的话，暂时可以使用Vim或者VSCode+插件的方法。

# 特性
## ownership 
这是rust最核心的技术，是它不需要GC的原因。由编译器在编译的时候就检查一个堆上变量的作用域，当离开作用域后，就会自动调用释放内存的函数，
是C++ RAII惯用法的体现，编译器保证内存不会发生泄露和多次释放。

### 引用 reference

1. 在任何的时刻，一个变量只能有一个可变的引用，或者多个不可变的引用
2. 引用指向的值必须总是有效的