# HTML详解

## 一、基本标签

### 1.<!DOCTYPE html>

声明解析格式

### 2.<html></html>

网页主题

### 3.<head></head>

头部

#### 3.1<meta> 

一般用来做SEO

#### 3.2 <title></title>

网页标题

### 4.<body></body>

网页的具体内容

#### 4.1<h1></h1> ……<h6></h6>

一级标签~六级标签

#### 4.2 <p></p>

段落标签,可以保持文本格式

#### 4.3 <br>(自闭和标签，单标签)

换行标签

#### 4.4 <hr>

水平线标签

#### 4.5 <strong></strong>   粗体

#### 4.6 <em></em> 斜体

#### 4.7 &nbsp (特殊符号)空格 &gt、&lt （大于、小于）,&copy （版权所有）

#### 4.8 <! -- comment content --> （注释）

#### 4.9 <img src="" alt="替代文字" title="悬停文字" width="300" height="300">

#### 4.10 <a herf='https://www.baidu.com'>点击跳转</a> 连接标签 

```bash
<a herf='www.baidu.com'></a>
嵌套其他元素
<a herf=""> 
<img src="" alt="替代文字" title="悬停文字" width="300" height="300">
</a>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>a标签</title>
</head>

<!--
可以嵌套在其他元素的外层
href 写明要跳转的链接
target:跳转方式
    _blank  新建页面
    _self   当前页面打开

锚链接 href 中 使用#

-->

<body>
    <a href="https://www.baidu.com">第一个链接</a>
    <a href="first_test.html" target="_blank">链接网页</a>
    <a href="first_test.html" target="_blank">
        <img src="../res/召合技能书.png" alt="test2" title="xuanting">
    </a>
    <br/>
    <a href="img_idx.html#top" target="_blank">锚链接top测试</a>
    <br/>
    <a href="img_idx.html#down" target="_self">锚链接down测试</a>
</body>
</html>
```



> <strong>列表</strong>

```bash
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>List Study</title>
</head>
<body>
    <!--
     有序列表
     -->
    <ol>
        <li>test1</li>
        <li>test1</li>
        <li>test1</li>
        <li>test1</li>
        <li>test1</li>
    </ol>
    <hr/>
    <!--
     无序列表
     -->
    <ul>
        <li>unorder 1</li>
        <li>unorder 1</li>
        <li>unorder 1</li>
        <li>unorder 1</li>
        <li>unorder 1</li>
    </ul>
    <hr/>
    <!--
     自定义列表
     dl 标签
     dt 列表题目
     dd 列表内容
     -->
    <dl>
        <dt>第一个标题</dt>
        <dd>第一组内容</dd>
        <dd>hah</dd>
        <dd>xixi</dd>
        <dd>heihie</dd>

        <hr/>

        <dt><a href="https://www.baidu.com" target="_blank">去百度吧</a>第二个标题</dt>
        <dd>test2</dd>
        <dd>test3</dd>
        <dd>test4</dd>
    </dl>
    <hr/>
</body>
</html>
```

> <strong>表格标签</strong>

```bash
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Table Study</title>
</head>
<body>
    <!--
    <table> 表格
    <tr></tr> 行 colspan夸列
    <td></td> 列 rowspan 跨行
    -->

    <table name="成绩" border="1px">
        <tr>
            <td colspan="3">1</td>
        </tr>
        <tr>
            <td rowspan="2">ORICAL</td>
            <td>语文</td>
            <td>3</td>
        </tr>
        <tr>
            <td>数学</td>
            <td>3</td>
        </tr>
        <tr>
            <td rowspan="2">JARRY</td>
            <td>语文</td>
            <td>99</td>
        </tr>
        <tr>
            <td>数学</td>
            <td>200</td>
        </tr>
    </table>
</body>
</html>
```

> 媒体元素

```bash
视频元素 video
音频元素 audio

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>媒体元素标签</title>
</head>
<body>
    <!--
    video 视频
    src:资源路径
    controls：控制条
    autoplay:自动播放
    -->
    <video src="../res/video/class-11.mp4" controls autoplay></video>
    <br/>
    <!--
        audio 音频
        src:资源路径
        controls：控制条
        autoplay:自动播放
        -->
    <video src="../res/music/逆相思.mp3" controls autoplay></video>
</body>
</html>
```

> 页面结构分析

```bash
header 表示头部
footer 标记脚部区域
section web页面中的独立区域
article 独立文章内容
aside 相关内容或应用(侧边栏)
nav 导航类辅助内容
```

