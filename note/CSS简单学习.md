# CSS简单学习

> 学习CSS的目的

1. 美化网页
2. 网页动画(特效效果)

> 难点 + 重点 CSS选择器

## 1.CSS基本

### 1.1 什么是CSS

Cascading Style Sheet 层叠级联样式表

css:表现

字体、颜色、边距、高度、宽度、背景图片、网页定位、网页浮动

### 1.2 发展史

CSS 1.0

CSS 2.0 DIV + CSS , HTML 与 CSS 分离，网页变得简单 易于SEO

CSS 2.1 浮动，定位

CSS 3.0 圆角，阴影，动画... 浏览器兼容

### 1.3 快速入门

> 做个简单的文件分离

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Lesson1</title>
    <link rel="stylesheet" href="./css/style.css">
</head>
<body>
    <h1>Hello world!</h1>
</body>
</html>
```



```css
/*style.css*/
h1{
    color:#ff0000;
}
```

样式卸载css文件里

结构写在html文件里

CSS文件每一个样式结尾记得用;

#### css的优势

```bash
1.内容和表现分离
2.网页结构表现统一，可以直接复用
3.样式十分丰富
4.利用SEO，容易被搜索引擎收录
```

### 1.4 CSS的三种导入方式

1. 行内样式
2. 内部样式
3. 外部样式

优先级是就近原则，行内样式最高，其次汗内部样式和内部样式哪个先载入

- 链接式

  ```html
  <link rel="stylesheet" href="./css/style.css">
  ```

  

- 导入式

  ```html
      <style>
          @import url("css/style.css");
      </style>
  ```

  

## 2.选择器

> 作用，选择页面上的某一个或者某一类元素

### 2.1 基本选择器

1. 标签选择器

   ```html
   会影响所有标签类 优先级最低
   h1{
   
   }
   ```

2. 类选择器 class

   ```html
   class 属性，可以复用，优先级高于标签选择器
   .classname{
   
   }
   ```

3. id选择器 id

   ```html
   id属性，全局唯一,优先级最高
   #idname{
   
   }
   ```

   

### 2.2 层次选择器

1. 后代选择器（在某个元素后面所有的后代元素）
2. 子选择器（一代节点）
3. 相邻兄弟选择器
4. 通用选择器

```html
html 文件

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>层次选择器</title>
    <link rel="stylesheet" href="./css/style_2_2.css">
</head>
<body>
<p>P1</p>
<p class="brother">P2</p>
<a class="brother">P3</a><br/>
<a>A1</a>
<ul>
    <li>
        <p>P4</p>
    </li>
    <li>
        <p>P5</p>
    </li>
    <li>
        <p>P6</p>
    </li>
</ul>
</body>
</html>
```

```css
/*p{*/
/*    background: greenyellow;*/
/*}*/

/*后代选择器，选择某个节点之后所有后代类中对应元素*/
/*body li{*/
/*    background: red;*/
/*}*/

/*子选择器 该节点后的一代节点*/
/*body>p{*/
/*    background: yellow;*/
/*}*/

/*相邻兄弟节点 只有邻近的同辈节点，且是该节点的下一个节点*/
/*.brother + p{*/
/*    background: blue;*/
/*}*/

/*这种隔了一隔元素就不是相邻了*/
/*.brother + a{*/
/*    background: pink;*/
/*}*/

/*通用选择器 相邻兄弟加上自己一起应用样式*/
.brother~a{
    background: antiquewhite;
}
```

### 2.3 结构伪类选择器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>结构伪类选择器</title>
    <style>
        /*ul第一个子元素*/
        /*ul li:first-child{*/
        /*    background: aqua;*/
        /*}*/

        /*!*ul最后一个子元素*!*/
        /*ul li:last-child{*/
        /*    background: bisque;*/
        /*}*/

        /*每个结构里 第一个p的父类下的第一个元素，必须同样是p才能生效0*/
        p:nth-child(1){
            background: green;
        }

        /*每个结构第一个p元素 其父节点下地n个P元素*/
        p:nth-of-type(1){
            background: orange;
        }
    </style>
</head>
<body>
<p>P1</p>
<p class="brother">P2</p>
<a class="brother">P3</a><br/>
<a>A1</a>
<ul>
    <li>
        <p>P4</p>
    </li>
    <li>
        <p>P5</p>
    </li>
    <li>
        <p>P6</p>
    </li>
</ul>
</body>
</html>
```

### 2.4 属性选择器(常用)

标签[属性]{}

标签[属性=？]{} //绝对等于

标签[属性*=？]{} //包含即可

标签[属性^=？]{} //以什么开头

标签[属性$=？]{} //以什么结尾

属性可以用正则匹配

## 美化网页元素

### 3.1美化网页

```bash
span 标签
<span></span> 重点内容用span套起来
```

### 3.2 字体样式

```css
body{
    font-family:"Arial Black",楷体;	//字体
    color:yellow;					//字体颜色
}
h1{
    font-size:50px;	//字体大小
}
.p1{
    font-weight:bolder; //字体粗细
}
```

### 3.3 文本样式

```css
h1{
    color:#FFFFFF; //颜色
    text-align:center;//布局，位置
    test-indent:2em; //首行缩进
    height:500px; //高度
    line-height:100px;行高
    text-decoration: underline/line-through/overline/none;
}
img,span{
    vertical-align: middle;
}
a:hover{ //悬停状态
    color
}
a:active{ //激活状态，鼠标点击未取消
    
}
a:visited{
    
}
```

