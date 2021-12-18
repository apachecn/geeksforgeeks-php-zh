# 如何用 PHP 检查 URL 是否包含某个字符串？

> 原文:[https://www . geesforgeks . org/how-to-check-if-URL-contain-seven-string-use-PHP/](https://www.geeksforgeeks.org/how-to-check-if-url-contain-certain-string-using-php/)

给定一个网址，任务是检查该网址是否包含特定的字符串。网址基本上就是字符串。因此，为了检查某些字符串的存在，可以遵循两种方法。第一种方法用于查找字符串中的子字符串匹配，第二种方法用于查找正则表达式匹配。PHP 包含这两种方法的函数。

**方法 1:**
**strpos()函数:**strpos()函数用于查找字符串中子字符串的第一次出现。如果子字符串存在，则函数返回子字符串的起始索引，否则如果在字符串(网址)中找不到子字符串，则返回假。

**语法:**

```php
int strpos( $String, $Substring )
```

**参数:**strpos()函数接受两个参数，如上所述，如下所述。

*   **$String:** 此参数保存执行搜索的文本。
*   **$Substring:** 此参数保存要搜索的模式或子字符串。

**程序:** PHP 程序使用 strpos()函数在一个 URL 中查找某个字符串。

```php
<?php
// PHP program to find certain substring in an URL

// Given URL
$url = 'https://www.geeksforgeeks.org/gfg/index';

// Search substring 
$key = 'gfg';

if (strpos($url, $key) == false) {
    echo $key . ' not exists in the URL <br>';
}
else {
    echo $key . ' exists in the URL <br>';
}

// Another search substring
$key = 'function';

if (strpos($url, $key) == false) {
    echo $key . ' not exists in the URL';
}
else {
    echo $key . ' exists in the URL';
}

?>
```

**Output:**

```php
gfg exists in the URL 
function not exists in the URL

```

**注意:**strpos()函数使用字符串匹配方法在文本中查找子字符串。有时它会产生不希望结果。例如:如果字符串网址是*https://www.geeksforgeeks.org/myfunction*，子字符串是*函数*，那么子字符串存在于字符串网址中。假设一个网站想要显示*功能*的结果，但是显示的是*我的功能*的结果，这是不一样的。strpos()函数不会检查子字符串是作为一个整体出现，还是带有后缀或前缀。

**注意:**要解决这个问题，那就是找出字符串(URL)中是否存在确切的模式，使用 preg_match()函数。

**方法 2:**
**preg_match()函数:**preg _ match()函数用于使用正则表达式搜索来查找文本中模式的精确匹配。这里给定了一个正则表达式模式，该函数对文本进行搜索，并找到完全匹配的文本(如果有的话)。如果模式存在，此函数返回 true 如果模式不存在，则返回 false。

**语法:**

```php
preg_match( $pattern, $subject )
```

**参数:**preg _ match()函数接受两个参数，如上所述，如下所述。

*   **$pattern:** 是作为字符串进行搜索的正则表达式模式
*   **$subject:** 是搜索正则表达式模式的文本字符串。

**程序 2:** PHP 程序，用于查找 URL 中字符串的精确匹配

```php
<?php
// PHP program to find exach match substring

// Given a URL
$url = 'https://www.geeksforgeeks.org/gfg/myfunction';

// Here '\b' represents the block

// This pattern search gfg as whole words
$pattern = '/\bgfg\b/';

if (preg_match($pattern, $url) == false) {
    echo 'gfg does not exist in the URL <br>';
}
else {
    echo 'gfg exist in the URL <br>';
}

// Given another URL
$url2 = 'https://www.geeksforgeeks.org/myfunction';

// This pattern search function as whole words
$pattern = '/\bfunction\b/';

if (preg_match($pattern, $url2) == false) {
    echo 'function does not exist in the URL';
}
else {
    'function exist in the URL';
}

?>
```

**Output:**

```php
gfg exist in the URL 
function does not exist in the URL

```