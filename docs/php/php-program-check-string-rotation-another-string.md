# PHP|检查字符串的程序是另一个字符串的旋转

> Original: [https://www.geeksforgeeks.org/php-program-check-string-rotation-another-string/](https://www.geeksforgeeks.org/php-program-check-string-rotation-another-string/)

给定这两根弦，我们必须检查一根弦是否是另一根弦的旋转。

例如：

```
Input : $string1 = "WayToCrack",
        $string2 = "CrackWayTo";
Output : Yes

Input : $string1 = "WillPower" 
        $string2 = "lliW";
Output : No.

```

上述问题在其他语言中可以很容易地解决，方法是将两个字符串连接起来，然后检查得到的连接后的字符串是否包含该字符串。 但在 PHP 中，我们将使用内置函数来解决该问题。 使用的内置函数包括：

*   **[strpos()](https://www.geeksforgeeks.org/php-strpos-stripos-functions/)：**该函数通常接受两个参数，一个用于指定要搜索的字符串，另一个用于在指定的字符串中查找。

在 PHP 解决方案中，如果在指定的字符串中找到字符串，则**strpos()**将给出字符串的最后一个位置。

下面是上述方法的实现

## PHP

```
<?php
    function rotation_string($string1, $string2)
    {
        // if both strings are not same length then stop
        if (strlen($string1) != strlen($string2))
           echo "No";

         // concatenate $string1 to itself, if both
         // strings are of same length
         if (strlen($string1) == strlen($string2))
            $string1 = $string1.$string1;

         if (strpos($string1, $string2) > 0)
            echo "Yes";
         else 
            echo "No";
    }

    // Driver code
    $string1 = "WayToCrack";
    $string2 = "CrackWayTo";        
    rotation_string($string1, $string2);
?>
```

**Output:**

```
Yes

```