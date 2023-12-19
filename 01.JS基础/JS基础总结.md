# JavaScript总结篇

[TOC]

## 1）用法

### 1> `<head>`中的JS

```html
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
</script>
</head>
<body>
<h1>我的 Web 页面</h1>
<p id="demo">一个段落</p>
<button type="button" onclick="myFunction()">尝试一下</button>
</body>
</html>
```

### 2>`<body>`中的JS

```html
<!DOCTYPE html>
<html>
<body>
<h1>我的 Web 页面</h1>
<p id="demo">一个段落</p>
<button type="button" onclick="myFunction()">尝试一下</button>
<script>
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
</script>
</body>
</html>
```

### 3>外部的JS

​	可以把脚本保存到外部文件中。外部文件通常包含被多个网页使用的代码。

​	外部 JavaScript 文件的文件扩展名是 .js。

​	如需使用外部文件，请在 `<script>` 标签的 "src" 属性中设置该 .js 文件：

```html
<!DOCTYPE html>
<html>
<body>
<script src="myScript.js"></script>
</body>
</html>
```

​	可以将脚本放置于 `<head>` 或者 `<body>`中，放在 `<script>` 标签中的脚本与外部引用的脚本运行效果完全一致。

​	myScript.js 文件代码如下：

```javascript
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
```

​	注意：外部脚本不能包含 `<script>` 标签。

## 2）输出

​	JavaScript 没有任何打印或者输出的函数，但可以通过不同的方式来输出数据：

### 1>使用window.alert()

​	可以弹出警告框来显示数据：

```html
<!DOCTYPE html>
<html>
<body>
<h1>我的第一个页面</h1><p>我的第一个段落。</p>
	
<script>window.alert(5 + 6);
</script>

</body>
</html>
```

### 2>操作HTML元素

​	如需从 JavaScript 访问某个 HTML 元素，您可以使用 document.getElementById(*id*) 方法。

​	请使用 "id" 属性来标识 HTML 元素，并 innerHTML 来获取或插入元素内容：

```html
<!DOCTYPE html><html>
<body>

<h1>我的第一个 Web 页面</h1>

	<p id="demo">我的第一个段落</p>

<script>
	document.getElementById("demo").innerHTML = "段落已修改。";
</script>

</body>
</html>
```

​	**document.getElementById("demo")** 是使用 id 属性来查找 HTML 元素的 JavaScript 代码 。

​	**innerHTML = "段落已修改。"** 是用于修改元素的 HTML 内容(innerHTML)的 JavaScript 代码。
