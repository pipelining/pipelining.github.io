---
title: "Objective-C 编程"
---

本节将直接切入主题, 演示如何编写第一个Objective-C程序.

首先, 举一个很简单的例子, 在屏幕上显示短语 "programming is fun!" 的程序.以下代码显示了完成此任务的代码.
```
	#import <Foundation/Foundation.h>
	int main (int argc, const char *argv[]) {
		@autoreleasepool {
			NLog (@"Programming is fun!");
		}
	}
```

### 编译并运行程序

在详细解释这个程序之前, 我们首先要学习编译和运行此程序的步骤. 可以使用Xcode编译并运行程序, 也可以使用GUN Objective-C编译器在Terminal窗口编译并运行程序. 我们将用这两种方法分别实现这一系列步骤. 然后, 你可以确定如何处理本书其余部分的程序.

	
***

#### 使用Xcode
Xcode是一款功能齐全的应用程序, 使用它可轻松输入, 编译, 调试和执行程序. 

启动Xcode, 在启动页面选择 "Create a new Xcode projects"
![创建一个新项目](../assets/images/demoImage/02-demo01.png)

此时出现一个窗口, 如下图所示.
![选择应用类型](../assets/images/demoImage/02-demo02.png)

在macOS下, 选择command Line Tool后, 会弹出一个面板.
![指定应用名称及组织标识](../assets/images/demoImage/02-demo03.png)

输入应用的名字, 及Organization Identifier, 点击Next. 选择创建位置, 点击Create按钮创建新应用. 显示如下.
![Xcode项目窗口](../assets/images/demoImage/02-demo04.png)

在左侧窗格选择main.m, 现在, 你可以输入第一个程序了.
![main.m文件编辑窗口](../assets/images/demoImage/02-demo05.png)

Objective-C源文件使用.m作为文件名的最后两个字符(称为扩展名). 如下列出了常见的文件扩展名:

-.c C语言源文件
-.cc, .cpp C++语言源文件
-.h 头文件
-.m Objective-C源文件
-.mm Objective-C++源文件
-.pl Perl源文件
-.o Object(编译后的)文件

返回Xcode项目窗口, 窗口右侧显示了文件main.m的内容, Xcode能自动创建一个模板文件,包含以下内容:
```
//
//  main.m
//  demo
//
//  Created by 张冬冬 on 2016/xx/xx.
//
//

#import <Foundation/Foundation.h>

int main(int argc, const char * argv[]) {
    @autoreleasepool {
        // insert code here...
        NSLog(@"Hello, World!");
    }
    return 0;
}
```

你可以在该窗口编辑文件. 修改Edit窗口中显示的程序, 使之与本节开始时给出的程序相符. 以两个斜杠字符//开始的行称为注释.

现在可以用Xcode编译并运行第一个程序了, 在这之前, 通过点击右上角中间图标
![Xcode调试区域显示](../assets/images/demoImage/02-demo06.png)

可以打开一个窗口, 该窗口用于显示程序的运行结果(输出). 将鼠标置于图标之上会显示 "Hide or show the Debug area". 在有数据写入调试区域时, Xcode一般会自动显示调试区域.

现在, 单击上方Run按钮, 或者command+r, Xcode将会分别执行编译和运行程序. 当你的程序没有错, 运行的过程才会执行.

如果在你的程序中出现错误, 会出现含有惊叹号的红色终止记号表示的错误 -- 称为严重错误, 只有修正了这些错误, 才能运行程序. 如果出现含有惊叹号的黄色三角形表示的警告 -- 在消除这些警告之前, 尽管你仍能运行程序, 但通常需要检查并修正这些问题. 修正所有的错误, 
运行程序之后, 右下区域会显示程序的输出.如下所示.