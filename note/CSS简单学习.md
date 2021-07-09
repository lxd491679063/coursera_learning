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

   

