# PHP|XMLReader getAttributeNo()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-getattributeno-function/](https://www.geeksforgeeks.org/php-xmlreader-getattributeno-function/)

**XMLReader：：getAttributeNo()函数**是 PHP 中的一个内置函数，用于根据属性的位置获取属性值，如果属性不存在或未定位在元素节点上，则获取空字符串。

**语法：**

```
*string* XMLReader::getAttributeNo( *int* $index )
```

**参数：**此函数接受单个参数**$index**，该参数保存要提取的属性值的索引。

**返回值：**此函数在成功时返回属性值或返回空字符串。

下面的示例说明 PHP 中的**XMLReader：：getAttributeNo()函数**：

**示例 1：**

*   **data.xml**

    ```
    <?xml version="1.0" encoding="utf-8"?>
    <body>
        <h1> Hello </h1>
    </body>
    ```

*   **index.php**

    ```
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Load the XML file
    $XMLReader->open('data.xml');

    // Iterate through the XML
    while ($XMLReader->read()) {
        if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

            // Get the value of first attribute
            $value = $XMLReader->getAttributeNo(0);

            // Output the value to browser
            echo $value . "<br>";
        }
    }
    ?>
    ```

*   **output:**

    ```
    // Empty string because no attributes are there in XML
    ```

示例 2：

*   **data.xml**

    ```
    <?xml version="1.0" encoding="utf-8"?>
    <body>
        <h1 id="geeksforgeeks"> Hello </h1>
        <h2 id="my_id"> World </h2>
    </body>
    ```

*   **index.php**

    ```
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Load the XML file
    $XMLReader->open('data.xml');

    // Iterate through the XML
    while ($XMLReader->read()) {
        if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

            // Get the value of first attribute
            $value = $XMLReader->getAttributeNo(0);

            // Output the value to browser
            echo $value . "<br>";
        }
    }
    ?>
    ```

*   **output:**

    ```
    geeksforgeeks
    my_id
    ```

**引用：**[https://www.php.net/manual/en/xmlreader.getattributeno.php](https://www.php.net/manual/en/xmlreader.getattributeno.php)