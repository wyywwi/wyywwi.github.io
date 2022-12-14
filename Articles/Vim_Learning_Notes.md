---
layout: default
title: "Vim"
permalink: /notes/vim/
---

<a href="vim"><img src="https://pica.zhimg.com/v2-53579b05d8e5a22e4700170a6132db04_1440w.jpg?source=172ae18b" alt="Vim Logo" border="0" style="zoom:50%" /></a>


## Vim

> *本部分内容主要来源于 [Learn-Vim-Progressively][1]*

### 1. 在Vim存活下来

为了能够使用Vim进行基本的编辑操作，也许你需要知道以下知识；知道它们不能让你立即体会到Vim带来的好处，但至少你可以顺利地把它当作一个文本编辑器，开始你的工作。

#### 1. 前置知识

Vim的四种模式：Normal-mode, Insert-mode, Command-mode & Visual-mode

- Normal-mode：正常模式（命令模式），用于功能/组合键输入。
- Insert-mode：插入模式，在此模式下类似于Windows下的记事本，不使用功能键而是正常输入。
- Command-mode：命令模式（底线命令模式），可以输入一些特殊指令。
- Visual-mode：可视模式，在这个模式下可以进行一些类似鼠标的操作。

四种模式之间的转换：

- Vim打开自动进入Normal-mode；
- Normal-mode下按 : 或者 / 进入Command-mode；
- Normal-mode下按i,I,a,A,o,O,s,S进入Insert-mode；
- Command-mode下执行完命令或者连按两次 Esc 键返回Normal-mode；
- Insert-mode下按一次Esc键返回Normal-mode。
- Normal-mode下按一次v键进入Visual-mode。

#### 2. 进行操作

1. **进入Vim，然后停止一切动作；*在Normal-mode下每一个按键都有特殊的功能！***

2. **按 i 键或者 a 键进入Insert-mode；i 键为在光标所在字符之前插入文本；a为在光标之后插入。**

3. 进行编辑。

4. 按Esc键返回Normal-mode；

   | Normal模式下命令（系列1） | 作用                               |
   | ------------------------- | ---------------------------------- |
   | x                         | 删除光标下方一个字符               |
   | dd                        | 删除光标所在行并复制到剪贴板       |
   | p                         | 将剪贴板内容粘贴到光标当前所在位置 |

5. 按 : 键进入Command-mode；

   | Command模式下命令（系列1） | 作用           |
   | -------------------------- | -------------- |
   | :w                         | 保存所作的修改 |
   | :q                         | 退出Vim        |
   | :q!                        | 强制退出Vim    |

6. 大功告成！

### 2. 我已出仓，感觉良好

现在你已经学会了怎么用Vim进行最基本的文本操作。是时候再学点东西了！

#### 1. 进入Insert模式的几种姿势

| 功能键 | 作用                         |
| ------ | ---------------------------- |
| i      | 在光标之前插入               |
| a      | 在光标之后插入               |
| o      | 在光标所在行之后另起一行插入 |
| O      | 在光标所在行之前另起一行插入 |
| cw     | 替换从光标开始的这个单词     |

[![vmLaKs.png](https://s1.ax1x.com/2022/08/05/vmLaKs.png)](https://imgtu.com/i/vmLaKs)

[![vmLdrn.png](https://s1.ax1x.com/2022/08/05/vmLdrn.png)](https://imgtu.com/i/vmLdrn)

（合按cw后，光标之后一直到空格之前，“our”三个字母被清空）

#### 2. 更高，更快，更强的Normal-mode

| Normal模式下命令（系列2） | 作用                                           |
| ------------------------- | ---------------------------------------------- |
| 0                         | 前往光标所在行的行首（第一列）（等同于Fn + ←） |
| ^                         | 前往光标所在行第一个非空格字符处               |
| $                         | 前往光标所在行最后一个字符处（行尾）           |
| g_                        | 前往光标所在行最后一个非空格字符处             |
| /example                  | 在光标之后的字符中寻找'example'                |
| yy                        | 复制光标当前所在行                             |
| p                         | 将剪贴板中内容粘贴至光标当前所在行的下一行     |

#### 3. 世上也有后悔药！

| Normal模式下命令（系列3） | 作用           |
| ------------------------- | -------------- |
| u                         | undo——撤销操作 |
| ctrl + r                  | redo——重做操作 |

#### 4. 命令——更多样的命令

| Command模式下命令（系列2） | 作用                           |
| -------------------------- | ------------------------------ |
| :e  path/to/file           | 打开文件file                   |
| :saveas path/to/file       | 另存为path/to/路径下的文件file |
| :bn                        | 打开下一个文件                 |
| :bp                        | 打开上一个文件                 |

### 3. Vim Pro

作为一名学生，上面这些操作已经足够我应付一般的编辑工作。至于写代码这样的复杂工作，我更乐意使用VSCode。（笑

所以，如果你看了觉得还不错，还想继续学下去的话，我将再次推荐[Learn-Vim-Progressively](http://yannesposito.com/Scratch/en/blog/Learn-Vim-Progressively/)————这确实是一个好教程。

如果你的英语不好，我也推荐这一篇[知乎文章]（https://zhuanlan.zhihu.com/p/68111471): 行文内容清晰，作为操作速查也十分合格。

以上~
