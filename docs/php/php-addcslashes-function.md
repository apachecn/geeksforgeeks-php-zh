# PHP |addcs 睫毛()函数

> 原文:[https://www.geeksforgeeks.org/php-addcslashes-function/](https://www.geeksforgeeks.org/php-addcslashes-function/)

addcs 睫毛()函数是 PHP 中的内置函数。add 睫毛()函数用于在给定字符串中的某些指定字符前添加反斜杠。

**语法**:

```
string addcslashes($string, $characters)

```

**参数**:该函数接受两个参数，如上语法所示，描述如下:

1.  **$string** :此参数指定需要转义的输入字符串。或者，我们也可以说，我们想要在其中的某些指定字符之前添加反斜杠的字符串。
2.  **$characters** :该参数指定了一个字符或字符序列，我们希望在输入字符串中通过在它们之前添加反斜杠来转义该字符或字符序列。我们可以将一系列字符指定为“a”..z。这是范围的开始字符，后跟两个点和结束字符。
    **注**:请谨慎使用 a、b、n、t 等字符，因为这个参数是预定义的转义序列，有一些特殊的含义。所以，我们可能得不到想要的结果。

**返回值**:该函数返回一个转义字符串，即输入字符串*$字符串*，在*$字符*之前添加反斜杠。

示例:

```
Input: $string = "GeeksforGeeks"  $characters = 'e'
Output: G\e\eksforG\e\eks

Input: $string = "GeeksforGeeks" $characters = 'a..k'
Output: G\e\e\ksnG\e\e\ks

```

下面的程序说明了 PHP 中的 addcs 睫毛()函数:

**程序 1** :

```
<?php
// PHP program to illustrate addcslashes()
// function

$str = "GeeksforGeeks";

$resStr = addcslashes($str, 'e');

echo $resStr;

?>
```

输出:

```
G\e\eksforG\e\eks

```

**程序 2** :

```
<?php
// PHP program to illustrate addcslashes()
// function

$str = "GeeksnGeeks";
$resStr = addcslashes($str, 'a..k');

echo $resStr;

?>
```

输出:

```
G\e\e\ksnG\e\e\ks

```

**参考**:
T3】http://php.net/manual/en/function.addcslashes.php