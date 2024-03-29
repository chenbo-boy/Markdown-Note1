# Markdown-Note1
##### (学习时间：2018-10-04)
## 目录
+ [文本块](#文本块)
    + [单行文本块](#单行文本块)
    + [多行文本块](#多行文本块)
+ [标题](#标题)
    + [标题(Atx形式)](#标题(Atx形式))
    + [分级标题(Setext形式)](#分级标题(Setext形式))
+ [文字高亮(行内标记)](#文字高亮(行内标记))
+ [横线](#横线)
+ [换行](#换行)
+ [文本效果](#文本效果)
    + [斜体、粗体、删除线](#斜体、粗体、删除线)
    + [支持内嵌CSS样式](#支持内嵌CSS样式)
+ [引用](#引用)
    + [单层嵌套](#单层嵌套)
    + [多层嵌套](#多层嵌套)
+ [代码块](#代码块)
+ [序列](#序列)
    + [无序序列](#无序序列)
    + [有序序列](#有序序列)
    + [复选框序列](#复选框序列)
+ [链接](#链接)
    + [外部链接](#外部链接)
    + [本地链接](#本地链接)
+ [插入图片](#插入图片)
+ [图片链接](#图片链接)
+ [锚点](#锚点)
+ [表格](#表格)
+ [diff语法](#diff语法)
+ [参考](#参考)
### 文本块
#### 单行文本块
    语法：在一行开头加入1个Tab或4个空格，注意这一行前面必须要有空行才有效[标题#自带换行类似空行效果]，文本块里的所有Markdown语法会被忽视。
    如：
        这是一个单行文本块
效果：

    这是一个单行文本块
#### 多行文本块
    语法1：在多行开头加入1个Tab或4个空格，注意这一行前面必须要有空行[标题#自带换行类似空行效果]
    如：
        这是多行文本效果，
        第一行,
        第二行
效果：

    这是多行文本效果，
    第一行,
    第二行

***
    
    语法2：文本前后添加三个反引号```，```独占一行
    如：
    ```
    我是段落，
    段落2，
    段落3，
    ```
效果：
```
这是多行文本效果，
第一行,
第二行
```
引用代码块语法也是用三个```,见[代码块](#代码块)

  我们可以看到Markdown文档转换为html文档后文本块就是`<pre><code>我是文本块</code></pre>`标签
### 标题
#### 标题(Atx形式)
    语法：在行首插入1-6个#，#后面加一个空格，对应1-6阶标题，字体大小从大到小
    如：
    # 标题1
    ## 标题2
    ### 标题3
    #### 标题4
    ##### 标题5
    ###### 标题6
效果：
# 标题1
## 标题2
### 标题3
#### 标题4
##### 标题5
###### 标题6

#### 分级标题(Setext形式)
    语法：在文字底部添加一行=或者-，最少一个
    如：
    一级标题
    ===============
    二级标题
    ----------------
效果：

一级标题
===============
二级标题
----------------

### 文字高亮(行内标记)
    语法：能使行内部分文字高亮，或将多行变成一行并高亮，使用一对反引号``
    如：`System.out.println()`用于向控制台输出信息
效果：`System.out.println()`用于向控制台输出信息
### 横线
    语法：三个***或者---或者___可以显示横线效果,必须独占一行才有效果

效果：  

`***`
***
`---`

---
`___`
___

### 换行
```
直接回车不能换行，可以在一行文本后面加2个空格+回车，就可以让下一行文本换行，或者在前面加一个空行，不过这种换行行间距有点大。
如：
我是第一行[空格]+[空格]+[回车]我是第二行
```
效果：  
我是第一行  
我是第二行

### 文本效果
#### 斜体、粗体、删除线
   语法 | 效果
--------|:-------:
`*斜体1*`|*斜体1*
`_斜体2_`|_斜体2_
`**粗体1**`|**粗体**
`__粗体2__(注意2个_)`|__粗体2__
`~~删除线~~`|~~删除线~~
`***粗体+斜体1***`|***粗体+斜体1***
`___粗体+斜体2___`|___粗体+斜体2___
`__*粗体+斜体3*__`|__*粗体+斜体3*__
`~~***粗体斜体删除线***~~`|~~***粗体斜体删除线***~~
Z<sup>a</sup>`Z<sup>a</sup>`|Z<sup>a</sup>
Z<sub>a</sub>`Z<sub>a</sub>`|Z<sub>a</sub>

    提示：斜体、粗体、删除线可混合使用

#### 支持内嵌CSS样式
    如：<p style="color: #AD5D0F;font-size: 30px; font-family: '宋体';">内联样式</p>
效果：<p style="color: #AD5D0F;font-size: 30px; font-family: '宋体';">内联样式</p>
  在github中，内嵌CSS样式貌似不起效果
### 引用
#### 单层嵌套
    语法：在行首添加 >字符，多行引用可以只在第一行添加。
    如：>android    
        >java    
        >高等数学 或者
                     >android
                     java
                     高等数学

效果：
>android    
>java    
>高等数学
#### 多层嵌套
    语法：
        >java基础
        >>基本数据类型
        >>>byte,int,long,double,char,String,boolean,array
效果：

>java基础   
>>基本数据类型  
>>>byte,int,long,double,char,String,boolean,array 

### 代码块
    语法：在三个反引号后面加上编程语言的名字，另起一行开始写代码，最后一行再加上三个反引号。

代码：
    
    ```
    public static void main(String[] args){}
    ```
效果1(和首行一个缩进或4个空格效果一样)：
 ```
public static void main(String[] args){}
 ```

代码：

    ```c
    int main(int arg1,char *arg[])
    ```
效果2(c代码块)：

```c
int main(int arg1,char *arg[])
```

代码：

    ```java
    public static void main(String[] args){}
    ```
效果3(java代码块)；
```java
public static void main(String[] args){}
```

### 序列
#### 无序序列
    语法：*或- + 空格就可以显示无序序列效果,使用tab缩进可以实现嵌套效果。
        * 中国
            * sfs
                * sfs
        - 美国
        * 日本
效果：

* 中国
    * sfs
        * sfs
- 美国
* 日本
#### 有序序列
    语法：数字.空格 实现有序序列效果，也可以多级嵌套。
    注意：.前面只能是数字。
    1. 主题
        1. 确定主题，思路清晰 
    2. 大纲
        1. 确定文章层次结构
    3. 举例
        1. 使用例子使观点更清晰易懂
    4. 说明
    5. 结论
效果：
1. 主题
    1. 确定主题，思路清晰 
2. 大纲
    1. 确定文章层次结构
3. 举例
    1. 使用例子使观点更清晰易懂
4. 说明
5. 结论
#### 复选框序列
    语法：有些平台不支持，兼容性一般
        - [x] 需求分析
        - [x] 系统设计
        - [x] 详细设计
        - [ ] 编码
        - [ ] 测试
        - [ ] 交付
效果：
- [x] 需求分析
- [x] 系统设计
- [x] 详细设计
- [ ] 编码
- [ ] 测试
- [ ] 交付

### 链接
#### 外部链接

|语法|效果|
|----|----|
|`[百度](http://www.baidu.com/ "悬停显示"){:target="_blank"}`|[百度](http://www.baidu.com/ "悬停显示")|

```
也可以使用引用的方式

语法：[标题][引用]
如：
[百度][baidu]

定义名称为baidu的引用
[baidu]:http://www.baidu.com/ "百度"
```
效果：  
[百度][baidu]

[baidu]:http://www.baidu.com/ "百度"

```
注：{:target="_blank"}跳转方式兼容性一般 ，多数第三方平台不支持跳转
```
#### 本地链接
    语法：[标题](本地路径)
    如：
        [demo](demo.txt)
[demo](demo.txt)  
     
### 插入图片
    基本语法：![alt](URL "title")
    alt和title即对应HTML中的alt和title属性，都可以省略.
    alt:表示图片显示失败时的替换文本
    title表示鼠标悬停在图片时的显示文本（注意这里要加引号）
    URL:即图片的url地址，如果引用本仓库中的图片，直接使用相对路径就可了，如果引用其他github仓库中的图片要注意格式，即：仓库地址/raw/分支名/图片路径。
    如：https://github.com/guodongxiaren/ImageCache/raw/master/Logo/foryou.gif

|#|语法|效果|
|----|----|----|
|1|`![百度](http://www.baidu.com/img/bdlogo.gif "百度logo")`|![百度](http://www.baidu.com/img/bdlogo.gif "百度logo")|
|2|`![][baiduImage]`|![baiduImage]|

>[baiduImage]的定义：
`[baiduImage]:http://www.baidu.com/img/bdlogo.gif "百度logo"`

[baiduImage]:http://www.baidu.com/img/bdlogo.gif "百度logo"

#### 控制图片大小
##### 方式一：使用html标签
    <img src="http://www.baidu.com/img/bdlogo.gif" width = "50" height = "50" alt="百度" align=center />
效果：  
<img src="http://www.baidu.com/img/bdlogo.gif" width = "50" height = "50" alt="百度" align=center />
##### 方式二：有些markdown编辑器支持设置大小
```
Mou中支持写法：![test image size](url){:height="100px" width="400px"}
其他编辑器：![](http://www.baidu.com/img/bdlogo.gif =100x100)
```

### 图片链接
    语法：普通链接和插入图片可以混合使用，即图片链接
|#|语法|效果|
|----|----|----|
|1.全写|`[![简书](https://cdn2.jianshu.io/assets/web/nav-logo-4c7bbafe27adc892f3046e6978459bac.png "简书")](https://www.jianshu.com/)`|[![简书](https://cdn2.jianshu.io/assets/web/nav-logo-4c7bbafe27adc892f3046e6978459bac.png "简书")](https://www.jianshu.com/)|
|2.图片简写|`[![简书][jianshu]](https://www.jianshu.com/)`|[![简书][jianshu]](https://www.jianshu.com/)|
|2.图片简写|`[![jianshu]](https://www.jianshu.com/)`|[![jianshu]](https://www.jianshu.com/)|
|3.图片和链接都简写|`[![jianshu]][link-jianshu]`|[![jianshu]][link-jianshu]|

>[jianshu]和[link-jianshu]的定义：  
`[jianshu]:https://cdn2.jianshu.io/assets/web/nav-logo-4c7bbafe27adc892f3046e6978459bac.png
[link-jianshu]:https://www.jianshu.com/`

[link-jianshu]:https://www.jianshu.com/
[jianshu]:https://cdn2.jianshu.io/assets/web/nav-logo-4c7bbafe27adc892f3046e6978459bac.png

### 锚点
    语法：每个标题都是锚点,即：[title](#锚点)
    注意：标题中的英文字母都被转化为小写字母了
效果：[回到底部](#参考)
### 表格
    语法：单元格用||包裹，:表示对齐方式，:与|之间不要有空格，否则有兼容问题。必须要有---------|--------|---------才有效果。
    github中markdown表格前面必须有空行才有效果
    |表头1-1|表头1-2|表头1-3|
    |---------|--------|---------|
    |单元个2-1|单元格2-2|单元格2-3|
效果：  

|表头1-1|表头1-2|表头1-3|
|--------|--------|---------|
|单元个2-1|单元格2-2|单元格2-3|
    或简写：
    表头1-1|表头1-2|表头1-3
    ---------|--------|---------
    单元个2-1|单元格2-2|单元格2-3

效果：

表头1-1|表头1-2|表头1-3
---------|--------|---------
单元个2-1|单元格2-2|单元格2-3

    对齐方式：默认左对齐(--),左对齐：:--,居中对齐：:--:,右对齐：--:
    如：
    | a | b | c | 
    |:-------:|:-------------| ----------:| 
    | 居中 | 左对齐 | 右对齐 | 
    |=========|===============|============|
效果：

| a | b | c | 
|:-------:|:-------------| ----------:| 
| 居中 | 左对齐 | 右对齐 | 
|=========|===============|============|

    特殊表格：一般对合并单元格，以及其它特殊格式表格，Markdown无能为力，一般做法是使用HTML标签
在线生成HTML代码网站[Tables Generator](http://www.tablesgenerator.com/html_tables)  

### diff语法
    语法：
    ```diff
    + 鸟宿池边树，僧敲月下门
    - 鸟宿池边树，僧推月下门
    ```
效果：
```diff
+ 鸟宿池边树，僧敲月下门
- 鸟宿池边树，僧推月下门
```
## 参考
[Github Flavored Markdown语法介绍](https://github.com/guodongxiaren/README#%E5%9B%BE%E7%89%87%E9%93%BE%E6%8E%A5)  
[Markdown 语法说明(简体中文版)_小众软件](https://www.appinn.com/markdown/)  
[Markdown 常用语法笔记](https://ouweiya.gitbooks.io/markdown/index.html)    
[Markdown 语法整理大集合2017](https://www.jianshu.com/p/b03a8d7b1719)
