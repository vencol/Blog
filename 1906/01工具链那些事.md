Markdown语法目录
使用[TOC]生成如下目录
[TOC]
# Markdown语法锚点 {#maodian}
## 锚点测试 {#ads}
## **<span id="title_split">标题分级</span>**
- 标题分级主要需要注意几点，多少个#号多少级，#号和标题之间需要空格，如下所示类比于html的h1...h5
* # 一级标题
* ## 二级标题
* ### 三级标题
* #### 四级标题
* ##### 五级标题
```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
```
## **<span id="list">列表</span>**
1. 无序列表
	* 使用 *，+，- 表示无序列表，他们可以单独或者交替使用，不影响最后效果
	- 无序列表项 一
	- 无序列表项 二
	- 无序列表项 三
	- 无序列表项 四
	```
	+ 无序列表项 一
	- 无序列表项 二
	* 无序列表项 三
	- 无序列表项 四
	```
1. 有序列表
	* 有序列表使用数字加上英文句号空格的方式，其中数字不必按顺序，会自动递增
	1. 有序1
	1. 有序2
	2. 有序3
	```
	1. 有序1
	1. 有序2
	2. 有序3
	```
* 有时列表会导致误识别，如123. test会由于前面的有序列表导致变成递增的列表，此时需要写成123\. test,这样不会被markdown误识别

## **<span id="list">跳转</span>**
1. 页内锚点跳转
	* 锚点跳转的方式有局限性，需要先定义锚点，后放置跳转入口，且锚点必须放置在标题（不管几级）后面，语法为```[显示的字符](#ID)```其中ID是可以自定义的
	跳转至[Markdown语法](#maodian)
	跳转至[锚点测试](#ads)
1. 页内span id跳转
	* 使用html方式进行页面跳转，相对比较灵活，可以不管id定义先后，语法为```[显示的字符](#ID)```其中ID是可以自定义的span id。
	跳转至[标题分级](#title_split)
	跳转至[锚点测试](#ads)
1. 超链接跳转
	* 使用超链接跳转可以跳转到外部链接以及相对的文件路径跳转位置。语法为```[显示的字符](路径)```其中路径可以是网址，也可以是文件路径。
	跳转至[百度搜索](https://www.baidu.com)
	跳转至[readme](../README.md)
1. 链接图片
	* 图片跳转的本质也是路径跳转，语法为```[显示的字符](路径)```其中路径可以是网址，也可以是文件路径。
	跳转至[网络图片](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1561367119854&di=4a8e27c9526bc15a1049cd2f2518235e&imgtype=0&src=http%3A%2F%2Fbbswater-fd.zol-img.com.cn%2Ft_s1200x5000%2Fg2%2FM00%2F04%2F06%2FChMlWl0PLL6IFdHHAAL7rD_mjKAAALLKwMCtcIAAvvE767.jpg)
	跳转至[本地鸡血图片](pic.jpg)

## **<span id="list">引用</span>**
* 引用有时也可以当成文档排布来用，语法就是箭头>,多少个箭头就有多少个嵌套引用,同时新行直接回车可以连续前面的引用层，最后回一层断开？
> 这是第一层
回车后还是一层
>> 这是第二层
回车后还是二层
>>> 这是第三层
回车后还是三层
>>>> 这是第四层
回车后还是四层
>>> 这是第三层
回车后还是三层
>> 这是第二层
回车后还是二层

> 这是第一层
回车后还是一层
```
> 这是第一层
回车后还是一层
>> 这是第二层
回车后还是二层
>>> 这是第三层
回车后还是三层
>>>> 这是第四层
回车后还是四层
>>> 这是第三层
回车后还是三层
>> 这是第二层
回车后还是二层

> 这是第一层
回车后还是一层
```

## **<span id="list">LaTeX 公式</span>**
1. 用$ 表示行内公式
	- 质能守恒方程可以用一个很简洁的方程式 $E=mc^2$ 来表达。其代码为```$E=mc^2$```
1. 用$$ 表示整行公式
	> $$\sum_{i=1}^n a_i=0$$
	$$f(x_1,x_x,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2 $$
	$$\sum^{j-1}_{k=0}{\widehat{\gamma}_{kj} z_k}$$
	
	```
	$$\sum_{i=1}^n a_i=0$$
	$$f(x_1,x_x,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2 $$
	$$\sum^{j-1}_{k=0}{\widehat{\gamma}_{kj} z_k}$$
	```
## **<span id="list">流程图</span>**
<div>
<textarea id="code" style="width: 100%;" rows="11">
st=>start: Start|past:>http://www.google.com[blank]
e=>end: End:>http://www.google.com
op1=>operation: My Operation|past
op2=>operation: Stuff|current
sub1=>subroutine: My Subroutine|invalid
cond=>condition: Yes
or No?|approved:>http://www.google.com
c2=>condition: Good idea|rejected
io=>inputoutput: catch something...|request

st->op1(right)->cond
cond(yes, right)->c2
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)->op2->e
</textarea>
</div>
<div>
<button id="run" type="button">Run</button>
</div>
<div id="canvas"></div>

[流程图语法参考](https://flowchart.js.org)

## **<span id="list">表格</span>**
	* 不管是哪种方式，第一行为表头，第二行分隔表头和主体部分，第三行开始每一行为一个表格行。 列于列之间用管道符|隔开。原生方式的表格每一行的两边也要有管道符。 第二行还可以为不同的列指定对齐方向。默认为左对齐，在-右边加上:就右对齐。
	
```
|学号|姓名|分数
|:-|:-:|-:
|小明|男|75
|小红|女|79
|小陆|男|92
```

|学号|姓名|分数
|:-|:-:|-:
|小明|男|75
|小红|女|79
|小陆|男|92

## **<span id="list">代码</span>**
1. 行内式插入代码，如 `printf("hellow")`,语法为\`printf("hellow")`
1. 多行代码
	> #include <stdio.h>
	int main(void)
	{
		printf("Hello world\n");
	}

```
#include <stdio.h>
int main(void)
{
	printf("Hello world\n");
}
```


## **<span id="list">分割线</span>**
	* 你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：
```
***
---
* * *
- - - 
```
1. ***
1. ---
1. * * *
1. - - - 

## **<span id="list">注脚</span>**
* 注脚会自动安排到末尾
* 使用 Markdown[^1]可以效率的书写文档, 直接转换成 HTML[^2], 你可以使用 Leanote[^Le] 编辑器进行书写。

[^1]:Markdown是一种纯文本标记语言
[^2]:HyperText Markup Language 超文本标记语言
[^Le]:开源笔记平台，支持Markdown和笔记直接发为博文


