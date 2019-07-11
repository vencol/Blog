# 士兰微bldc学习<span id="TOCID"></span>
1. [IQ库学习](#iqmathlib)
1. [矢量合成学习(SVPWM)](#svpwm)
1. [函数分析](#funanalysis)
1. [linux文件系统与驱动](#fsdriver)
1. [devfs文件系统与驱动](#devfsdriver)
1. [sysfs文件系统和linux设备模型](#sysfsmode)
1. [udev的组成](#udevmakeof)
1. [udev规制文件](#udevrule)
## <span id="iqmathlib"></span>[IQ库学习](#TOCID)
1. [IQ库英文文档](pic/04IQ_math_lib.pdf),文件路径：pic/04IQ_math_lib.pdf
1. [IQ库中文文档](pic/04IQmath中文手册.pdf),文件路径：pic/04IQmath中文手册.pdf
1. [Sin_Table](https://www.mymathtables.com/trigonometric/cotangents-0to90-tables.html),文件路径：https://www.mymathtables.com/trigonometric/cotangents-0to90-tables.html
## <span id="svpwm"></span>[矢量合成学习(SVPWM)](#TOCID)
![基本电压矢量图](pic/04基本电压矢量图1.png)
![期望电压矢量图](pic/04期望电压矢量图2.png)
![电压和磁链关系](pic/04电压矢量和磁链的关系4.png)
![合成电压矢量(磁势)图](pic/04合成电压矢量(磁势)图3.png)
|电压|开关S<sub>A</sub>|开关S<sub>B</sub>|开关S<sub>C</sub>|U<sub>A</sub>|U<sub>B</sub>|U<sub>C</sub>|合成U<sub>S</sub>|
|:-|:-|:-|:-|:-|:-|:-|:-|:-|
|U<sub>0</sub>|0|0|0|-U<sub>d</sub>/2|-U<sub>d</sub>/2|-U<sub>d</sub>/2|0|
|U<sub>1</sub>|1|0|0|U<sub>d</sub>/2|-U<sub>d</sub>/2|-U<sub>d</sub>/2|sqrt(2/3)U<sub>d</sub>|
|U<sub>2</sub>|1|1|0|U<sub>d</sub>/2|U<sub>d</sub>/2|-U<sub>d</sub>/2|sqrt(2/3)U<sub>d</sub> e<sup>j*pi/3</sup>|
|U<sub>3</sub>|0|1|0|-U<sub>d</sub>/2|U<sub>d</sub>/2|-U<sub>d</sub>/2|sqrt(2/3)U<sub>d</sub> e<sup>j*2pi/3</sup>|
|U<sub>4</sub>|0|1|1|-U<sub>d</sub>/2|U<sub>d</sub>/2|U<sub>d</sub>/2|sqrt(2/3)U<sub>d</sub> e<sup>j*pi</sup>|
|U<sub>5</sub>|0|0|1|-U<sub>d</sub>/2|-U<sub>d</sub>/2|U<sub>d</sub>/2|sqrt(2/3)U<sub>d</sub> e<sup>j*4pi/3</sup>|
|U<sub>6</sub>|1|0|1|U<sub>d</sub>/2|-U<sub>d</sub>/2|U<sub>d</sub>/2|sqrt(2/3)U<sub>d</sub> e<sup>j*5pi/3</sup>|
|U<sub>7</sub>|1|1|1|U<sub>d</sub>/2|U<sub>d</sub>/2|U<sub>d</sub>/2|0|
## <span id="funanalysis"></span>[函数分析](#TOCID)
|函数|功能分析描述|
|:-|:-|
|svpwmGen()|逆变波形svpwm产生<br>1. 通过 Ualpha 和 Ubeta 确定当前的实时扇区<br>2.通过表确定扇区所在位置 |
|||