> 内联框架

```bash
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>iframe内联框架</title>
</head>
<body>
<!--
    iframe
    src : 路径
    name : frame_name
    width : 宽度
    height : 高低
-->
<!--<iframe src="//player.bilibili.com/player.html?aid=55631961&bvid=BV1x4411V75C&cid=97257967&page=11" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>-->

    <iframe src="https://www.baidu.com" name="hello" width="1000px" height="800px"></iframe>
    <a href="https://exmail.qq.com/cgi-bin/frame_html?sid=20s_0rFhDsQif1Y2,7&sign_type=&r=d5a81bd3ff0b4890e08febdf25d9db32" target="hello">点击跳转</a>
</body>
</html>
```

> <strong>表单</strong>

```bash
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>form 表单标签</title>
</head>
<body>
<!--
    form
    action:
    method:post,get 提交方式 get url上显示，高效，post在url上不显示提交内容，但是也可以查询到，可以传输大文件
-->
<h1>注册</h1>
<form action="first_test.html" method="post">
    <p name="passport">账号 <input type="text" name="username"></p>
    <p>密码 <input type="password" name="pwd"></p>
    <p>
        <input type="submit">
        <input type="reset">
    </p>
</form>

</body>
</html>
```

> input

```bash
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>input 输入框组件</title>
</head>
<body>
<!--
input
type:指定类型
｛text,password,checkbox,radio,submit,reset,file,hidden,image,button,默认text｝
name:元素名称
value:元素初始值 (type 为radio时必须指定初始值
size:表单元素初始宽度
maxlength:类型为text和password时的最大字符数
checkd:type 为radio 或 checkbox时，指定按钮是否被选中

require 必须填写
placeholder 占位符
pattern 正则匹配
-->

<h1>注册</h1>
<form action="first_test.html" method="get">
    <p name="passport">账号 <input type="text" name="username" value="用户名" maxlength="12" size="30" placeholder="请输入用户名" required></p>
    <p>密码 <input type="password" name="pwd" size="30" maxlength="12" required></p>
<!--    单选框 -->
    <p> 想要多少钱：<br/>
        <input type="radio" value="100" name="money"/>100<br/>
        <input type="radio" value="200" name="money"/>200<br/>
        <input type="radio" value="300" name="money"/>300<br/>
    </p>
    <p> 按钮 <br/>
        <input type="button" name="test_btn" value="测试按钮">
        <input type="image" src="../res/img/召合技能书.png" size="30"/>
    </p>
    <p>
        多选框 <br/>
        <input type="checkbox" name="select_1" value="吃饭">吃饭<br/>
        <input type="checkbox" name="select_2" value="睡觉">睡觉<br/>
        <input type="checkbox" name="select_3" value="打豆豆">打豆豆<br/>
        <input type="checkbox" name="select_4" value="蹭吃">蹭吃<br/>
    </p>
    <p>
        聚餐选择 <br/>
        <input type="checkbox" name="eat_1" value="火锅">火锅<br/>
        <input type="checkbox" name="eat_2" value="烤肉">烤肉<br/>
        <input type="checkbox" name="eat_3" value="海底捞">海底捞<br/>
        <input type="checkbox" name="eat_4" value="弄堂里">弄堂里<br/>
    </p>

    <p>
        国家：<br/>
        <select name="country" id="1001">
            <option value="china">中国</option>
            <option value="USA">美国</option>
            <option value="Switzerland" selected>瑞士</option>
            <option value="Canada">加拿大</option>
        </select>
    </p>

    <p>
        <textarea name="reply" id="1002" cols="100" rows="10" value="文本内容">test3</textarea>
    </p>

    <p>
        <input type="file" value="文件" name="upload_file" required>
    </p>

<!--    URL 验证 -->
    <p>
        链接：
        <input type="url" name="upload_url">
    </p>

   <p>
       邮箱：
       <input type="email" name="upload_email" id="email_label"/>
   </p>

    <p>
        搜
        <input type="search" name="search_text">
    </p>

    <p>
        自定义邮箱：<input type="text" name="diy_email" placeholder="***@***.***" pattern="^\w+([-+.]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$"/>
    </p>

<!--    滑块   -->
    <p>
        音量：<input type="range" name="audio_num" value="10" max="100" min="0"/>
    </p>

    <p>
        <label for="1001">点一下试试</label>
    </p>
    
    <p>
        <input type="submit">
        <input type="reset">
    </p>
</form>

</body>
</html>
```

