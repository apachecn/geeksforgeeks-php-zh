# PHP|strtr()函数

> Original: [https://www.geeksforgeeks.org/php-strtr-function/](https://www.geeksforgeeks.org/php-strtr-function/)

**strtr()**是 PHP 中的一个内置函数，用于将字符串中的子字符串替换为给定的字符串。 它还可以选择将特定单词更改为字符串中的不同单词。 该函数区分大小写。

**语法：**

```php
strtr($string, $string1, $string2) 

or,

strtr($string, $arr)

```

**参数：**此函数接受上述语法中所示的三个参数，如下所述：

1.  **$string：**它指定要进行替换的字符串。 这是必选参数。
2.  **$string 1：**如果出现在**$string**中，它指定必须替换的字符串。 如果未使用数组，则此参数为必选参数。
3.  **$string 2：**它指定要将**$string 1**的字符更改为的字符串。 如果未使用数组，则此参数为必选参数。
4.  **$arr：**我们可以将(**$string 1**和**$string 2**)或**$array**作为参数传递。 当我们想要更改任何特定的子字符串时，数组作为参数传递。 **$array**包含要更改的字符串和要更改的字符串。

**注意：**当**$STRIN1**和**$STRING 2**的长度不同时，较长的字符串将被格式化为较短的字符串的长度。

**返回值：**此函数的返回值取决于两种情况：

*   当**$STRIN1**和**$STRING 2**作为参数传递时，它通过将**$STRIN1**字符更改为**$STRING 2**字符来返回转换后的字符串。
*   如果将**$array**作为参数传递，它将通过将键字符串更改为值字符串来返回转换后的字符串。 如果将任何键作为“”传递，则它将返回 False 作为输出。

例如：

```php
Input : $string = "gieuz foh geeks", 
        $string1 = "iuzh"   ,    $string2="eksr"
Output : geeks for geeks
Explanation : i replaced by e 
u replaced by k 
z replaced by s 
h replaced by r 

Input : $string = "gieuz foh geeks",
        $string1 = "iuzh"   ,   $string2 = "eks"
Output : geeks foh geeks 
Explanation: "iuzh" was reduced to "iuz" and then 
replacement was done.  

Input: $string = "giiks in giiks",
       $arr = array("giiks" => "geeks", "in" => "for")
Output: geeks for geeks  
Explanation: "giiks" was replaced by "geeks" and 
"in" by "for" 

```

下面的程序演示了 PHP 中的 strtr()函数：

**程序 1：**当传递相同长度的字符串 1 和字符串 2 时，演示 strtr()函数的程序。

```php
<?php
// PHP program to demonstrate the strtr() function 
// when same length string1 and string2 is passed
$string = "gieuz foh geeks" ;
$string1 = "iuzh"; 
$string2 = "eksr";

// replacement is done 
echo strtr($string, $string1, $string2);

?>
```

产出：

```php
geeks for geeks
```

**程序 2：**当传递不同长度的字符串 1 和字符串 2 时，演示 strtr()函数的程序。

```php
<?php
// PHP program to demonstrate the strtr() function 
// when different length string1 and string2 is passed
$string = "gieuz foh geeks" ;
$string1 = "iuzh"; 
$string2 = "eks";

// replacement is done 
echo strtr($string, $string1, $string2);

?>
```

产出：

```php
geeks foh geeks
```

**程序 3：**演示 strtr()函数的程序，该函数替换出现字符的所有位置。

```php
<?php
// PHP program to demonstrate the strtr() function 
// which replaces at all positions where 
// characters are present
$string = "giiks for giiks" ;
$string1 = "i"; 
$string2 = "e";

// replacement is done 
echo strtr($string, $string1, $string2);

?>
```

产出：

```php
geeks for geeks
```

**程序 4：**当数组作为参数传递时，演示 strtr()函数的程序。

```php
<?php
// PHP program to demonstrate the strtr() function 
// when array is passed as the parameter

$string = "giiks in giiks" ;
$arr = array("giiks" => "geeks", "in" => "for");

// replacement is done 
echo strtr($string, $arr);
?>
```

产出：

```php
geeks for geeks
```

**程序 5：**当数组中的一个键作为“”传递时，演示 strtr()函数的程序。

```php
<?php
// PHP program to demonstrate the strtr() function 
// when one key in array is passed as ""

$string = "giiks in giiks" ;
$arr = array("giiks" => "geeks", "" => "for");

// replacement is done 
echo strtr($string, $arr);
?>
```

产出：

```php
No Output
```

**参考**：
[http://php.net/manual/en/function.strtr.php](http://php.net/manual/en/function.strtr.php)