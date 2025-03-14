**初见Python解释器**

是一种用来执行其他程序的程序（介于代码逻辑和硬件之间）

对待python程序的视角：程序员/python解释器 

①程序员：从上到下执行      ②字节码（加速代码执行 --pyc extension (“.pyc” means compiled “.py” source)）->虚拟机

下次运行时，python就不会再次编译代码了（在没有修改源代码的前提下）                                        --python versions:如果是用不同python版本编译的是：3.2之前是同一个字节码版本；3.2之后则是另一个字节码版本 <u>--字节码和源代码修改是字节码重新生成的主因</u>

如果python不能将字节码保存在你的电脑里，但你的程序依旧会运行，程序运行结束后则会直接丢弃字节码。-- python甚至可以在没有源代码的情况下，直接运行 .pyc 文件

PVM(python 虚拟机) ->代码执行的实际位置

![](C:\Users\li\AppData\Roaming\marktext\images\2025-03-03-13-24-46-image.png)

其实它就只是一段来回循环的程序，把你的byte code从头到尾看了个遍 （python解释器的最后一步）

**性能方面**

python字节码并不是实际的机器码，这是python独有的一种的对代码的表现形式，code编写完成之后会立刻开始执行

**开发方面**

python的执行和运行环境其实没有特别明显的区别（there is no initial compile-time phase at all）

Cpython就是在python org官网上能下载到的版本-> portable ANSI C

**Frozen Binaries**

有些时候人们想把python直接转化为机器码(standalone binary code)，也就是说实际运行此类代码时，不需要安装python

典型代表（window exe）实际上打包的是你的python代码，所有的支持文件和PVM（解释器）

**<u>quizz</u>**

1.什么是python编译器？执行python程序的程序

2.什么是源代码？ 你为程序写的各种语句

3.什么是字节码？    在python编译你的源码程序后生成的一种低等级的程序表现形式

4.什么是PVM? python 虚拟机 - the runtime engine of Python that in
terprets your compiled byte code.

5.
