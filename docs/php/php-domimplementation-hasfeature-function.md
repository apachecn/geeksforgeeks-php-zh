# PHP|DOMImplementation hasFeature()函数

> Original: [https://www.geeksforgeeks.org/php-domimplementation-hasfeature-function/](https://www.geeksforgeeks.org/php-domimplementation-hasfeature-function/)

**DOMImplementation：：hasFeature()函数**是 PHP 中的一个内置函数，用于测试 DOM 实现是否实现了特定功能。

**语法：**

```php
*bool* DOMImplementation::hasFeature( *string* $feature, *string* $version )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Feature:** it specifies the functionality to test.
*   **$version:** it specifies the version number of the feature to be tested.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**异常：**此函数在出错时抛出**E_Strict**异常。

以下示例说明 PHP 中的**DOMImplementation：：hasFeature()函数**：

**示例 1：**

```php
<?php

// Write the feature name
$featureName1 = "Core";

// Check if it exists
$hasFeature1 = 
    DOMImplementation::hasFeature($featureName1, '1.0');
if ($hasFeature1) {
    echo "Has feature $featureName1 module <br>";
}

// Write another feature name
$featureName2 = "XML";

// Check if it exists
$hasFeature2 = 
    DOMImplementation::hasFeature($featureName2, '2.0');
if ($hasFeature2) {
    echo "Has feature $featureName2 module <br>";
}
?>  
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php
// Write the feature name
$featureName1 = "Events";

// Check if it doesn't exists
$hasFeature1 = 
    DOMImplementation::hasFeature($featureName1, '1.0');
if (!$hasFeature1) {
    echo "Doesn't have feature $featureName1 module. <br>";
}

// Write another feature name
$featureName2 = "CSS";

// Check if it doesn't exists
$hasFeature2 = 
    DOMImplementation::hasFeature($featureName2, '2.0');
if (!$hasFeature2) {
    echo "Doesn't have feature $featureName2 module. <br>";
}
?>  
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domimplementation.hasfeature.php](https://www.php.net/manual/en/domimplementation.hasfeature.php)