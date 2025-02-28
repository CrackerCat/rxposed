# rxposed

### 介绍
rxposed,是一个无感知的Android平台应用注入框架，主要用来对抗应用侵入检测。


### 平台支持
目前只支持android 13 ,后续可能会对android 11 和12 兼容，但是不会兼容11以下，主要是因为andrid11以上开始有包可见性问题，这样就可以隐藏安装在手机上的管理app。





| 项目       | rxposed | xposed                                                       | frida                    |
| :--------: | :-----: | :----------------------------------------------------------: | :----------------------: |
| 定位 | 在测试方面不如frida,在模块生态方面不如xposed，但是就功能而言完全可以兼容xposed，并且扩展了native接口。同时还提供了类似frida版本的native模块实现，完全可以做到frida能做到的 | 插件型改机类工具， | 应用测试类工具快速的对应用进行测试，测试逆向结果，运行情况等等 |
| 反检测对抗 | rxposed自带反检测功能和模块隐藏加载功能 | 本身不具备反检测功能，只能依靠使用者自行对抗                                 | 本身不具备反检测功能，只能依靠使用者自行对抗 |
| 使用便捷性 | app安装到手机上，需要使用就开启，不需要可以关闭，没有任何痕迹留存，也不依赖任何外部模块，只需要root权限 | 需要刷机，打开和关闭，都需要重启 | 虽然便携，但是每次使用都需要进入控制台打开server服务 |
| 兼容以及运行 | 实现原理简单，依赖少，只支持特定版本，兼容性很好 | 多android版本支持，但是存在一定的稳定运行问题 | 多android版本支持，但是兼容需要通过不同的frida版本来解决，存在一定的稳定运行问题 |
| 模块开发详情 | android本地代码开发，只提供入口函数，开发复杂项目难度低，而且由于是纯原生，所以兼容好，运行稳定 | android本地代码开发，提供了更方便的hook api | js开发，易上手，开发容易，但是想开发复杂项目难度高，学习成本大。 |






### 可能需要者

广大安全开发研究者，它的主要的目是用来无感知注入，有时候这可能需要修改特征，自行编译完成对抗。



[核心技术点具体实现说明文档](/document/android10.md)

| 项目         | 描述                                                                 | 使用说明                                           |
|------------|--------------------------------------------------------------------|------------------------------------------------|
| `Manager`  | rxposed 行为管控app 以及要注入的so                                  | [Manager/README.md](/document/instructions.md) |
| `Tool`     | 进行ptrace的注入工具，同时添加了将注入的so的内存段进行隐藏的功能       |                                                |
| `loadxposed` | 一个rxposed的模块，用于注入加载xposed以及管理xposed模块（目前有些问题，正在处理hook框架的问题，高版本不可用）（感觉没啥用，后续可能删除了） | [loadxposed/README.md](/loadxposed/README.md)  |



### 模块地址
https://github.com/Thehepta/Rxmodule

### 公众号和知识星球
主要以对抗为主题希望大家支持一下

![输入图片说明](document/images/wx.jpg)

知识星球（没免费卷，想支持就支持一下，不想支持也没事，主要是希望可以接触到更多的问题，收集更多的样本）
![输入图片说明](document/images/start.jpg)

如果在使用中遇到任何问题，或者有什么不懂的地方，可以主动联系我


### 致谢
https://github.com/sanfengAndroid/fake-linker

https://github.com/LSPosed/LSPosed

https://github.com/frida/frida



### License

LSPosed is licensed under the **GNU General Public License v3 (GPL-3)** (http://www.gnu.org/copyleft/gpl.html).