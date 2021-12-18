# PHP|IntlChar：：charAge()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharcharage-function/](https://www.geeksforgeeks.org/php-intlcharcharage-function/)

**IntlChar：：charAge()**函数是 PHP 中的一个内置函数，用于计算代码点的年龄。 其中，年龄是首次指定或分配字符时的 Unicode 版本。 这对于避免向不接受较新字符的进程发出代码点非常有用。

**语法：**

```php
*array* IntlChar::charAge( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数是字符或整数值，编码为*UTF-8*字符串。

**返回值：**在 true 情况下，*$codepoint*返回数组的 Unicode 版本号。

下面的程序演示了 PHP 中的**IntlChar：：charAge()**函数。

**程序 1：**

## PHP

```php
<?php
// PHP code to illustrate IntlChar::charAge()
// function

// Input int codepoint value
var_dump(IntlChar::charage("\u{2025}"));
echo "<br>";

// Input character codepoint value
var_dump(IntlChar::charage("\u{1F878}"));
echo "<br>";

// Input int codepoint value
var_dump(IntlChar::charage("\u20"));
echo "<br>";

// Input character codepoint value
var_dump(IntlChar::charage("Geeks"));
echo "<br>";

?>
```

发帖主题：Re：Колибри0.7.0

```php
array(4) { [0]=> int(1) [1]=> int(1) [2]=> int(0) [3]=> int(0) } 
array(4) { [0]=> int(7) [1]=> int(0) [2]=> int(0) [3]=> int(0) } 
NULL 
NULL 
```

**程序 2：**

## PHP

```php
<?php
// PHP code to illustrate IntlChar::charAge()

// Declare an array $arr
$arr = array("^", "2345", "6", "\n");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::charage($val));
    echo "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
array(4) { [0]=> int(1) [1]=> int(1) [2]=> int(0) [3]=> int(0) } 
NULL 
array(4) { [0]=> int(1) [1]=> int(1) [2]=> int(0) [3]=> int(0) } 
array(4) { [0]=> int(1) [1]=> int(1) [2]=> int(0) [3]=> int(0) } 
```

**相关文章：**

*   [IntlChar：：isalpha()函数](https://www.geeksforgeeks.org/php-intlcharisalpha-function/)
*   [IntlChar：：isbase()函数](https://www.geeksforgeeks.org/php-intlcharisbase-function/)
*   [IntlChar：：isBlank()函数](https://www.geeksforgeeks.org/php-intlcharisblank-function/)
*   [IntlChar：：iscntrl()函数](https://www.geeksforgeeks.org/php-intlchariscntrl-function/)

**引用：**[http://php.net/manual/en/intlchar.charage.php](http://php.net/manual/en/intlchar.charage.php)