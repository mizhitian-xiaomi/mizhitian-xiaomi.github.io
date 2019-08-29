---
layout: post
title: DOSBox与MASM环境搭载及简单使用
description: 汇编程序设计课实验环境搭载
tags: Handbooks
---

---

> DOSBox和MASM下载链接
>
> 链接：https://pan.baidu.com/s/1Y21S4IJ5PYMXELMDU1nJjQ 
> 提取码：iusk 

<br>

# 安装DOSBox

<br>

一直下一步就好了，选择安装位置的时候可以自定义，全凭个人习惯。
<br>

### DOSBox更改界面大小

* 来到安装目录下，打开配置文件进行设置

  >  如果找不到自己安装在哪里了，可以右击桌面的快捷方式，再点击`打开文件所在位置`      

![1567074804362](https://raw.githubusercontent.com/mizhitian-xiaomi/mizhitian-xiaomi.github.io/master/images/posts/1567074804362.png)

* 在用DOSBox的过程中受不了界面实在太小了，这一步是更改界面大小的，有需要的自行更改**非必要步骤**
	
 > 在配置语句前加#是注释的意思
 >
 > 绿色框选的是默认配置，红色是我更改界面大小的配置

 ![1567074891958](https://raw.githubusercontent.com/mizhitian-xiaomi/mizhitian-xiaomi.github.io/master/images/posts/1567074891958.png)

### DODBox自动挂载

* 同样也是更改配置文件，我们把配置文件拉到底端就可以看见下面图片的位置

  > 这里是设置自动挂载的目录，这样每次打开DOSBox就不用再挂载了
  >
  > 挂载的意思其实就是.....(以下个人理解有误请指正)
  >
  > >  你的C盘放在哪里，模拟DOS操作系统的资源管理，这个目录被指定为C盘

  1. 在配置文件添加

     `mount <盘名> <目录路径> `         将<盘名>放在<目录路径>下
> 我挂载在当前目录的playground文件夹下
> ![1567074915041](https://raw.githubusercontent.com/mizhitian-xiaomi/mizhitian-xiaomi.github.io/master/images/posts/1567074915041.png)
>
>   2. 运行DOSBox

     `<盘名>:`         进入该盘（你刚刚挂载的盘）

不区分大小写
![1567076062039](https://raw.githubusercontent.com/mizhitian-xiaomi/mizhitian-xiaomi.github.io/master/images/posts/1567076062039.png)


没有挂载则会报错![1567075960875](https://raw.githubusercontent.com/mizhitian-xiaomi/mizhitian-xiaomi.github.io/master/images/posts/1567075960875.png)

**大功告成！！！**

<br>

# MASM使用

<br>

1. 将masm全部拉到你挂载的目录下![1567076156927](https://raw.githubusercontent.com/mizhitian-xiaomi/mizhitian-xiaomi.github.io/master/images/posts/1567076156927.png)

2. 新建一个**.asm**的测试程序

   > 怎么建都行，可以在Windows下建好直接拉到挂载的目录下都可以

   * 输入`masm`，再输入测试程序，一直回车就可以了，最后结果会得到一个`.obj`文件

     ![1567076307770](https://raw.githubusercontent.com/mizhitian-xiaomi/mizhitian-xiaomi.github.io/master/images/posts/1567076307770.png)

	* 输入`link`，执行上一步得到的`.obj`文件，其他步骤同上，得到一个`.exe`文件
	
	  ![1567076454482](https://raw.githubusercontent.com/mizhitian-xiaomi/mizhitian-xiaomi.github.io/master/images/posts/1567076454482.png)
	
	* 执行`debug`，执行上一步得到的`.exe`文件
	
	  > U命令: 对机器代码反汇编显示
	  >
	  > Q命令: 退出DEBUG，回到DOS状态
	
	  debug还有很多命令，自行探索，同为小白我还不会（尬笑...
	
	  ![1567076678562](https://raw.githubusercontent.com/mizhitian-xiaomi/mizhitian-xiaomi.github.io/master/images/posts/1567076678562.png)



### Refer

[调整DOSBOX窗口大小并运行程序](https://blog.csdn.net/m0_37822685/article/details/80241598)

[DOSBox下调试(masm、link、debug)简单的汇编语言程序](https://bingyishow.top/Technical-article/54.html)

[dosbox+masm汇编环境的安装和使用](https://blog.csdn.net/YuzuruHanyu/article/details/80287419)

### Logging

- 190829  xiaomi  init