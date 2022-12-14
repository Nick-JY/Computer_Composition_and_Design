#### 通用寄存器：
- 我们知道寄存器是CPU中存储小数据的一个存储器，因此CPU在读取寄存器数据的时候异常的快。
- 通用寄存器指的是可以存储任何二进制数的寄存器，这个数可以是某个存储单元的地址，也可以是某一条指令，也可以是某个数据。
##### a.通用寄存器数量:
- 在MIPS-32中，通用寄存器的数量为32个，并且每个寄存器都是32位。
- 32个寄存器能够使MIPS-32架构具有更高的性能。
##### b.通用寄存器的分类：
###### 1.零寄存器：
- $zero，寄存器编号为0，该寄存器永久存放0，规定不能进行更改。
###### 2.临时寄存器：
- $t0 ~ $t7，寄存器 $t0的编号是8，这类寄存器主要用来存放过程(c语言中的函数)中创建的临时变量的值，使用后不需要恢复临时寄存器原有的值。
###### 3.保留寄存器：
- $s0 ~ $s7，寄存器 $s0的编号是16，这类寄存器用来存放主函数中变量的值，如果在过程中需要使用保留寄存器，需要把保留寄存器的值换出到栈，使用完之后在把栈中存储的值存回保留寄存器。
###### 4.额外的临时寄存器：
- $t8 ~ $t9。
###### 5.全局指针：
- $gp，存储的是存储区中静态区的某个地址，通过偏移来访问整个静态区。在C语言中，全局变量和static声明的变量都存放到存储区中的静态区。
###### 6.栈指针：
- $sp，存储的是栈顶的地址，栈指针指向当前创建的栈区的顶端。
###### 7.帧指针：
- $fp，存储的是栈底的地址，帧指针指向当前创建的栈区的底部。
###### 8.返回地址寄存器：
- $ra，用来存储某个过程的返回地址。(C语言在调用函数结束后要返回主函数)