# 用 PHP

生成随机字符串的程序

> Original: [https://www.geeksforgeeks.org/program-to-generate-random-string-in-php/](https://www.geeksforgeeks.org/program-to-generate-random-string-in-php/)

给定大小为 N，任务是生成大小为 N 的随机字符串。

示例：

```
Input: 5
Output: eR3Ds

Input: 10
Output: MPRCyBgdcn

```

**方法：**创建一个包含小写字母、大写字母和数字(0 到 9)的域名字符串。 然后生成一个随机数并选取出现在该随机索引处的字符，并将该字符附加到答案字符串中。

**以下是使用上述方法生成随机字符串的程序：**

```
<?php

// PHP function to print a 
// random string of length n
function RandomStringGenerator($n)
{
    // Variable which store final string
    $generated_string = "";

    // Create a string with the help of 
    // small letters, capital letters and
    // digits.
    $domain = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890";

    // Find the length of created string
    $len = strlen($domain);

    // Loop to create random string
    for ($i = 0; $i < $n; $i++)
    {
        // Generate a random index to pick
        // characters
        $index = rand(0, $len - 1);

        // Concatenating the character 
        // in resultant string
        $generated_string = $generated_string . $domain[$index];
    }

    // Return the random generated string
    return $generated_string;
}

// Driver code to test above function
$n = 5;
echo "Random String of length " . $n 
   . " = " . RandomStringGenerator($n);
?>
```

**输出：**

```
Random String of length 5 = EEEto

```