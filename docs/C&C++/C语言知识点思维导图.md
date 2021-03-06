> 用心分享，共同成长
>



<p align="center">本文已经收录至我的github,欢迎大家踊跃star 和 issues。</p>
<p align="center"><a  href="https://github.com/midou-tech/articles" target="_blank">https://github.com/midou-tech/articles</a></p>
&emsp;最近有很多学弟学妹问我要期末C语言复习重点，刚开始我很是不以为然的，觉得大家肯定是闹着玩的，想当年可是平时不学习，考试奋斗几天的人，妥妥的考过。不吹了，不吹了，看着学弟学妹们这么诚恳的给我说，我不得不牺牲我的休息时间，给大家整理了一份史上最全的C语言复习思维导图。按照这个思维导图去复习，要是考不过，学长给您。。。

![image-20200103011543542](https://tva1.sinaimg.cn/large/006tNbRwly1gaiq04k0p3j30wq0digmt.jpg)



&emsp;这么好的东西记得分享给你的同学噢，看完记得**点赞👍**  **关注❤️**  ，学长长期更新噢。有问题还可以加学长微信(回消息不会太快，但是问问题一定会回复你的，会在晚上十点之后了。)

![C语言详细知识点脑图](https://tva1.sinaimg.cn/large/006tNbRwly1gaiq8nycm4j30u01dlaqs.jpg)

<p><h4   style="color:green;text-align:center">点关注，不迷路！！！</h4></p>
&emsp;`敲黑板、划重点，看好啦，以下都是必考点`

###填空题

1. C语言的标识符，标识符规则，比如`标识符只能由字母、数字和下划线组成，字母区分大小写`这只是一条，还有其他几条，老师很喜欢玩这种填空题。
2. 数据类型，几种数据类型以及各种数据类型的范围，课本上应该有一张图，这个要看明白，填空题会考。
3. 数据类型对应在平台下的大小，这个题很坑的，一定看清楚前置条件说的是多少的平台。
4. 进制转换，二进制、八进制、十进制、十六进制四种进制之间的转换，如2进制转十进制，十进制转十六进制等其他几种。
5. 运算符，前置和后置运算的顺序，包括+=，-=，*=，/=运算。
6. 原码、反码、补码计算。
7. 数组相关填空题，如int a[5] = {1,2,3,4,5}；求 sizeof(a)，sizeof(&a)，sizeof(a[1])。
8. 指针的运算，如int array[5] = {1,2,3,4,5}; int \*p = &a; 问你p++或者p+1的值。
9. 移位运算，如 16>>1  为多少？
10. 结构体数据类型的大小，给你整个复杂的结构体，问你结构体大小？（结构体是有内存对齐问题的，不是简单的各类型大小相加。）
11. 字符串相关问题，比如问你常用字符串函数？

### 编程题

**学校老师出的编程题**

1. 编一个函数，从屏幕获取两个整数，交换两个整数。
2. 编写一个函数，从终端输入三个数，求出三个数中的最大数。
3. 实现冒泡排序，并使得交换次数最少。
4. 给定一个链表，删除指定链表某个节点。

面试中常问的问题

1. 编写一个printf函数，要求能支持所有数据类型的的输出，支持可变参数。

&emsp;不要小看这个题目，不要说我天天使用printf函数，还真没想过自己去写。也不要说我们只是用printf函数就好，实现它干嘛，其实实现它不重要，重要的是你要学会去分析和质疑；你有没有遇到printf函数出错的时候，如果遇到了你会怎么处理？  不吹的说，这个看似简单的题会考难道80%在校大学生，而且能考到很多C语言很牛逼的同学。当然放心你们考试一定不会考这个问题。

2. 选一个最熟悉的排序算法，给指定数组排序，要求数组元素任意，排序方向任意。
3. 给定两个有序单链表，合并两个单链表。
4. 给定一个单链表，将改链表逆置，要求空间复杂O(1)。
5. 编写一个程序求出一个单链表是否带有环。



### 分享一个重要知识点，这个点在面试中会被问到

**结构体内存对齐原因：**

1、平台原因(移植原因)：
不是所有的硬件平台都能访问任意地址上的任意数据的；某些硬件平台只能在某些地址处取某些特定类型的数据，否则抛出硬件异常。

2、性能原因：数据结构(尤其是栈)应该尽可能地在自然边界上对齐。
原因在于，为了访问未对齐的内存，处理器需要作两次内存访问；而对齐的内存访问仅需要一次访问。

**结构体内存对其规则：**

1.第一个成员在与结构体变量偏移量为0的地址处。
2.其他成员变量要对齐到某个数字（对齐数）的整数倍的地址处。
    //对齐数 = 编译器默认的一个对齐数 与 该成员大小的较小值。
    VS中默认的值为8
    linux中的默认值为4
3.结构体总大小为最大对齐数（每个成员变量除了第一个成员都有一个对齐数）的整数倍。
4.如果嵌套了结构体的情况，嵌套的结构体对齐到自己的最大对齐数的整数倍处，结构体的整体大小就是所有最大对齐数（含嵌套结构体的对齐数）的整数倍。

<p><h4   style="color:red;text-align:center">求点赞👍  求关注❤️ </h4></p>
<p><h4   style="color:blue;text-align:center">「转发」是明目张胆的喜欢，「在看」是偷偷摸摸的爱。</h4></p>
`有偿征文(具体细则公众号回复征文)，欢迎投稿或推荐你的项目。提供以下几种方式投稿`

- `去我的github提交 issue:` https://github.com/midou-tech/articles
- `发送到邮箱: 2507367760@qq.com 或者 longyueshier@163.com  或者 longyueshier@gmail.com`
- `微信发送: 扫描下面二维码，公众号里面有作者微信号。`

**公众号还不能留言，有任何疑问可以发送邮件或者微信咨询我**。

`精选文章都同步在公众号里面，公众号看起会更方便，随时随地想看就看。微信搜索 龙跃十二 或者扫码即可订阅。`

<p align="center"><image src="https://tva1.sinaimg.cn/large/006tNbRwly1gajt6oiqwmj30p00dw79g.jpg" ></image></p>