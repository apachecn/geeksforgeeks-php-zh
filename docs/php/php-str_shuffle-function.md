# PHP|str_shashffle()函数

> Original: [https://www.geeksforgeeks.org/php-str_shuffle-function/](https://www.geeksforgeeks.org/php-str_shuffle-function/)

**str_ashffle()**函数是 PHP 中的一个内置函数，用于随机搅乱作为参数传递给函数的字符串的所有字符。 当传递一个数字时，它将该数字视为字符串并对其进行混洗。 此函数不会对原始字符串或作为参数传递给它的数字进行任何更改。 相反，它返回一个新字符串，该字符串是在参数中传递给它的字符串的可能排列之一。

**语法：**

```php
str_shuffle($string) 
```

**参数：**此函数接受单个参数$STRING。 参数*$string*指定需要对其字符进行混洗的字符串。 除了字符串，还可以传递数字。 如果传递的是数字而不是字符串作为参数，则此函数会将该数字视为字符串。

**返回值**：该函数返回一个长度相同的字符串，但其内部包含混洗字符。 每次执行程序时，它都会显示不同的输出，因为字符的洗牌每次都是不同的。 在某些情况下，原始字符串或数字可以是返回值。

例如：

```php
Input : $string = "raj" 
Output : jar 

Input : $string = "geeks" 
Output : eeksg 

Input : $string = 142 
Output : 412 

Note: The output will be different on every execution. 

```

下面的程序说明了 str_shashffle()函数：

**程序 1：**传递字符串时演示 str_ashffle()函数的程序。

```php
<?php
// PHP program to demonstrate the str_shuffle()
// function when a string is passed
$string = "geeks"; 

// prints the shuffled string 
echo str_shuffle($string);
?>
```

产出：

```php
keegs
```

**程序 2：**在传递数字时演示 str_ashffle()函数的程序。

```php
<?php
// PHP program to demonstrate the str_shuffle()
// function when a number is passed
$string = 142; 

// prints the shuffled string 
echo str_shuffle($string);
?>
```

产出：

```php
124
```

**参考**：
[http://php.net/manual/en/function.str-shuffle.php](http://php.net/manual/en/function.str-shuffle.php)