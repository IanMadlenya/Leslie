# C&C++ : GCC&G++

从来没有好好学习过编程，一切从头开始。

# 预编译

```bash
gcc -E helloworld.c -o helloworld.i
gcc -C -E helloworld.c -o helloworld.i #保留注释
```

# 查看文件关联信息

```bash
gcc -M helloworld.c
```

# 编译

```bash
gcc -S helloworld.i -o  helloworld.s
```

# 汇编

```bash
gcc -c helloworld.s -o helloworld.o
```

# 连接

```bash
gcc helloworld.o -o helloworld
```

# 头文件目录
```bash
gcc -I/home/balabala/inc1/ -I/home/balabala/inc2/  helloworld.c -o helloworld
```
# 库目录和库
```bash
gcc -L/home/balabala/lib/ -ltvm helloworld.c #目录~/lib/下载找libtvm.so库文件
```
# 定义符号常量
```bash
gcc -DENV1 -D ENV2 helloworld.c -o helloworld
```
# 开启警告
```bash
gcc -Wall helloworld.c -o helloworld
gcc -Werror helloworld.c -o helloworld
```
# 优化
```bash
gcc -O1 helloworld.c -o helloworld
gcc -O2 helloworld.c -o helloworld
gcc -O3 helloworld.c -o helloworld
```
# 使用管道代替临时文件
```bash
gcc -pipe helloworld.c -o helloworld
```
# 静态、共享
```bash
gcc -static -L../lib/ -ltvm helloworld.c -o helloworld
gcc -shared -L../lib/ -ltvm helloworld.c -o helloworld
```
