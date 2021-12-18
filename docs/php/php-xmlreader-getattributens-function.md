# PHP|XMLReader getAttributeNS()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-getattributens-function/](https://www.geeksforgeeks.org/php-xmlreader-getattributens-function/)

**XMLReader：：getAttributens()函数**是 PHP 中的一个内置函数，用于根据名称和命名空间 URI 获取属性的值，如果属性不存在或不在元素节点上，则获取空字符串。

**语法：**

```
*string* XMLReader::getAttributeNs( *string* $localName, 
                               *string* $namespaceURI )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$localName:** it specifies the local name.
*   **$NamespaceURI:** it specifies the namespace URI.

**返回值：**成功时返回属性值，失败时返回空字符串。

下面的示例说明 PHP 中的**XMLReader：：getAttributeNS()函数**：

**示例 1：**

*   **data.xml**

    ```
    <?xml version="1.0" encoding="utf-8"?>
    <div xmlns:x="geeksforgeeks">
        <x:h1 x:attrib="value">
          Namespaced Text 
        </x:h1>
    </div>
    ```

*   **index.php**

    ```
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Load the XML file
    $XMLReader->open('data.xml');

    // Move to next node three times
    $XMLReader->read();
    $XMLReader->read();
    $XMLReader->read();

    // Get the value of attribute but
    // give a wrong namespace here
    $value = $XMLReader->getAttributeNs(
        "attrib", "wrong_namespace");

    // Output the value to browser
    echo $value . "<br>";

    ?>
    ```

*   **output:**

    ```
     // Empty string because namespace name doesn't match
    ```

示例 2：

*   **data.xml**

    ```
    <?xml version="1.0" encoding="utf-8"?>
    <div xmlns:x="my_namespace">
        <x:h1 x:attrib="value"> 
          Namespaced Text 
        </x:h1>
    </div>
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

            // Get the value of attribute with name "attrib"
            // and namespace "my_namespace"
            $value = $XMLReader->
                   getAttributeNs("attrib", "my_namespace");

            // Output the value to browser
            echo $value . "<br>";
        }
    }
    ?>
    ```

*   **output:**

    ```
    value
    ```

**引用：**[https://www.php.net/manual/en/xmlreader.getattributens.php](https://www.php.net/manual/en/xmlreader.getattributens.php)