##### CSS基本语法：

```
选择器{
	属性声明=属性名:属性值;
  ......
}

selector{
	property1:value;
	property2:value;
	......
}
```

##### 浏览器私有属性
- Chrome，Safari：-webkit-
- Firefox：-moz-
- IE：-ms-
- Opera：-o-

##### 属性值语法

先看一个例子：

```
margin:[<length>|<percentage>|auto]{1,4}
```

> 基本元素

上面例子中，length,percentage,auto就是基本元素。

- 关键字：auto，solid，bold……
- 类型
  - 基本类型：<length>,<percentage>,<color>……
  - 其他类型：<'padding-width'>,<color-stop>……
  - 符号：/,
  - inherit,initial

> 组合符号

例子中[],|就是组合符号。

组合符号——空格
```
<'font-size'> <'font-family'> //空格前后的两个值都必须有，且顺序不能交换
```

组合符号——&&
```
<length>&&<color> //&&前后的两个值都必须有，顺序可以交换
```

组合符号——||
```
underline||overline||line-through||blink //这些属性值至少要出现一个，出现多个时顺序无要求
```

组合符号——|
```
<color>|transparent //两个属性值只能出现一个
```

组合符号——[]
```
bold[thin||<length>] //[]表示一个分组，可以把[]里面的看做是一个整体
```

> 数量符号

{1,4}:是数量符号，表示数量是：1个 <= 出现次数 <= 4个

数量符号——无
```
<length> //表示此基本元素只能出现一次
```

数量符号—— +
```css
<color-stop>[,<color-stop>]+ //+表示至少出现一次，也可以是多次
```

数量符号——?
```
inset?&&<color> //?表示可以出现也可以不出现，相当于可选
```

数量符号——{}
```
<length>{2,4} //{2,4}表示出现次数的范围
```

数量符号——*
```
<time>[,<time>]*  // *表示可以出现0次，1次或者多次
```

数量符号——#
```
<time># // #表示至少出现一次，也可以是多次，用逗号隔开
```

##### @规则语法

语法格式：@标识符 xxx;@标识符 xxx{}

```css
@import "subs.css";
@charset "utf-8";
@media print{
  body{
  font-size: 10pt;
  }
}
@keyframes fadein{
  0%{top:0;}
  50%{top:30px;}
  100%{top:0;}
}
@font-face{}
```
