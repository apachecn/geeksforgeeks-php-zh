# 在 PHP 中如何判断一个数组是否包含特定的值？

> 原文:[https://www . geesforgeks . org/如何确定数组是否包含特定的 php 值/](https://www.geeksforgeeks.org/how-to-determine-if-an-array-contains-a-specific-value-in-php/)

给定一个数组和一个特定的值，我们必须确定该数组是否包含该值。因此，有两种流行的方法来确定特定值是否在数组中。一个程序是通过**循环**使用，另一个是 [**in_array()**](https://www.geeksforgeeks.org/php-in_array-function/) 函数。通过使用**循环**来获取特定值的存在与否与 **in_array()** 功能相比是非常耗时的，所以这里我们将跳过**循环**一个，使用 **in_array()** 功能。
下面的程序说明了如何确定数组是否包含特定值:
**程序 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
//array containing elements
$names = array('Geeks', 'for', 'Geeks');

//search element
$item = 'Geeks';
if(in_array($item, $names)){
        //the item is there
    echo "Your element founded";
}
else{
        //the item isn't there
    echo "Element is not found";
}
?>
```

**输出:**

```php
Your element founded
```

**程序 2:** 在本例中， **in_array** 函数在严格模式下执行，它还将检查数组元素的类型。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
$name = array("Python", "Java", "C#", 3);

      //Searching python
if (in_array("python", $name, TRUE))
  {
  echo "found \n";
  }
else
  {
  echo "not found \n";
  }

    //Searching 3
if (in_array(3, $name, TRUE))
  {
  echo "found \n";
  }
else
  {
  echo "not found \n";
  }

  //Searching Java
if (in_array("Java", $name, TRUE))
  {
  echo "found \n";
  }
else
  {
  echo "not found \n";
  } 
?>
```

**输出:**

```php
not found 
found 
found 
```

**节目 3:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
$arr= array('gfg', 1, 17);

if (in_array('gfg', $arr)) {
    echo " gfg \n";
}

if (in_array(18, $arr)) {
    echo "18 found with strict check\n";
}
?>
```

**输出:**

```php
gfg 
```

在上面的例子中，数组包含字符串“gfg”和两个数字 1 和 17。if 语句调用 in_array() 函数，该函数检查给定数组中是否存在作为参数的给定项。如果函数返回 true，则执行 If 语句。