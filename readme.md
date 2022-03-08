# Less,Sass预处理器教程

# 

# 1.0 CSS预处理器的介绍

> <font color="red" size=5>CSS预处理器</font>
>
> 1. 基于CSS的另一种语言
> 2. 通过工具编译成CSS
> 3. 添加了很多CSS不具备的特性
> 4. 能提升CSS文件的组织方式

<font color="red" size=5>CSS预处理器到底提供了哪些功能?</font>

> 1. 嵌套 反映层级和约束
> 2. 变量和计算,减少重复代码
> 3. Extend和Mixin代码片段
> 4. 循环 适用于复杂有规律的样式
> 5. import CSS文件模块化

# Nesting(嵌套)

##  less 嵌套

> 因为 Less 和 CSS 非常像，因此很容易学习。而且 Less 仅对 CSS 语言增加了少许方便的扩展，这就是 Less 如此易学的原因之一。

```cmd
//可以自动生成css文件
F:\vscode面试\less学习>lessc 1-nest.less >1-nest.css
```

```less
body{
    padding:0;
    margin:0;
}

.wrapper{
    background:white;

    .nav{
        font-size: 12px;
    }
    .content{
        font-size: 14px;
        &:hover{
            background:red;
        }
    }
}
=========================转换为css
body {
  padding: 0;
  margin: 0;
}
.wrapper {
  background: white;
}
.wrapper .nav {
  font-size: 12px;
}
.wrapper .container {
  font-size: 14px;
}
.wrapper .container:hover {
  background: red;
}

```

##  sass嵌套

> 两者的嵌套规则基本一样

<font color="red" size=5>

- `--style`表示解析后的`css`是什么排版格式;sass内置有四种编译格式:`nested``expanded``compact``compressed`。`--sourcemap`表示开启`sourcemap`调试。开启`sourcemap`调试后，会生成一个后缀名为`.css.map`文件</font>





#  变量（Variables）

> 二者的差别原因,在于理念不同,less的理念是接近css语法,css中也会使用@符号
>
> sass的理念在于,既然和css不是同一种语言,就尽量和css产生混淆

## less变量

无需多说，看代码一目了然：

```less
@width: 10px;
@height: @width + 10px;

#header {
  width: @width;
  height: @height;
}
```

编译为：

```css
#header {
  width: 10px;
  height: 20px;
}
```

## sass变量

### 变量 `$` (Variables: `$`)

SassScript 最普遍的用法就是变量，变量以美元符号开头，赋值方法与 CSS 属性的写法一样：

```scss
$width: 5em;
```

直接使用即调用变量：

```css
#main {
  width: $width;
}
```

变量支持块级作用域，嵌套规则内定义的变量只能在嵌套规则内使用（局部变量），不在嵌套规则内定义的变量则可在任何地方使用（全局变量）。将局部变量转换为全局变量可以添加 `!global` 声明：

```scss
#main {
  $width: 5em !global;
  width: $width;
}

#sidebar {
  width: $width;
}
```

编译为

```css
#main {
  width: 5em;
}

#sidebar {
  width: 5em;
}
```

#  混合（Mixins）

> 当我们需要一段代码进行复用的时候,可以使用less中的混合

## less混合

混合（Mixin）是一种将一组属性从一个规则集包含（或混入）到另一个规则集的方法。假设我们定义了一个类（class）如下：

```css
.bordered {
  border-top: dotted 1px black;
  border-bottom: solid 2px black;
}
```

如果我们希望在其它规则集中使用这些属性呢？没问题，我们只需像下面这样输入所需属性的类（class）名称即可，如下所示：

```less
#menu a {
  color: #111;
  .bordered();
}

.post a {
  color: red;
  .bordered();
}
```

`.bordered` 类所包含的属性就将同时出现在 `#menu a` 和 `.post a` 中了。（注意，你也可以使用 `#ids` 作为 mixin 使用。）

## sass混合

> 概念几乎和less一样,但是使用方法和less完全不同,定义sass混合指令需要用@mixin 

==定义混合指令 `@mixin` (Defining a Mixin: `@mixin`)==

混合指令的用法是在 `@mixin` 后添加名称与样式，比如名为 `large-text` 的混合通过下面的代码定义：

```scss
@mixin large-text {
  font: {
    family: Arial;
    size: 20px;
    weight: bold;
  }
  color: #ff0000;
}
```

混合也需要包含选择器和属性，甚至可以用 `&` 引用父选择器：

```scss
@mixin clearfix {
  display: inline-block;
  &:after {
    content: ".";
    display: block;
    height: 0;
    clear: both;
    visibility: hidden;
  }
  * html & { height: 1px }
}
```

