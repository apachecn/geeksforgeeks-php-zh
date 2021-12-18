# PHP|Next()函数

> Original: [https://www.geeksforgeeks.org/php-next-function/](https://www.geeksforgeeks.org/php-next-function/)

**Next()**函数是 PHP 中的内置函数，它执行以下操作：

*   它用于返回数组中内部指针当前指向的下一个元素的值。 我们可以通过[CURRENT](https://www.geeksforgeeks.org/php-current-function/)函数知道当前元素。
*   函数**Next()**在返回值后递增内部指针。
*   在 PHP 中，所有数组都有一个内部指针。 此内部指针指向该数组中的某个元素，该元素称为数组的当前元素。
*   通常，开头的下一个元素是数组中插入的第二个元素。

**语法：**

```php
next($array)
```

**参数：**它只接受一个参数*$array*。 此参数是必需的。 它是我们需要在其中找到下一个元素的数组。

**返回值：**此函数返回内部指针当前指向的数组中下一个元素的值。 如果 NEXT 处没有元素，则返回*False*。 最初，next()函数返回第二个插入的元素。

例如：

```php
Input : array = [1, 2, 3, 4] 
Output : 2 

Input : array = [1, 2, 3, 4], next() function executed two times      
Output : 2
         3 

```

下面的程序演示了 PHP 中的 next()函数：

**程序 1：**

```php
<?php
// PHP Program to demonstrate the
// first position of next() function 

$array = array("geeks", "Raj", "striver",
                         "coding", "RAj");

echo next($array);

?>
```

产出：

```php
Raj
```

**程序 2：**

```php
<?php
// PHP Program to demonstrate the 
// working of next() function 

$array = array("geeks", "Raj", "striver", "coding", "RAj");

// prints the initial current element (geeks)  
echo current($array), "\n"; 

// prints the initial next element (Raj)
// moves the pointer forward
echo next($array), "\n";  

// prints the  current element (Raj)  
echo current($array), "\n";  

// prints the  next element (striver)
// moves the pointer forward
echo next($array), "\n";  

// prints the  current element (striver)  
echo current($array), "\n";  

// prints the  next element (coding)
// moves the pointer forward
echo next($array), "\n";  

// prints the  current element (coding)  
echo current($array), "\n"; 
?>
```

产出：

```php
geeks
Raj
Raj
striver
striver
coding
coding

```

**参考**：
[http://php.net/manual/en/function.next.php](http://php.net/manual/en/function.next.php)