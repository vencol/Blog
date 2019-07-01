Markdown语法目录
使用[TOC]生成如下目录
[TOC]
使用页内span id跳转的目录<span id="TOCID"></span>
1. [标题分级](#title_split)
1. [空格](#space)
1. [列表](#list)
1. [引用](#reference)
1. [跳转](#jump)
1. [插入图片](#picture)
1. [LaTeX 公式](#formula)
1. [流程图](#flowchart)
1. [表格](#table)
1. [代码](#codeid)
1. [分割线](#dividing)
1. [注脚](#footnote)
# Markdown语法锚点 {#maodian}
## 锚点测试 {#ads}
## **<span id="title_split"></span>[标题分级](#TOCID)**
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
## **<span id="space"></span>[空格](#TOCID)**
1. 直接使用中文状态下的空格，但有时候这种方法不管用的时候可以使用planB。
1. 半方大的空白&ensp;或&#8194;`&ensp;或&#8194;`;号是必须的
1. 全方大的空白&emsp;或&#8195;`&emsp;或&#8195;`;号是必须的
1. 不断行的空白格&nbsp;或&#160;`&nbsp;或&#160;`;号是必须的

## **<span id="list"></span>[列表](#TOCID)**
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

## **<span id="reference"></span>[引用](#TOCID)**
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

## **<span id="jump"></span>[跳转](#TOCID)**
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
	跳转至[本地鸡血图片](00Markdown语法0.jpg)

## **<span id="picture"></span>[插入图片](#TOCID)**
1. 插入本地图片，使用`![本地鸡血图片](00Markdown语法0.jpg)`
	![本地鸡血图片](00Markdown语法0.jpg)
1. 插入网络图片，使用`![网络图片](https://raw.githubusercontent.com/vencol/Blog/master/1906/00Markdown%E8%AF%AD%E6%B3%950.jpg)`
	![网络图片](https://raw.githubusercontent.com/vencol/Blog/master/1906/00Markdown%E8%AF%AD%E6%B3%950.jpg)
1. 输入base64数据流图片
```
![avatar](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACEAAAAeCAIAAAAtquBAAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAZ9SURBVEhLrVZrbBRVFL7z2Jndbtt99LV90ZZtBVqF8GghSI0QwQchkpj4A1FEJSag0fjDGIIYAiEmEgNoYkj8oaKBRFEBHwmBQltEQBNsAUkf0m1p2dJuu+x2233MzB3PuXd2+zImJp5chjP38X3nfOfc6QoFe5vI/2SCIFgeIaZATMsl0zjmO8M7yttL1HFicqPMYU9K4UEI5Q48iQlO+pU51kx6MphyHh5ZO6RWCIX7zlsMhBye17zGe8dChDhwa/oMQDACMMTCGSOzxByDLRnpPeg0h4p3jT4nWvDMStTYZMj8ZIaAOewwn5lKAHD/QECpUUSGjOFekQokM7gySIDPNEHaB5NdflN2a5oOPi5ZBOhw3CkOCwKGoU/LAylmELDAYTBQQ7AX5tW/6V3ymi55dB1jZysW0xRnMkuAnc5B6L9KZMZ6z/ecfS8+Hsmu2WgrWq74GiRvHWSnaSAWoE8SgMErRA3NNo0DijpJwB2+m82ACJIo5ORXZblL8/yryxrfKVm1s2LdAf/Tn/oe2U2VIg0zy2RgaQWoMgfnxqTiO7CLuESoFTsDvt1Xn790R3xsJPD78XgkaGhxJcvjKV/qm7c6t3x5oPmDSOdpmwhqQwYZHCJPvTiTCywETsBmDHhXCxfn1m7ubvl4uPOcLFHAgns2QWm049tAi6dm7btVq3e2h3q00DVZSMfK8phdc6YMI7D2sQzk3Epn5brAL59EAxdyHILLIWarYpYiOBWSbRccdKTz5OsDbSeKlzyfTFEDQsLjKBfAzuBgyjACdBgBMhEpZ+5TQ90tsYGrDpvpUIgEghAq2uy5/seLlr1asWbP/PX7bfZsd8nCvLpnNJQKj0OBQSehYP8Fi4GQ4/5jD6hDnIBngAkZNLt6A1WLAq2HHIqpykSwgoBWopqupzQDqi0qLimrQHGVJyMD2nCbXUIZuiNZ2/tfnKkVHMbAMwSU2jw1Uq5/sP0bRaKq3SnYcqhoR/mwRoZITCiMKpuwqoe7Yt0/a0N/yAIDYQNgkQPTYYZTaYkQxDAExeNduHXwxmktekeRiWf+xvK1B2AUN+5Wi1ekNEQRBSqLYs2Gg77Fm8AHPolxIBR+Rqf3LqADuFq4SFS9guIichY8+347Oj54DWsgENlZ3NV6ZKT7gruk1r/6beiESMd3smg6fEtBsZw5jX1XvhDNBDBZavM8IHyOD8b6ykjGRh2ljfmLtgz13exp/Wj87lUgkEEUVA/iQmX0kRu3z+0tbXg5gV1kuuY+Grx+yjA0OacMLiKTmmuFeczUCtZS4c6es7t6Wg9Vrdwm2eyACAQ8LogC7gRIAZUnE0EjGSWql4oOZ9FDoc6m6ECbe069DpycIJMHxp82hkJBE7uYinV9f6/9a0/lw7rOlYUkDLjB7CTeZIEmqTYh292io0A3zEQ0GL7dnOdvhI8yFNMiyOSBClnG1wwsnY1EO07QeAhLBCpZx5CF+4Jog6ElYo78eWqur27jh+UNW/OqG6GNWcsxgtl5oCCMBkwwDUUyJ3qboDVZmyENC8faIEEGak58tM9VsTJw5cvAlaOBy59F+ttcFSs0LAnbmckjY4wCuxaVsXQzJAHDYQeQQ1KcUla+w7eksGF77+XPFafb7i69d/PHRPBqYuDS8J+nfQ+uN/CjbuUNHTWtd+NlL6TcAnBgpPAPqmfSyP3R/P6D7ICRiA6U12/W6tZDtQdvNYU6zmR7yxL37+hj/XZoDcEMd/xQXfOYaHNSGhExOMxDKHq/hROAHWnMfXLZgks3ghev3+VpbnliwWgwIFzchI0LLWcqSUPWUykjEYE2VERTkkXdtAElCAt/ryEqQ87R4xG49vD611juW+E3pmmF0ZtmbaWnoy/006/dMKLjSdYkmBAMyRhXjbCDjDlV4lRMRaYiTcnGGCeAqOEpamFFtP5+gPwAO6t3CTl1sSsYilAKPwzwtwEjZuLiKn45JBHqhA4cgBn2cwMJYBtgwGWFFGEeCWbXHMDgln515nokNlFX6YXBoS0CgMg41o8568kJ2BIz5nAfbvhMreAGTcST1SXuPS+t2vdKY3GeE5sdz0A9eMtNQs8kQM9yOEE4pRBBxL6CrwjngFmnQ3l2zYKh0VieKwsRCQHgwH3HFOhMK3OHwwET/M9e0wT34vZjoXqpsgj7KsOxv1ZbXOqOJ7W+wXBVsRvihuCDwcFtJ2/xDf/NIANvsVRY8TfCO5lH5PGOoQAAAABJRU5ErkJggg==)
```

![base64图片](data:image/png;base64,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)

## **<span id="formula"></span>[LaTeX 公式](#TOCID)**
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
## **<span id="flowchart"></span>[流程图](#TOCID)**
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

## **<span id="table"></span>[表格](#TOCID)**
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

## **<span id="codeid"></span>[代码](#TOCID)**
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


## **<span id="dividing"></span>[分割线](#TOCID)**
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

## **<span id="footnote"></span>[注脚](#TOCID)**
* 注脚会自动安排到末尾
* 使用 Markdown[^1]可以效率的书写文档, 直接转换成 HTML[^2], 你可以使用 Leanote[^Le] 编辑器进行书写。

[^1]:Markdown是一种纯文本标记语言
[^2]:HyperText Markup Language 超文本标记语言
[^Le]:开源笔记平台，支持Markdown和笔记直接发为博文


