# PHP|ReflectionExtension export()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-export-function/](https://www.geeksforgeeks.org/php-reflectionextension-export-function/)

**ReflectionExtension：：Export()函数**是 PHP 中的一个内置函数，用于在返回参数设置为 true 时以字符串形式返回导出，否则返回 NULL。

**语法：**

```
*string* ReflectionExtension::export( *string* $name,
 *string* $return )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$name：**此参数保存反射的导出。
*   **$return：**此参数保存布尔值。 如果它的值设置为 True，则它将导出反映的扩展。 如果其值设置为 False，则不会导出反映的扩展名。

**返回值：**如果返回参数设置为 true，则此函数以字符串形式返回导出，否则返回 NULL。

下面的程序演示了 PHP 中的 ReflectionExtension：：Export()函数：

**程序 _1：**

```
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the export() function
$B = $extension->export($A, $return = FALSE);

// Getting the export as a string 
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

> 扩展[<persistent>扩展#18 DOM 版本 20031129]{</persistent>
> 
> -依赖关系{
> 依赖关系[libxml(必需)]
> 依赖关系[domxml(冲突)]
> }
> 
> -常量[45]{
> 常量[整数 XML_ELEMENT_NODE]{1}
> 。 。 。
> 常量[整数 DOM_VALIDATION_ERR]{16}
> }
> 。 。 。
> 。 。 。
> -参数[3]{
> 参数#0[<必填>$expr]
> 参数#1[<可选>DOMNode 或 NULL$Context]
> 参数#2[<可选>$registerNodeNS]
> }
> }
> 
> 方法[<dom>公共方法 registerPhpFunctions]{</dom>
> 
> -Parameters[0]{
> }
> }
> }
> }
> }
> }
> 
> 无约束力的 / 无效的

**程序 _2：**

```
<?php

// Using ReflectionExtension() over 
// a extension xml
$extension = new ReflectionExtension('xml');

// Calling the export() function and
// Getting the export as a string 
var_dump($extension->export('xml', $return = TRUE));
?>
```

**Output:**

> String(6209)“Extension[<persistent>Extension#15 XML 版本 7.0.33-0ubuntu0.16.04.7]{</persistent>
> 
> -依赖项{
> 依赖项[libxml(必需)]
> }
> 
> ...。 ...。 ...
> 
> 函数[<xml>函数 UTF8_DECODE]{</xml>
> 
> -参数[1]{
> 参数#0[<必需的>$DATA]
> }
> }
> }
> }
> “

**引用：**[https://www.php.net/manual/en/reflectionextension.export.php](https://www.php.net/manual/en/reflectionextension.export.php)