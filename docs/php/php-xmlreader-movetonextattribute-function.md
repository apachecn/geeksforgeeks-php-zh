# PHP|XMLReader moveToNextAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-movetonextattribute-function/](https://www.geeksforgeeks.org/php-xmlreader-movetonextattribute-function/)

**XMLReader：：moveToNextAttribute()函数**是 PHP 中的一个内置函数，如果定位在属性上，则用于将光标移动到下一个属性；如果定位在元素上，则用于移动到第一个属性。 此函数还可用于检查元素中是否有属性。

**语法：**

```php
*bool* XMLReader::moveToNextAttribute( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明 PHP 中的**XMLReader：：moveToNextAttribute()函数**：

**示例 1：**

*   **data.xml**

    ```php
    <?xml version="1.0" encoding="utf-8"?>
    <div>
        <h1> Foo Bar </h1>
    </div>
    ```

*   **index.php**

    ```php
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Iterate through the XML nodes
    // to reach the h1 node
    $XMLReader->read();
    $XMLReader->read();
    $XMLReader->read();

    // Checking if attribute is there or not
    if ($XMLReader->moveToNextAttribute()) {
        echo "Attribute is there";
    } else {
        echo "No, attributes.";
    }
    ?>
    ```

*   **output:**

    ```php
    No, attributes.
    ```

示例 2：

*   **data.xml**

    ```php
    <?xml version="1.0" encoding="utf-8"?>
    <div>
        <h1 attrib1="value1"
            attrib2="value2" 
            attrib3="value">
         Foo Bar 
        </h1>
    </div>
    ```

*   **index.php**

    ```php
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Iterate through the XML nodes
    // to reach the h1 node
    $XMLReader->read();
    $XMLReader->read();
    $XMLReader->read();

    // Move to first attribute
    $XMLReader->moveToFirstAttribute();

    // Print name of element
    echo "Before:<br> We are currently "
          . "at: $XMLReader->name<br>";

    // Move to next attribute
    $XMLReader->moveToNextAttribute();

    // Print name of element
    echo "After:<br> We are currently "
          . "at: $XMLReader->name";
    ?>
    ```

*   **output:**

    ```php
    Before:
    We are currently at: attrib1
    After:
    We are currently at: attrib2
    ```

**引用：**[https://www.php.net/manual/en/xmlreader.movetonextattribute.php](https://www.php.net/manual/en/xmlreader.movetonextattribute.php)