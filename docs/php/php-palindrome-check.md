# PHP|回文检查

> Original: [https://www.geeksforgeeks.org/php-palindrome-check/](https://www.geeksforgeeks.org/php-palindrome-check/)

在本文中，我们将学习如何在 PHP 中检查数字和字符串是否为回文。 如果数字或字符串在分别颠倒数字或字母后仍保持不变，则称其为回文。
回文编号示例：

```
Input : 1441
Output : Palindrome
Explanation: Reversing 1441 will also get 1441

Input : 12521
Output : Palindrome
Explanation remains same
```

**检查回文编号**

在这里，我们简单地使用迭代方法来检查回文数。 在一次迭代中提取每个数字，并形成反数，最后检查是否与原数相同。“

## PHP

```
<?php
// PHP code to check for Palindrome number in PHP
// Function to check for Palindrome
function Palindrome($number){ 
    $temp = $number; 
    $new = 0; 
    while (floor($temp)) { 
        $d = $temp % 10; 
        $new = $new * 10 + $d; 
        $temp = $temp/10; 
    } 
    if ($new == $number){ 
        return 1; 
    }
    else{
        return 0;
    }
} 

// Driver Code
$original = 1441;
if (Palindrome($original)){ 
    echo "Palindrome"; 
}
else { 
echo "Not a Palindrome"; 
}

?> 
```

输出：0

```
Palindrome
```

**检查回文字符串**

回文字符串的示例：

```
Input : "MALAYALAM"
Output : Palindrome
Explanation: Reversing "MALAYALAM" will also get "MALAYALAM"

Input : "14441"
Output : Palindrome
Explanation remains same
```

**方法 1：使用 strrev()**和
在 PHP 中使用[strrev()](https://www.geeksforgeeks.org/php-reverse-string/)函数来反转字符串。 我们可以简单地使用此方法来反转字符串，并将其与前一个值进行匹配。 如果是匹配项，则字符串为回文，否则不是。-
示例：

## PHP

```
<?php
// PHP code to check for Palindrome string in PHP
// Using strrev()
function Palindrome($string){ 
    if (strrev($string) == $string){ 
        return 1; 
    }
    else{
        return 0;
    }
} 

// Driver Code
$original = "DAD";
if(Palindrome($original)){ 
    echo "Palindrome"; 
}
else { 
echo "Not a Palindrome"; 
}
?> 
```

输出：0

```
Palindrome
```

**方法 2：使用 substr()**和
的递归方式[substr()](https://www.geeksforgeeks.org/php-substr-function/)方法用于返回字符串的一部分，称为子字符串。 使用这种方法，有一种递归的方式来检查是否有回文。 在此方法中，不会形成新字符串，并且在每次递归调用中都会修改原始字符串。例如：

## PHP

```
<?php
// PHP code to check for Palindrome string in PHP
// Recursive way using substr()
function Palindrome($string){

    // Base condition to end the recursive process
    if ((strlen($string) == 1) || (strlen($string) == 0)){
        echo "Palindrome";
    }

    else{

        // First character is compared with the last one
        if (substr($string,0,1) == substr($string,(strlen($string) - 1),1)){

            // Checked letters are discarded and passed for next call
            return Palindrome(substr($string,1,strlen($string) -2));
        }
        else{
            echo " Not a Palindrome"; }
    }
}

$string = "MALAYALAM";
Palindrome($string);
?> 
```

输出：0

```
Palindrome
```

**工作：**和
在每次递归调用期间，第一个字符与字符串的最后一个字符匹配，如果匹配，则在下一次调用期间丢弃这两个字符。 这一直持续到字符串的长度减少到 0 或 1 为止。在下面的例子中，使用单词“马拉雅拉姆”，让我们来看看它是如何工作的。
在第一步中，两个 M 都在，末尾进行比较。 因为匹配，所以这两个字符串都被丢弃，下一个要传递的字符串是“ALAYALA”。 同样，两个 A 在两端都匹配，所以下一个要传递的字符串是“layal”。 这种情况一直持续到只剩下“Y”为止。