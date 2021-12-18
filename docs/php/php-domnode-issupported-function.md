# PHP|DOMNode isSupport()函数

> Original: [https://www.geeksforgeeks.org/php-domnode-issupported-function/](https://www.geeksforgeeks.org/php-domnode-issupported-function/)

**DOMNode：：isSupport()函数**是 PHP 中的一个内置函数，用于检查指定版本是否支持被询问的功能。

**语法：**

```php
*bool* DOMNode::isSupported( *string* $feature, *string* $version )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Feature:** it specifies the functionality to test.
*   **$version:** it specifies the version of the feature to be tested.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**DOMNode：：isSupport()函数**：

**示例 1：**

```php
<?php

// Write the feature name
$featureName1 = "Core";

// Check if it exists
$node1 = new DOMNode();
$isSupported1 = $node1->isSupported($featureName1, '1.0');
if ($isSupported1) {
    echo "Has feature $featureName1 module<br>";
}

// Write another feature name
$featureName2 = "XML";

// Check if it exists
$isSupported2 = $node1->isSupported($featureName2, '2.0');
if ($isSupported2) {
    echo "Has feature $featureName2 module";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

// Write the feature name
$featureName1 = "Events";

// Check if it exists
$node1 = new DOMNode();
$isSupported1 = $node1->isSupported($featureName1, '1.0');
if (!$isSupported1) {
    echo "Doesn't has feature $featureName1 module<br>";
}

// Write another feature name
$featureName2 = "CSS";

// Check if it exists
$isSupported2 = $node1->isSupported($featureName2, '2.0');
if (!$isSupported2) {
    echo "Doesn't has feature $featureName2 module";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domnode.issupported.php](https://www.php.net/manual/en/domnode.issupported.php)