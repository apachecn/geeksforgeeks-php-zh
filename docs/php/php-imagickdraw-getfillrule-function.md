# PHP|ImagickDraw getFillRule()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getfillrule-function/](https://www.geeksforgeeks.org/php-imagickdraw-getfillrule-function/)

**ImagickDraw：：getFillRule()函数**是 PHP 中的一个内置函数，用于获取绘制多边形时使用的填充规则。

**语法：**

```php
*int* ImagickDraw::getFillRule( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回与[FILLRULE 常量](https://www.php.net/manual/en/imagick.constants.php/#imagick.constants.fillrule-undefined)之一对应的整数值。

下面给出了 FILLRULE 常量列表：

*   Imagick：：FILLRULE_UNDEFINED(0)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   ==同步，由 Elderman 更正==@ELDER_MAN

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**ImagickDraw：：getFillRule()函数**：

**程序 1：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the Fill Rule
$fillRule = $draw->getFillRule();
echo $fillRule;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the Fill Rule
$draw->setFillRule(2);

// Get the Fill Rule
$fillRule = $draw->getFillRule();
echo $fillRule;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickdraw.getfillrule.php](https://www.php.net/manual/en/imagickdraw.getfillrule.php)