# OpenGL 指南

## OpenGL准备工作

> 一、安装GLFW

```bash
GLFW是c语言版本的OpenGL库

下载cmake、vistual studio （需要安装windows cmake 组件）
https://learnopengl-cn.github.io/01%20Getting%20started/02%20Creating%20a%20window/#_3

visual studio 2019 cmake后出现的问题  #对 COM 组件的调用返回了错误 HRESULT E_FAIL

解决方案：
1.找到Developer Command Prompt for VS 2019 以管理员权限运行
2.E:…\Common7\IDE\PublicAssemblies  跳转至vs安装目录对应的目录
3.执行命令gacutil -i Microsoft.VisualStudio.Shell.Interop.11.0.dll
4.重启Cmake后的工程
参考来自:https://blog.csdn.net/u013419838/article/details/103697286
```

> 二、引用

```bash
将第三方库统一放入一个文件夹中，include 和 lib 分开存放
在工程中添加对应的库引用目录和头文件引用目录
```

![image-20210707141451477](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210707141451477.png)

```bash
添加依赖库文件
```

![image-20210707141549532](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210707141549532.png)

>三、安装GLAD

```basic
OpenGl 不同版本接口函数不一致，通过glad在线可以获取对应的OpenGL函数
在https://glad.dav1d.de/ 输入对应的版本号
Profile选择Core，生成库文件

下载OpenGL Extensions Viewer 可以查看opengl版本
```

![image-20210707141952568](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210707141952568.png)

![image-20210707142014385](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210707142014385.png)

```basic
下载glad.zip 解压后得到 include 和 src 文件夹

include走头文件引用，src中的glad.c引入工程中

注意#include <glad\glad.h>  的引用，需要放在所有头文件引用之前
```

