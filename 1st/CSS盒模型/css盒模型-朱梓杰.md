#css盒模型
---
###一：简述
![模型图](https://www.runoob.com/images/box-model.gif)
>这些属性我们可以把它转移到我们日常生活中的盒子（箱子）上来理解。内容就是盒子里装的东西；而内边距就是物体和盒子内壁的距离；边框就是盒子本身；外边距则表实盒子和别的物体的距离

###二：两种盒模型
>W3C盒模型  box-sizing:content-box
>
>IE盒模型   box-sizing:border-box
>
>![两种盒模型](https://img-blog.csdn.net/20150629102231720)

###三：四种属性

```
div {
    width: 300px;
    border: 25px solid green;
    padding: 25px;
    margin: 25px;
}
```

1.margin（上右下左原则）

+ 简写属性

+ 单独设置


2.border

+ width：简写+单独（border-top-width）

+ style：简写+单独（border-top-style)

+ color:单独使用不起作用，必须配合style使用

3.padding（同margin）

4.content(width,height)
>当你指定一个css元素的宽度和高度时，你只是设置内容区域的宽度和高度

###四：一些相关知识点

1.外边距合并

![](https://www.w3school.com.cn/i/ct_css_margin_collapsing_example_1.gif)

2.边距重叠

>父元素没有设置margin-top，而子元素设置了margin-top：20px;可以看出，父元素也一起有了边距

![](https://images2017.cnblogs.com/blog/1265396/201711/1265396-20171119160218265-419904943.png)

>防止方法
触发BFC（块级格式化上下文）

>.浮动元素、inline-block 元素、绝对定位元素的 margin 不会和垂直方向上其他元素的 margin 折叠（注意这里指的是上下相邻的元素）

3.清除默认padding
>一些元素，默认带有padding，比如ul标签，所以我们为了方便控制，会选择清除

```
 *{
            margin: 0;
            padding: 0;
        }
```