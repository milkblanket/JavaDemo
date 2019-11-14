# GIT
- go to the target folder, both press "shift" and right click mouse, choose PowerShell
- get the whole list from the target folder
```
target path> LS
```
OR
```
target path> DIR
```
- initialize the target folder
```
git init
```
- add origin path remotely, path got after creating a new repository
```
git remote add origin https://github.com/milkblanket/JavaDemo.git
```
- get the status of repository before each pushing
```
git status
```
- add file/files
```
git add filename.filefomate
```
OR
```
git add .
```
- add commitment
```
git commit -m "comments"
```
- ATTENTION! THE MOST IMPORTANT ACTION!!! authenticate your github account
```
git push origin -u master
```
- change username
```
git config -l
git config --local user.name "xxxxx"
```










# Markdown Title
## Markdown Title
### Markdown Title
#### Markdown Title
##### Markdown Title
###### Markdown Title


First Level Title
=================

Second Level Title
-----------------



Paragraph One(Two blank)  
Paragraph Two

Paragraph One 
  
Paragraph Two

*italic*  
_italic_  
**Bold**  
__Bold__  
***Bold italic***  
___Bold italic___  


Separator; Divider; split line
***

* * *

*****

- - -

----------


~~Line-THROUGH~~

<u>Underline</u>

[^Footnote]failed?

1. Head1：
    - First line
    + Second line
2. Head2：
    * First line
    - Second line
    
> OUTEST
> > OUTER
> > > INSIDE  


> List in Block
> 1. First line
> 2. Second line
> + Third line




* First line
    > Block 1
    > Block 2
* Second line

`printf()` 函数



```javascript
$(document).ready(function () {
    alert('RUNOOB');
});
```

This is a link [菜鸟教程](https://www.runoob.com)

链接也可以用变量来代替，文档末尾附带变量地址：  
这个链接用 1 作为网址变量 [Google][1]  
这个链接用 runoob 作为网址变量 [Runoob][runoob]  
然后在文档的结尾为变量赋值（网址）  

  [1]: http://www.google.com/
  [runoob]: http://www.runoob.com/
  
  
  

![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png)  
  
![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png "RUNOOB")  

这个链接用 1 作为网址变量 [RUNOOB][1].  
然后在文档的结尾位变量赋值（网址）

[1]: http://static.runoob.com/images/runoob-logo.png

|  Header   | Header  |
|  ----  | ----  |
|  Cell  | Cell |
| Cell  | Cell |

| left justifying | right justifying | center aligned |
| :---| ---: | :---: |
| Cell | Cell | Cell |
| Cell | Cell | Cell |


1、横向流程图源码格式：

```mermaid
graph LR
A[方形] -->B(圆角)
    B --> C{条件a}
    C -->|a=1| D[结果1]
    C -->|a=2| E[结果2]
    F[横向流程图]
```
2、竖向流程图源码格式：

```mermaid
graph TD
A[方形] --> B(圆角)
    B --> C{条件a}
    C --> |a=1| D[结果1]
    C --> |a=2| E[结果2]
    F[竖向流程图]
```
3、标准流程图源码格式：

```flow
st=>start: 开始框
op=>operation: 处理框
cond=>condition: 判断框(是或否?)
sub1=>subroutine: 子流程
io=>inputoutput: 输入输出框
e=>end: 结束框
st->op->cond
cond(yes)->io->e
cond(no)->sub1(right)->op
```
4、标准流程图源码格式（横向）：

```flow
st=>start: 开始框
op=>operation: 处理框
cond=>condition: 判断框(是或否?)
sub1=>subroutine: 子流程
io=>inputoutput: 输入输出框
e=>end: 结束框
st(right)->op(right)->cond
cond(yes)->io(bottom)->e
cond(no)->sub1(right)->op
```
5、UML时序图源码样例：

```sequence
对象A->对象B: 对象B你好吗?（请求）
Note right of 对象B: 对象B的描述
Note left of 对象A: 对象A的描述(提示)
对象B-->对象A: 我很好(响应)
对象A->对象B: 你真的好吗？
```
6、UML时序图源码复杂样例：

```sequence
Title: 标题：复杂使用
对象A->对象B: 对象B你好吗?（请求）
Note right of 对象B: 对象B的描述
Note left of 对象A: 对象A的描述(提示)
对象B-->对象A: 我很好(响应)
对象B->小三: 你好吗
小三-->>对象A: 对象B找我了
对象A->对象B: 你真的好吗？
Note over 小三,对象B: 我们是朋友
participant C
Note right of C: 没人陪我玩
```
7、UML标准时序图样例：

```mermaid
%% 时序图例子,-> 直线，-->虚线，->>实线箭头
  sequenceDiagram
    participant 张三
    participant 李四
    张三->王五: 王五你好吗？
    loop 健康检查
        王五->王五: 与疾病战斗
    end
    Note right of 王五: 合理 食物 <br/>看医生...
    李四-->>张三: 很好!
    王五->李四: 你怎么样?
    李四-->王五: 很好!
```
8、甘特图样例：

```mermaid
%% 语法示例
        gantt
        dateFormat  YYYY-MM-DD
        title 软件开发甘特图
        section 设计
        需求                      :done,    des1, 2014-01-06,2014-01-08
        原型                      :active,  des2, 2014-01-09, 3d
        UI设计                     :         des3, after des2, 5d
    未来任务                     :         des4, after des3, 5d
        section 开发
        学习准备理解需求                      :crit, done, 2014-01-06,24h
        设计框架                             :crit, done, after des2, 2d
        开发                                 :crit, active, 3d
        未来任务                              :crit, 5d
        耍                                   :2d
        section 测试
        功能测试                              :active, a1, after des3, 3d
        压力测试                               :after a1  , 20h
        测试报告                               : 48h
```




