# PHP|XMLReader readString()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-readstring-function/](https://www.geeksforgeeks.org/php-xmlreader-readstring-function/)

**XMLReader：：readString()函数**是 PHP 中的一个内置函数，用于将当前节点的内容作为字符串读取。 ReadString()和 getInnerXml()的区别在于前者不包含标记，而只包含子节点的内容。

**语法：**

```php
*string* XMLReader::readString( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**失败时，此函数以字符串或空字符串的形式返回当前节点的内容。

下面的示例说明了 PHP 中的**XMLReader：：readString()函数**：

**示例 1：**在本程序中，我们将读取没有子节点的元素的值。

*   **data.xml**

    ```php
    <?xml version="1.0" encoding="utf-8"?>
    <div>
        <h1>GeeksforGeeks</h1>
    </div>
    ```

*   **index.php**

    ```php
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Iterate through the XML nodes to
    // reach the h1 element
    $XMLReader->read();
    $XMLReader->read();
    $XMLReader->read();

    // Print the XML content
    echo "The text inside is:" 
      . $XMLReader->readString();
    ?>
    ```

*   **output:**

    ```php
    The text inside is: GeeksforGeeks
    ```

**示例：**在本程序中，我们将读取带有子节点的元素的值。

*   **data.xml**

    ```php
    <?xml version="1.0" encoding="utf-8"?>
    <div>
        <h1>Hello World 
           <sub>G4G</sub>
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

    // Iterate through the XML nodes to
    // reach the h1 element
    $XMLReader->read();
    $XMLReader->read();
    $XMLReader->read();

    // Print the XML content
    echo "The text inside is:" 
      . $XMLReader->readString();
    ?>
    ```

*   **output:**

    ```php
    The text inside is: Hello World G4G
    ```

**引用：**[https://www.php.net/manual/en/xmlreader.readstring.php](https://www.php.net/manual/en/xmlreader.readstring.php)