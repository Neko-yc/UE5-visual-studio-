# UE5-visual-studio-
UE5在visual studio上运行的常见错误以及解决方法

以下是正常运行的展示结果，可以从visual studio编译运行UE5 project：

https://github.com/yclzy/UE5-visual-studio-/blob/main/images/success1.mp4
https://github.com/yclzy/UE5-visual-studio-/blob/main/images/success2.mp4

1.生成visual studio解决方案，在UE5-工具-生成visual解决方案中生成

![](https://github.com/yclzy/UE5-visual-studio-/blob/main/images/%E7%94%9F%E6%88%90visual%20studio%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88new.png)

2.第一次生成的时候因为游戏工程名称为中文报错：

![](https://github.com/yclzy/UE5-visual-studio-/blob/main/images/%E4%B8%AD%E6%96%87%E5%90%8D%E7%A7%B0%E6%8A%A5%E9%94%99.png)

  首先进入到该游戏工程所在的文件夹，强制将游戏工程（.uproject）的名称改为英文
  
![](https://github.com/yclzy/UE5-visual-studio-/blob/main/images/%E4%B8%AD%E6%96%87%E5%90%8D%E7%A7%B0%E6%8A%A5%E9%94%99%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88.png)

  之后进入到UE5中重新生成visual studio代码
  
![](https://github.com/yclzy/UE5-visual-studio-/blob/main/images/%E4%B8%AD%E6%96%87%E5%90%8D%E7%A7%B0%E6%8A%A5%E9%94%99%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%882.png)

3.在debug模式下运行UE5工程报错：未加载shader
  这个问题网上众说纷纭，有的是因为没有在UE5中cook而没有产生shader，有的是因为没有安装win10的SDK而不能cook而没有产生shader，还有的是因为没有选择debug-editor模式下运行
  本人遇到的是第2、3两种问题，并且在安装了win10的SDK后自动就可以cook，没有cook content就自动烘焙了。
  
![](https://github.com/yclzy/UE5-visual-studio-/blob/main/images/%E6%9C%AA%E5%8A%A0%E8%BD%BDshader%E6%8A%A5%E9%94%99.png)
  
  第一种问题：没有在UE5中cook而没有产生shader：
  记得要选择win10的cook
  
![](https://github.com/yclzy/UE5-visual-studio-/blob/main/images/%E7%83%98%E7%84%99%E5%86%85%E5%AE%B9.png)

  第二种问题：因为没有安装win10的SDK而不能cook而没有产生shader：
  
![](https://github.com/yclzy/UE5-visual-studio-/blob/main/images/%E5%AE%89%E8%A3%85win10%20SDK.png)

  第三种问题：没有选择debug-editor模式下运行：
  
![](https://github.com/yclzy/UE5-visual-studio-/blob/main/images/%E9%80%89%E6%8B%A9debug%20editor.png)

4.缺少.net的库错误：visual studio安装库：

![](https://github.com/yclzy/UE5-visual-studio-/blob/main/images/%E2%80%98.net%E2%80%99%E6%8A%A5%E9%94%99.png)

---------------------------------------------------------------------------------------------------------------------
正常运行结果：visual studio运行调用UE5引擎界面，但是又与原本的UE5引擎不冲突

![](https://github.com/yclzy/UE5-visual-studio-/blob/main/images/%E6%AD%A3%E5%B8%B8%E5%90%AF%E5%8A%A8%E6%88%AA%E5%9B%BE.png)
