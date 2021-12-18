# PHP|XMLReader moveToFirstAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-movetofirstattribute-function/](https://www.geeksforgeeks.org/php-xmlreader-movetofirstattribute-function/)

**XMLReader：：moveToFirstAttribute()函数**是 PHP 中的一个内置函数，用于将光标定位在元素的第一个属性上。 当一个元素有多个属性并且我们想要获取第一个属性时，或者当我们想检查一个元素是否有任何属性时，这个函数很有用。

**语法：**

```php
*bool* XMLReader::moveToFirstAttribute( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明 PHP 中的**XMLReader：：moveToFirstAttribute()函数**：

**示例 1：**

*   **data.xml**

    ```php
    <?xml version="1.0" encoding="utf-8"?>
    <div>
        <h1>Foo Bar</h1>
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
    if ($XMLReader->moveToFirstAttribute()) {
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

**程序 2：**

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

    // Move to attribute with name attrib3
    $XMLReader->moveToAttribute("attrib3");

    // Print name of element
    echo "Before:<br> We are currently "
          . "at: $XMLReader->name<br>";

    // Move to first attribute
    $XMLReader->moveToFirstAttribute();

    // Print name of element
    echo "After:<br> We are currently "
          . "at: $XMLReader->name";
    ?>
    ```

*   **output:**

    ```php
    Before:
    We are currently at: attrib3
    After:
    We are currently at: attrib1
    ```

**引用：**[https://www.php.net/manual/en/xmlreader.movetofirstattribute.php](https://www.php.net/manual/en/xmlreader.movetofirstattribute.php)