CSS引入有三种方式：
- 外部样式表
- 内部样式表
- 内嵌样式

> 外部样式表

用link标签引入，在html文档头部引入，即head标签内引入，href属性定义样式文件url。

```html
<link rel="stylesheet" href="css/style.css" />
```

> 内部样式表

用style标签引入，和link引入方式一样，在head标签内引入。

```html
<style>
  body{
    margin: 0;
  }
</style>
```

> 内嵌样式

用标签的属性style引入，添加在要自定义样式的标签中，例如要给段落元素自定义样式：

```html
<p style="font-size: 14px;line-height: 20px;">这是一个段落。</p>
```
