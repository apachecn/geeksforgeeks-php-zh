# PHP|按自然顺序和标准顺序对字符串数组进行排序

> Original: [https://www.geeksforgeeks.org/php-sort-array-strings-natural-standard-orders/](https://www.geeksforgeeks.org/php-sort-array-strings-natural-standard-orders/)

您将看到一个字符串数组。 您必须以标准方式(字母大小写重要)和自然方式(字母大小写无关)对给定的数组进行排序。

```php
Input : arr[] = {"Geeks", "for", "geeks"}
Output : Standard sorting: Geeks for geeks 
         Natural sorting: for Geeks geeks 

Input : arr[] = {"Code", "at", "geeks", "Practice"}
Output : Standard sorting: Code Practice at geeks 
         Natural sorting: at Code geeks Practice 

```

如果您试图以一种简单的方式对字符串数组进行排序，则可以简单地创建一个用于字符比较的比较函数，并对给定的字符串数组进行排序。 但这将区分小写字母和大写字母。 要解决这个问题，如果你想用 c/java 解决这个问题，你必须编写自己的比较函数，专门处理字母表的大小写。 但是，如果我们选择[PHP](https://www.geeksforgeeks.org/php/)作为我们的语言，那么我们可以在 natcasesort()的帮助下直接对其进行排序。
natcasesort()：它对字符串进行排序，而不考虑它们的大小写。 表示‘a’&‘A’在此排序方法中被视为小于‘b’&‘B’。

```php
// declare array
$arr = array ("Hello", "to", "geeks", "for", "GEEks");

// Standard sort
$standard_result = sort($arr);
print_r($standart_result);

// natural sort
$natural_result = natcasesort($arr);
print_r($natural_result);

```

```php
<?php
// PHP program to sort an array 
// in standard and natural ways.

// function to print array
function printArray ($arr)
{
    foreach ($arr as $value) {
        echo "$value ";
    }
}

// declare array
$arr = array ("Hello", "to", "geeks", "for", "GEEks");

// Standard sort
$standard_result = $arr;
sort($standard_result);
echo "Array after Standard sorting: ";
printArray($standard_result);

// natural sort
$natural_result = $arr;
natcasesort($natural_result);
echo "\nArray after Natural sorting: ";
printArray($natural_result);
?>
```

产出：

```php
Array after Standard sorting: GEEks Hello for geeks to 
Array after Natural sorting: for geeks GEEks Hello to 

```