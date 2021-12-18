# PHP|DOMText isWhitespaceInElementContent()函数

> Original: [https://www.geeksforgeeks.org/php-domtext-iswhitespaceinelementcontent-function/](https://www.geeksforgeeks.org/php-domtext-iswhitespaceinelementcontent-function/)

**DOMText：：isWhitespaceInElementContent()函数**是 PHP 中的内置函数，用于指示此文本节点是否包含空格。 简而言之，此函数用于检查 DOMText 对象是否包含文本。

**语法：**

```
*bool* DOMText::isWhitespaceInElementContent( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

以下示例说明 PHP 中的**DOMText：：isWhitespaceInElementContent()函数**：

**示例 1：**

```
<?php

// Create the DOMText without text
$text = new DOMText();

// Check if whitespace is there
if($text->isWhitespaceInElementContent()) {
    echo 'Yes ! object is empty.';
} else {
    echo 'NO it is not empty';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```
<?php

// Create a DOMText with text
$text = new DOMText('Geeksforgeeks');

// Check if whitespace is there
if(!$text->isWhitespaceInElementContent()) {
    echo 'No ! object isn\'t empty.';
} else {
    echo 'Object is empty';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domtext.iswhitespaceinelementcontent.php](https://www.php.net/manual/en/domtext.iswhitespaceinelementcontent.php)