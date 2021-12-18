# PHP|XMLReader getParserProperty()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-getparserproperty-function/](https://www.geeksforgeeks.org/php-xmlreader-getparserproperty-function/)

**XMLReader：：getParserProperty()函数**是 PHP 中的内置函数，用于检查是否设置了指定的属性。

**语法：**

```php
*bool* XMLReader::getParserProperty( *int* $property )
```

**参数：**此函数接受单个参数**$property**，该参数保存与解析器选项常量之一相对应的整数。
解析器选项常量列表如下：

*   ***XMLReader：：LOADDTD(1)***这将加载 DTD，但不会进行验证。
*   ***XMLReader：：DEFAULTATTRS(2)***这将加载 DTD 和默认属性，但不会进行验证。
*   ***XMLReader：：VALIDATE(3)***这将在解析时加载 DTD 并进行验证。
*   ***XMLReader：：SUBST_ENTITIES(4)***这将替换实体并展开引用。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**异常：**此函数在出错时引发 XMLReaderException。

以下示例说明 PHP 中的**XMLReader：：getParserProperty()函数**：

**示例 1：**

*   **data.xml**

    ```php
    <?xml version="1.0" encoding="utf-8"?>
    <div xmlns:x="geeksforgeeks">
        <x:h1 x:attrib="value">
          Namespaced Text 
        </x:h1>
    </div>
    ```

*   **index.php**

    ```php
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file with sample XML
    $XMLReader->open('data.xml');

    // Check if XMLReader::VALIDATE is set or not
    $isProperty = $XMLReader->
    getParserProperty(XMLReader::VALIDATE);

    if (!$isProperty) {
        echo 'Property isn\'t set.';
    }
    ?>
    ```

*   发帖主题：Re：Колибри0.7.8.0

**示例 2：**

*   **data.xml**

    ```php
    <?xml version="1.0" encoding="utf-8"?>
    <div xmlns:x="geeksforgeeks">
        <x:h1 x:attrib="value">
          Namespaced Text 
        </x:h1>
    </div>
    ```

*   **index.php**

    ```php
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file with sample XML
    $XMLReader->open('data.xml');

    // Set the Parser Property
    $XMLReader->setParserProperty(
        XMLReader::VALIDATE, true);

    // Check if XMLReader::VALIDATE
    // is set or not
    $isProperty = $XMLReader->getParserProperty(
            XMLReader::VALIDATE);

    if ($isProperty) {
        echo 'Property is set.';
    }
    ?>
    ```

*   发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/xmlreader.getparserproperty.php](https://www.php.net/manual/en/xmlreader.getparserproperty.php)