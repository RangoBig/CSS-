# CSS全面学习

# 课程内容

> HTML 和CSS基础知识

1. html元素的分类和特性
2. html元素的默认样式和定制化
3. CSS选择器全解析
4. CSS常见属性逐一讲解

> CSS布局实战

1. 布局属性和组合解析
2. 常见布局方案介绍
3. 三栏布局案例
4. 国内大站布局方案解析

> 动画和效果专题讲解

1. 多背景多投影特效
2. 3D特效编写实践
3. 过渡动画和关键帧动画实践
4. 动画细节和原理深入解析

> 框架集成和CSS过程化

1. 预处理器作用和原理
2. Less和Sass代码实践
3. Bootstrap原理和用法
4. CSS过程化实践方式
5. JS框架中的CSS集成实践

## 1.0 CSS常见面试问题

![image-20220217035255042](https://gitee.com/rango007/pic-md1/raw/master/20220217035255.png)

![image-20220217035328486](https://gitee.com/rango007/pic-md1/raw/master/20220217035328.png)

## 2.0 课程目标

![image-20220217121003234](https://gitee.com/rango007/pic-md1/raw/master/20220217121003.png)

# 第1章 HTML常见元素和理解

- 前端三大件:
  - HTML结构
  - CSS样式
  - JavaScript行为

- HTML常见元素和理解
- HTML版本
- HTML元素分类
- HTML元素嵌套关系
- HTML元素默认样式和定制化
- HTML面试真题解答

> head区域的元素,

1. meta
2. title
3. style
4. link
5. script
6. base

> body中的元素

- div/section/article/aside/header/footer
- p
- span/em/strong
- table/thead/tbody/tr/td
- ul/ol/li/dl/dt/dd
- a
- form/input/select/textarea/button

![image-20220217121743209](https://gitee.com/rango007/pic-md1/raw/master/20220217121743.png)

> HTML重要属性

1. a[href,target]
2. img[src,alt]
3. table td[colspan,rowspan] `colspan`是“column span（跨列）”的缩写。**`colspan`属性用在td标签中，用来指定单元格横向跨越的列数**：**`rowspan`的作用是指定单元格纵向跨越的行数**。
4. form[target,method,enctype]
5. input[type,value]
6. button[type]
7. select > option[value]
8. label[for]

> 当多个多选框的name相同的时候,表示他们是一组的,
>
> label和input通过id关联起来

## 1.0 如何理解HTML

- HTML"文档"
- 描述文档的"结构"
- 有区块和大纲

> 使用语义化的标签就是为了让html结构更加清晰

> h5o - HTML5 Outliner大纲工具
>
> http://h5o.github.io/

## 2.0 HTML版本问题

- HTML4/4.01(SGML)
- XHTML(XML)
- HTML5

![image-20220217151404166](https://gitee.com/rango007/pic-md1/raw/master/20220217151404.png)

> 可以使用W3C验证网站,验证网页的合理性

![image-20220217151833204](https://gitee.com/rango007/pic-md1/raw/master/20220217151833.png)

## 3.0 HTML5新增的内容

- 新区块标签 
- section
- article
- nav
- aside

> 表单新增内容

- 表单增强input新增了一些类型
- 日期,时间,搜索
- 表单验证: 通过require
- Placeholder 自动聚焦

> HTML新增语义:
>
> 语义化标签的作用,会进大纲算法

- header/footer头尾
- section/article区域
- nav导航
- aside不重要内容
- em/strong强调
- i  icon 用它做图标

> HTML新增语义

## 4.0 HTML面试真题

1. doctype的意义是什么?

> IE将会以标准模式渲染.
>
> - 让浏览器以标准模式进行渲染
> - 让浏览器知道元素的合法性

2. HTML和XHTML HTML5的关系

> HTML属于SGML(非常通用的标记语言)
>
> XHTML属于XML,是HTML进行XML严格化的结果
>
> HTML5不属于SGML或XML.比XML宽松

3.HTML5有什么变化

> - 新的语义化元素,<article>、<section>、<aside>、<hgroup>、 <header>,<footer>、<nav>、<time>、<mark>、<figure> 和<figcaption>等
> - 表单增强
> - 新的API(离线,音视频,图形.实时通信,本地存储,设备能力)

4. em和i有什么区别

   1. em是语义化的标签,表示强调
   2. i是纯样式的标签,表斜体
   3. HTML5中i基本废除了.一般作为图标

5. 语义化的意义是什么?

   1. 开发者容易理解
   2. 机器容易理解(搜索,读屏,软件)
   3. 有助于SEO
   4. semantic.microdata

6. 哪些元素可以自闭合

   1. 表单元素input
   2. 图片img
   3. br hr
   4. meta link

7. HTML和DOM的关系

8. property和attribute的区别

   ***\*注意，不同点一：存在dom对象中的位置不一样，一个是作为dom对象的属性，而且在attributes属性对应的对象里面也同样存在，而另一个只存在dom对象的attributes属性对应的对象中\****

   ***\*注意，不同点二：property的值会同步html上的属性值，而且attributes里面的值只能通过代码进行修改，可以理解为attributes里面的数据时初始化数据\****

   注意，不同点三:property的值页面显示的值双向绑定，而attributes里面的值不会，而且半单向绑定，因为只有初始化时候的值会绑定到attributes里面。
   也有一个共同点，就是通过代码修改的不管是property还是attributes里面的值，都没有办法影响到对方。
   **attributes 是 HTML元素（标签）的属性，而 properties 是 DOM 对象的属性。**

   *prop（）和attr（）的区别：*

   - prop（）prop()针对的是DOM元素的property，而不是元素节点的attribute。 
     可以看出源码中使用的是elem[name]的形式，即对DOM对象属性的获取和设置方式。
   - attr（）设置的是HTML元素的特性，，源码中使用的也是setAttribute（）和getAttribute（），即用于操作特性的方法。

9. form的作用有哪些

   1. 直接提交表单
   2. 使用submit/reset按钮
   3. 便于浏览器保存表单
   4. 第三方库可以整天提取值
   5. 第三方库可以进行表单验证

## 6.0 HTML5语义化标签

**简洁的DOCTYPE：**

HTML5 只有一个简单的文档类型：<!DOCTYPE html>，表示浏览器会按照标准模式解析。

**简单易记的编码类型:**

你现在可以在meta 标签中使用”charset”：<meta charset=”utf-8″ />

**脚本和链接无需type:**

```
<link rel="stylesheet" href="path/to/stylesheet.css" /><script src="path/to/script.js"></script>
```

**更加语义化的新增标签:**

比如说：<article>、<section>、<aside>、<hgroup>、 <header>,<footer>、<nav>、<time>、<mark>、<figure> 和<figcaption>等

**视频和音频:**

```
<video 
width="640" height="320" preload="auto" poster="0.jpg" controls>    
<source src="movie.ogg" type="video/ogg" />    <source 
src="movie.mp4" type="video/mp4" />    Your browser does not support 
the video tag.</video>
```

**表单增强:**

新的input类型：color, email, date, month, week, time, datetime, datetime-local, number,range,search, tel, 和url

新属性：required, autofocus, pattern, list, autocomplete 和placeholder

新元素：<keygen>, <datalist>, <output>, <meter> 和<progress>

canvas标签绘制2D图形。

```
var
 canvas = document.getElementById('canvas');var context = 
canvas.getContext('2d');context.beginPath;context.moveTo(100,100);context.lineTo(300,300);context.lineTo(100,500);context.lineWidth
 = 5;context.strokeStyle = "red";context.stroke;
```

**地理位置获取**

**HTML语义化**

**1.什么是HTML语义化？**

通过标签判断内容语义，例如根据h1标签判断出内容是标题，根据<p>判断内容是段落、<input>标签是输入框等。

**2.为什么要语义化？**

1).去掉或样式丢失的时候能让页面呈现清晰的结构

2).方便其他设备解析（如屏幕阅读器、盲人阅读器、移动设备）以意义的方式来渲染网页

3).有利于SEO

4).便于团队开发和维护，遵循W3C标准，可以减少差异化

**3.如何确定你的标签是否语义良好？**

去掉样式，看网页结构是否组织良好有序，是否仍然有很好的可读性。

**4.常见的语义化标签模块**

表单

```
<form
 action="" method="">    <fieldset style="border: none">       
 <legend style="display: none">登录表单</legend>        
<p><label for="name">账号：</label><input type="text" 
id="name"></p>        <p><label 
for="pw">密码：</label><input type="password" 
id="pw"></p>        <input type="submit" name="登录" 
class="subBtn">    </fieldset></form>
```

表单域要用fieldset标签包起来，并用legend标签说明表单的用途；每个input标签对应的说明文本都需要使用label标签，并且通过为input设置id属性，在lable标签中设置for=someld来让说明文本和相对应的input关联起来。

**5.语义化标签应注意的一些问题**

尽可能少的使用无语义的标签div和span；

在语义不明显时，既可以使用div或者p时，尽量用p, 因为p在默认情况下有上下间距，对兼容特殊终端有利；

不要使用纯样式标签，如：b、font、u等，改用css设置。

需要强调的文本，可以包含在strong或者em标签中，strong默认样式是加粗（不要用b），em是斜体（不用i）



# 第2章 CSS基础

![image-20220218020049456](https://gitee.com/rango007/pic-md1/raw/master/20220218020049.png)

> 浏览器解析选择器的方式是从右往左解析,一步一步进行验证,处于效率的模式进行考虑

## 1.0 选择器分类

- 元素选择器 a{}
- 伪元素选择器::before{}
- 类选择器.link{}
- 属性选择器[type=radio]{}
- 伪类选择器 :hover{}
- ID选择器 #id{}
- 组合选择器 [type=checkbox] +label{}
- 否定选择器 :not(.link){}
- 通用选择器 *{}



## 2.0 选择器权重

- ID选择器 #id{} +100
- 类 属性 伪类 +10
- 元素 伪元素 +1
- 其他选择器 +0
- !import优先级最高
- 元素属性,优先级最高
- 相同权重,后写的生效

## 非布局样式

- 字体,字重,颜色,大小,行高
- 背景,边框
- 滚动,换行
- 粗体,斜体,下划线
- 其他



## 3.0 非布局样式-字体

- 字体族
  - serif sans-serif monospace cursive fantcy
  - 多字体fallback
  - 网络字体,自定义字体
  - iconfont

## 4.0 非布局样式-行高

- 行高的构成
- 行高相关的现象和方案
- 行高的调整

> 行高不一样的时候,为什么渲染高度是一样的,
>
> `line boxes`什么特性也没有，就高度。所以一个没有设置`height`属性的`div`的高度就是由一个一个`line boxes`的高度堆积而成的。其实`line boxes`不是直接的生产者，属于中层干部，真正的活儿都是它的手下 – `inline boxes`干的，这些手下就是文字啦，图片啊，`<span>`之类的`inline`属性的标签啦。`line boxes`只是个考察汇报人员，考察它的手下谁的实际`line-height`值最高，谁最高，它就要谁的值，然后向上汇报，形成高度。例如，`<span style="line-height:20px;">取手下line-height<span style="line-height:40px;">最高</span>的值</span>`。则line boxes的高度就是40像素了。

<font color="red" size=5>行高的构成是怎么来的?行高是line-box决定的,line-box是由什么组成的,是由inline-box组成的</font>

> 行高相关的现象和方案

1. 可以使用line-height设置居中
2. 在单行或多行或图片垂直居中实现上的应用

![在这里插入图片描述](https://gitee.com/rango007/pic-md1/raw/master/20220303013335.png)

3. 文字默认是基线对齐,如果居中对齐,可以设置一个vertical-align

## 5.0 非布局样式-背景

> - 背景颜色
> - 渐变色背景
> - 多背景的叠加
> - 背景图片和属性(雪碧图)
> - base64和性能优化
> - 多分辨率适配

> 1.0 颜色格式

==0deg不是按我们数学的角度向右定义的，默认方向是向上的，是从方向北开始的，所以北才是0deg，==

![img](https://gitee.com/rango007/pic-md1/raw/master/20220303152102.png)



```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>background</title>
    <style>
      body {
        background: yellow;
      }
      .c1 {
        height: 90px;
        /* background: red; */
        background: url(../test.png);
      }
      .c2 {
        height: 90px;
        /* 设置一个线性渐变 */
        /* background: -webkit-linear-gradient(left, red, green, blue); */
        /* 线性渐变最新写法, to right */
        /* background: linear-gradient(to right, red, green, blue); */
        /* 对于渐变,我们更多的时候会使用一个角度的值 */
        /* background: linear-gradient(45deg,red, green, blue) */
        /* 线性渐变,还可以使用百分比来规定颜色区域 */

        /* background: linear-gradient(135deg, red 0, green 10%, blue 50%) */
        /* 多背景的叠加,如何画一道绿线 */
        background: linear-gradient(
          135deg,
          transparent 0,
          transparent 49.5%,
          green 49.5%,
          green 50.5%,
          transparent 50.5%,
          transparent 100%
        ),linear-gradient(
          45deg,
          transparent 0,
          transparent 49.5%,
          red 49.5%,
          red 50.5%,
          transparent 50.5%,
          transparent 100%
        );
        background-size:30px 30px;
      }
    </style>
  </head>
  <body>
    <div class="c1"></div>
    <div class="c2"></div>
  </body>
</html>

```

<font color="red" size=5>背景图片和属性(雪碧图)</font>

> 所以聪敏的开发者想出来把所有的动作图片合成成一张图片，这样只要加载一次就能全速在内存中读取了。后来的游戏机还为此专门搞了一个处理器来加速Sprite资源，就好象3d加速卡一样。现在的游戏机性能提高了，但是2d游戏还是保留了这样的技术。
>
> 因为雪碧的英文名叫做 Sprite，这种图标文件英文名是 Sprites，所以就有雪碧图的叫法了。因为http请求每次都要握手，时间开销很，所以借鉴了Sprite技术，把一些零碎的图片素材合成成一张图片，这样只要一次请求就能把图片资源加载完成了。但是这个技术在http2和http3中就不一定那么有效果了，因为新的协议中会合并请求，所以Sprite技术没有那么节约了。最后也要合理使用，太大得雪碧图也会造成加载缓慢的情况

## 6.0 非布局样式-边框

> - 边框的属性:线型 大小 颜色
> - 边框背景图
> - 边框衔接 (三角形)

> 1.0 边框背景图
>
> css中repeat 和 round 的区别
>
> round平铺图像的方式与repeat一样，不过不会裁剪图像。背景图不会被裁剪，而是被缩放。并排着一列列显示。为了做到这一点，浏览器会扭曲各个图像副本，因此会破坏图像的纵横比。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>border</title>
    <style>
        /* 边框是如何处理图片
            可以拉伸图片
        */
        .c1{
            width: 400px;
            height: 200px;
            border: 5px dashed red;
        }
        .c2{
            width: 400px;
            height: 200px;
            /* border-width: 30px; */
            border: 30px solid transparent;
            border-image: url(../border.png) 30 repeat;
        }
    </style>
</head>
<body>
    <div class="c1"></div>
    <div class="c2"></div>
</body>
</html>
```

> 2.0 边框的衔接部分使用的切面
>
> 我们可以使用边框部分的真实,使用css画出一个三角形,跳转角的度数我们还可以画出来一个扇形



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>border</title>
    <style>
        /* 边框是如何处理图片
            可以拉伸图片
        */
        .c1{
            width: 400px;
            height: 200px;
            border: 5px dashed red;
        }
        .c2{
            width: 400px;
            height: 200px;
            /* border-width: 30px; */
            border: 30px solid transparent;
            border-image: url(../border.png) 30 round;
        }
        .c3{
            /* 如何使用css设置一个三角形,利用边框,左右边框链接部分为边,设置透明
            然后再设置div盒子模型的宽度为0,边框就会压缩为一个
            */
            width: 0px;
            height: 200px;
            border-bottom: 30px solid red;
            border-right: 30px solid transparent;
            border-left: 30px solid transparent;
        }
    </style>
</head>
<body>
    <div class="c1"></div>
    <div class="c2"></div>
    <div class="c3"></div>
</body>
</html>
```

## 7.0 非布局样式-滚动

![image-20220304012607180](https://gitee.com/rango007/pic-md1/raw/master/20220304012607.png)



## 8.0 非布局样式-文本折行

> 文档折行和滚动相似的是,都面临的问题是显示不下,
>
> - overflow-wrap(word-wrap)通用换行控制
>   - 是否保留单词
> - word-break针对多字节文字
> - 中文句子也是单词
> - white-space空白处是否断行

## 9.0 非布局样式-装饰性属性

> - 字重(粗体)font-weight
> - 斜体font-style:italic
> - 下划线text-decoration
> - 指针cursor





## 10.0 hack和案例

> ### 什么是CSS hack
>
> 由于不同厂商的流览器或某浏览器的不同版本（如IE6-IE11,Firefox/[Safari](https://so.csdn.net/so/search?q=Safari&spm=1001.2101.3001.7020)/Opera/Chrome等），对CSS的支持、解析不一样，导致在不同浏览器的环境中呈现出不一致的页面展现效果。这时，我们为了获得统一的页面效果，就需要针对不同的浏览器或不同版本写特定的CSS样式，我们把这个针对不同的浏览器/不同版本写相应的CSS code的过程，叫做CSS hack!

![image-20220303144909399](https://gitee.com/rango007/pic-md1/raw/master/20220303144909.png)

> 1. Hack即不合法但生效的写法
> 2. 主要用于区分不同浏览器
> 3. 缺点:难理解,难维护,易失效
> 4. 替代方案:特性检测
> 5. 替代方案:针对性加class

##  第二章-CSS真题面试题
> 选择器的真题
> 1. CSS样式(选择器)的优先级
> 2. 计算权重确定
> 3. !importtant
> 4. 内联样式
> 5. 后写的优先级高

> 雪碧图的作用
>
> - 利用background属性,大小位置,background-position
> - 减少HTTP请求数,提高加载性能
> - 有一些情况下可以减少图片大小

> 自定义字体的使用场景
>
> 1. 宣传/品牌/banner等固定文案
> 2. 字体图标

> base64的使用
>
> 1. 用于减少HTTP请求
> 2. 适用于图片
> 3. base64的体积约为原图4/3

> 伪元素和伪类的区别
>
> 1. 伪类表状态
> 2. 伪元素是真的有元素
> 3. 前者单冒号,后者双冒号



> 如何美化checkbox
>
> 1. label[for]和id
> 2. 隐藏原生的input
> 3. :checked+label

# 第3章 CSS布局

## 1.0 布局简介

> 1. CSS知识体系的重中之重
> 2. 早期以table为主(简单)
> 3. 后来以技巧性布局为主(难)
> 4. 现在有flexbox/grid(偏简单)
> 5. 响应式布局是必备知识

<font color="red" size=5>常用布局方法</font>

> 1. table表格布局
> 2. float浮动 + margin
> 3. inline-block布局
> 4. flexbox布局



1.直接使用table进行布局,和利用div的display属性进行布局

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>display</title>
    <style>
      .left {
        background: red;
      }
      .right {
        background: blue;
      }
      table {
        width: 800px;
        height: 200px;
        /* 为表格设置合并边框模型 */
        border-collapse: collapse;
      }
      /* 开始设置div的table布局 */
      /* 1.0 先设置外部盒子 */
      .table {
          margin-top: 20px;
          display: table;
          width: 800px;
          height: 200px;
      }
      .table-row{
          display: table-row;
      }
      .table-cell{
          /* vertical-align 属性设置元素的垂直对齐方式。 */
          vertical-align: center;
          display: table-cell;
      }
    </style>
  </head>
  <body>
    <table>
      <tr>
        <td class="left">左</td>
        <td class="right">右</td>
      </tr>
    </table>
    <!-- 使用div设置table布局 -->
    <div class="table">
      <div class="table-row">
        <div class="left table-cell">左</div>
        <div class="right table-cell">右</div>
      </div>
      <div class="table-row">
        <div class="left table-cell">左</div>
        <div class="right table-cell">右</div>
      </div>
    </div>
  </body>
</html>
 
```

![image-20220305001443144](https://gitee.com/rango007/pic-md1/raw/master/20220305001443.png)

## 2.0 一些布局属性

![image-20220305003222379](https://gitee.com/rango007/pic-md1/raw/master/20220305003222.png)

>  display/positon
>
> 1. 确定元素的显示类型
> 2. block/inline/inline-block
> 3. 确定元素的位置
> 4. static/relative/absolute/fixed

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>position</title>
    <style>
        /* 默认就是静态布局,按照文档流 */
        div{
            background:red;
            width: 100px;
            height: 100px;
        }
        /* 相对定位,相对于元素本身来说,不会因为布局而改变空间的计算 */
        .p2{
            position: relative;
            left: 10px;
            top: 20px;
            background:blue;
        }
        /* 绝对定位,已经脱离了文档流,独立存在
            relative相对于body定位
            absolute相对于最近的一个父级absolute或者relative
            如果不是就往上找,一直找到body
        */
        .p3{
            position: absolute;
            left: 80px;
            top: 30px;
            background:green;
        }
        /* 相对于可视屏幕是固定的 */
        .p4{
            background:yellow;
            position:fixed;
            left: 0;
            bottom: 1px;
        }
    </style>
</head>
<body>
    <div class="p1">
        position:static
    </div>
    <div class="p2">
        position:relative
    </div>
    <div class="p3">
        position:absolute
    </div>
    <div class="p4">
        position:fixed
    </div>
    <div class="p5">
        p5
    </div>
    
</body>
</html>
```

> 使用z-index可以改变层叠顺序,使用样的元素可以使用z-index,定位属性为:relative,absolute,fixed

## 2.0 flexbox

> 1. 弹性盒子
> 2. 盒子本来就是并列
> 3. 指定宽度即可
>
> 没有比大规模使用,适用性弱

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>flex_02</title>
    <style>
        .container{
            width: 800px;
            height: 200px;
            display: flex;
        }
        /* 左边两百,右边自适应 */
        .left{
            background: red;
            display: flex;
            width: 200px;
        }
        .right{
            background: blue;
            display: flex;
            flex: 1;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="left">
            左
        </div>
        <div class="right">
            右
        </div>
    </div>
</body>
</html>
```

## 3.0 float布局

> 1. 元素"浮动"
> 2. 脱离文档流
> 3. 但不脱离文本流
> 4. 本来就是做图文混排文字环绕效果的
>
> ==float有什么特效==<font color="red" size=5>float对自身的影响</font>
>
> 1. 对自身影响:
>    1. 会形成块BFC
>    2. 位置会尽量靠上
>    3. 位置尽量靠左(右)

![image-20220305192927436](https://gitee.com/rango007/pic-md1/raw/master/20220305192927.png)

```
块格式化上下文（Block Formatting Context，BFC） 是Web页面的可视CSS渲染的一部分，是块盒子的布局过程发生的区域，也是浮动元素与其他元素交互的区域。
```

![image-20220305220005258](https://gitee.com/rango007/pic-md1/raw/master/20220305220005.png)

> <font color="red" size=5>float对兄弟的影响</font>
>
> - 对兄弟的影响
> - 上面贴非float元素
> - 旁边贴float元素
> - 不影响其他块级元素位置
> - 影响其他块级元素内部文本



> <font color="red" size=5>float对父级的影响</font>
>
> 1. 从父级布局上消失了
> 2. 父级高度有可能会塌陷

<font color="red" size=5>如何解决父元素塌陷的问题</font>

> 1. overflow:auto

浮动的布局怎么做?

## 4.0 inline-block

- 像文本一样排block元素
- 没有清除浮动等问题
- 需要清除间隙

> 同学你好，造成空白间隙的原因是在标签和标签之间使用了空格或换行符， 因为空白字符也是字符，也会引用CSS样式。而这个距离就是以字体大小为准的，所以当设置为0的时候，表示这几个空格符的字体大小也是0，就像我们文字设置为0，不显示一样，所以这里也不显示了哦。
>
> 希望能帮助到你，祝学习愉快！
>
> ==所以我们不换行的话,就不会有空隙了==



## 5.0 响应式布局

> 1. 在不同设备上正常使用
> 2. 一般主要处理屏幕大小问题
> 3. 主要方法:
>    1. 隐藏 + 折行 + 自适应空间
>    2. rem/viewport/media query
> 4. 还可以使用脚本动态的获取页面大小,

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>响应式布局</title>
    <style>
        .container {
            margin: 0 auto;
            max-width: 800px;
            display:flex;
            border: 1px solid #000;
        }
        /* 左边 */
        .left{
            display:flex;
            width: 200px;
            background: red;
            margin: 5px;
        }
        .right{
            display:flex;
            flex: 1;
            background:blue;
            margin: 5px;
        }
        /* 自适应 */
        @media (max-width: 640px) {
            .left{
                display:none;
            }

        }
    </style>
</head>
<body>
    <div class="container">
        <div class="left">
            的了子求国始洪后世是，互长陈牛白，害人。
        </div>
        <div class="right">
            之尘持人范感同音使骂王罚之感帅，意一的吞少同自巴太绛就他过他着愿不，留司皇有生洞德，收不不笔了搏，案惜招的登恩哥畴种国，县卧秦文天心仓杂制劝何对娟氏，说但他是若是念的第要命木锐责你由，人弟洪丑，览衣尝自大人韩高皮变嗣沫娘，却三台活如始而说骨骂怒巴来艳对我临彷，的的不的国人主县世颜，后光得褒丰罪，治苦国不挟，因年啦没沫婵是送守她皇六极因与是，甲重将九司不廿，满才且丰一锐貂洪无大光，韩我人的，联己派。
        </div>
    </div>
</body>
</html>
```

> 使用rem做适配的方法,可以根据不同的设备给他不同html:font-size的值就可以让他的大小进行随意缩放,
>
> 而且在指定rem的时候,范围大的放在上面,范围小的放在下面
>
> rem的单位不一定很精确
>
> 

## 6.0 主流网站使用的布局方式

> 大多数使用的都是float布局,所以我们应该掌握float布局规则



## 7.0 CSS面试真题

1. 使用两栏(三栏)布局的方法
   1. 表格布局display:table
   2. float + margin布局
   3. inline-block布局
   4. flexbox布局(兼容性)

2. position:absolute / fixed有什么区别?
   1. 前者是相对于最近的absolute/relative
   2. 后者相对屏幕(viewport)
3. display:inline-block的间隙
   1. 原因就是:字符间距
   2. 解决:解决字符或者消灭间距
4. 如何清除浮动(浮动的元素不会占据父元素的布局空间,也就是父元素布局的时候不回去管浮动元素,有可能浮动元素会超出浮动元素,从而对其他的元素造成影响)
   1. 让盒子负责自己的布局(强制让盒子来管理)
   2. overflow:hidden(auto)
   3. ::after{clear:both}为了让父元素一定包含浮动元素
5. 如何适配移动端页面
   1. 需要适配viewport页面宽度要和移动端的宽度适配
   2. rem viewport media query
   3. 设计上; 隐藏 折行 自适应

# 第4章 CSS效果属性

- box-shadow 投影
- text- shadow文本投影
- border-radius  圆角
- background 背景
- clip-path
- 

## 4.1 box-shadow

```html
box-shadow: 
h-shadow 水平阴影,允许负值
v-shadow 垂直阴影 允许负值
blur 模糊距离
spread 阴影大小
color 阴影颜色
inset;从外层的阴影(开始时)改变阴影内侧阴影
```

![image-20220306173900434](https://gitee.com/rango007/pic-md1/raw/master/20220306173900.png)

> 1. 营造层次感(立体感)
> 2. 充当没有宽度的边框
> 3. 特殊效果



## 4.2 text-shadow

> - 立体感
> - 印刷品质感

```css
text-shadow: h-shadow v-shadow blur color;
注意： text-shadow属性连接一个或更多的阴影文本。属性是阴影，指定的每2或3个长度值和一个可选的颜色值用逗号分隔开来。已失时效的长度为0。
```

| 值         | 描述                                |
| :--------- | :---------------------------------- |
| *h-shadow* | 必需。水平阴影的位置。允许负值。    |
| *v-shadow* | 必需。垂直阴影的位置。允许负值。    |
| *blur*     | 可选。模糊的距离。                  |
| *color*    | 可选。阴影的颜色。参阅 CSS 颜色值。 |

## 4.3 border-radius

> - 圆角矩形
> - 圆形
> - 半圆 / 扇形 
> - 一些奇奇怪怪的角

## 4.4 background

> 1. 多个背景是可以叠加的
> 2. 纹理,图案
> 3. 渐变
> 4. 雪碧动画
> 5. 背景图尺寸适应

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .container{
        }
        .i{
            width: 20px;
            height: 20px;
            background: url(./background.png) no-repeat;
            background-size: 20px 40px;
            transition: background-position .1s;
        }
        .i:hover{
            background-position: 0 -20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="i"></div>
    </div>
</body>
</html>

```

## 4.5clip-path

> 1. 对容器进行裁剪
> 2. 常见几何图形
> 3. 自定义路径裁剪

## 4.6 3D变换

![image-20220307123510350](https://gitee.com/rango007/pic-md1/raw/master/20220307123510.png)

> 1. translate 位移
> 2. scale 2D缩放
> 3. skew  定义沿着 X 和 Y 轴的 2D 倾斜转换。
> 4. rotate 

![image-20220307190525770](https://gitee.com/rango007/pic-md1/raw/master/20220307190525.png)











## 4.7 如何用一个div画xxx

1.box-shadow无限投影

- ::before
- ::after

2.如何产生不占空间的边框

> 1. box-shadow
> 2. outline
>
> outline（轮廓）是绘制于元素周围的一条线，位于边框边缘的外围，可起到突出元素的作用。
>
> outline简写属性在一个声明中设置所有的轮廓属性。
>
> 可以设置的属性分别是（按顺序）：outline-color, outline-style, outline-width
>
> 如果不设置其中的某个值，也不会出问题，比如 outline:solid #ff0000; 也是允许的。

## 4.8 如何实现圆形元素(头像)

border-radius:50%

## 4.9 如何实现ios图标的圆角

![image-20220307125732112](https://gitee.com/rango007/pic-md1/raw/master/20220307125732.png)

## 4.10 如何实现半圆,扇形等图形

> border-radius组合
>
> - 有无边框
> - 边框粗细
> - 圆角半径



## 4.11 如何实现背景图居中显示/ 不重复/改变大小

> - background-position
> - background-repeat
> - background-size(cover/contain)



## 4.12 如何平移/放大一个元素

- transform:translateX(100px)
- transform:sacle(2)

## 4.13 如何平移/放大一个元素

- transform:translateX(100px)
- transform:scale(2)

transform 属性向元素应用 2D 或 3D 转换。该属性允许我们对元素进行旋转、缩放、移动或倾斜。

为了更好地理解 transform 属性，请查看这个[演示](https://www.w3school.com.cn/example/css3/demo_css3_transform.html)。

## 4.14 如何实现3D效果

> 1. perspective:500px
> 2. transform-style:preserve-3d
> 3. transform:translate rote...

# 第5章 CSS动画

> 动画的原理:
>
> 1. 视觉暂留作用
> 2. 画面逐渐变化

![image-20220307182712328](https://gitee.com/rango007/pic-md1/raw/master/20220307182712.png)

![image-20220307195545418](https://gitee.com/rango007/pic-md1/raw/master/20220307195545.png)

![image-20220307195606929](https://gitee.com/rango007/pic-md1/raw/master/20220307195607.png)

![image-20220307195645653](https://gitee.com/rango007/pic-md1/raw/master/20220307195645.png)

<font color="red" size=5>CSS中的动画类型</font>

> 1. transition补间动画( 有开头有结尾中间的部分是补出来的)
> 2. keyframe关键帧动画(动画部分也是关键帧,但是可以状态转换)
> 3. 逐帧动画

## 5.1 补间动画

补间动画就是指控制最开始的状态和最末的状态的动画，中间的状态由浏览器自动帮我们计算生成。

![image-20220307214259995](https://gitee.com/rango007/pic-md1/raw/master/20220307214300.png)

![image-20220307215846086](https://gitee.com/rango007/pic-md1/raw/master/20220307215846.png)

![image-20220307220649198](https://gitee.com/rango007/pic-md1/raw/master/20220307220649.png)





> 可以自己设置曲线

![image-20220307225345605](https://gitee.com/rango007/pic-md1/raw/master/20220307225345.png)

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>transition</title>
    <style>
      .container {
        width: 100px;
        height: 100px;
        background: red;
        /* 过渡 */
        transition: all 1s;
        /* 延迟属性 */
        /* transition-delay: .5s; */
        /* 我们可以自己调整动画进度和时间的关系 */
        transition-timing-function: 
        ease-in
        ;
      }
      .container:hover {
          width: 800px;
          background: green;

      }
    </style>
  </head>
  <body>
    <div class="container"></div>
  </body>
</html>

```

## 5.2 关键帧动画

![image-20220307225520194](https://gitee.com/rango007/pic-md1/raw/master/20220307225520.png)

```
css3动画之@keyframes关键帧
css3新增属性@keyframes（关键帧），可以帮助开发者不必依赖JavaScript，只使用css代码完成动画制作。

@keyframes创建动画的原理是：将一套 CSS 样式逐渐变化为另一套样式，在动画过程中，可以多次改变这套 CSS 样式，以百分比来规定改变发生的时间，或者通过关键词 "from" 和 "to"，等价于 0% 和 100%。

注意，@keyframes的兼容性如下：
目前浏览器都不支持 @keyframes 规则
Firefox 支持替代的 @-moz-keyframes 规则
Opera 支持替代的 @-o-keyframes 规则
Safari 和 Chrome 支持替代的 @-webkit-keyframes 规则

```



> 过渡动画一定要有状态的变更,keyframe是不需要这个状态的变更
>
> 进度是可控制的
>
> 



## 5.3 逐帧动画

> transition,和keyframe

![image-20220308005723642](https://gitee.com/rango007/pic-md1/raw/master/20220308005723.png)

> 逐帧动画适用于什么样的场景哪?适用于动画的面积比较小,动画时长不是太大 ,我们可以循环使它的时长很大,

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      .container {
        width: 100px;
        height: 100px;
        border: 1px solid red;
        background: url(../animal.png) no-repeat;
        animation:run 1s infinite;
        /* 可以实现动画静止 ,steps主要就是设置
            
        */
        animation-timing-function: steps(1);
      }
      /* 每一帧都是12.5%,一共八帧
        但是关键帧动画中间会有过渡,
      */
      @keyframes run {
          0%{
              background-position: 0 0;
          }
          12.5%{
              background-position: -100px 0;
          }
              25%{
                background-position: -200px 0;
            }
            37.5%{
                background-position: -300px 0;
            }
            50%{
                background-position: 0 -100px;
            }
            62.5%{
                background-position: -100px -100px;
            }
            75%{
                background-position: -200px -100px;
            }
            87.5%{
                background-position: -300px -100px;
            }
            100%{
                background-position: 0 0;
            }
      }
    </style>
  </head>
  <body>
    <div class="container"></div>
  </body>
</html>

```

## 5.4 面试真题

> css中动画怎么写?使用transition和animation(动画)

1.CSS动画的实现方式有几种

> - transition
> - keyframes(animation)

2.<font color="red" size=5>过渡动画和关键字动画的区别</font>

> - 过渡动画需要有状态变化
> - 关键帧动画不需要状态变化
> - 关键帧动画能控制更精细

3.<font color="red" size=5>如何实现逐帧动画</font>

> 使用关键帧动画,去掉补间(steps)



<font color="red" size=5>4.CSS动画的性能</font>

> 1. 性能不坏
> 2. 部分情况下优于JS
> 3. 但JS可以做到更好
> 4. 部分高危属性
>    1. box-shadow

# 第6章 预处理器

## 6.1  介绍

- 基于CSS的另一种语言
- 通过工具编译成css
- 添加了很多css不具备的特性
- 能提升css文件的组织方式



> less 

![image-20220308111513410](https://gitee.com/rango007/pic-md1/raw/master/20220308111513.png)

<font color="red" size=5>CSS处理器到底解决了什么东西?</font>

> - 嵌套 反映层级和约束
> - 变量和计算,减少重复代码
> - Extend和Mixin代码片段
> - 循环 适用于复杂有规律的样式
> - import CSS文件模式化
> - 

