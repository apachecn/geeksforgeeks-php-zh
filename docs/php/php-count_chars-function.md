# PHP|count_chars()函数

> Original: [https://www.geeksforgeeks.org/php-count_chars-function/](https://www.geeksforgeeks.org/php-count_chars-function/)

Count_chars()是 PHP 中的一个内置函数，用于执行几个与字符串相关的操作，如字符串中出现的 ASCII 字符数。

**语法：**

```
count_chars(string,return_mode);

```

**参数**：count_chars()函数接受两个参数*string*和*return_mode*，如下所示：

*   **string:** this parameter refers to the input string on which you want to perform an operation.
*   **RETURN_MODE:** this parameter is optional. This parameter defines the action that needs to be performed on the string. It accepts a value of 0pm 1pm 2pm 3pm 4.
    1.  **0:** if you select this mode, the function returns an array with a key-value pair whose key is an ASCII value, and the corresponding value will be the number of times that ASCII value occurs.
    2.  **1:** if you select this mode, the count_chars () function returns an array of key-value pairs whose key is an ASCII value, and the corresponding value will be the number of times that ASCII value occurs. Here, the array will contain only keys in the form of ASCII values with a frequency greater than 0.
    3.  **2:** in this mode, the function returns an array of key-value pairs, where key is the ASCII value of frequency 0 in the string.
    4.  **3:** in this mode, the count_chars () function returns strings of all different characters used in the string in ascending order.
    5.  **4:** in this mode, the count_chars () function returns the input string

中未使用的字符串

**返回类型**：此函数将返回一个数组或字符串，具体取决于如上所述的 RETURN_MODE 参数。

示例：

```
Input : string = "GeeksforGeeks"  ,  return_mode = 3
Output : Gefkors

```

下面是说明 count_chars()函数工作原理的 PHP 程序：

```
<?php
    // PHP program to illustrate count_chars() 

    // Input string
    $string = "geeksforgeeks";

    // return_mode 1
    print_r(count_chars($string,1));

    // return_mode 3
    print_r(count_chars($string,3));

    // return_mode 4
    print_r(count_chars($string,4));
?>
```

帖子主题：Re：Колибри

上面的程序显示了字符串“geeksforgeek”的返回值，其中 return_mode 为 1、3 和 4。您可以通过更改函数调用中的 return_mode 的值来修改程序，以查看模式 0 和 2 的返回值。