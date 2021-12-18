# PHP|XMLReader Close()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-close-function/](https://www.geeksforgeeks.org/php-xmlreader-close-function/)

**XMLReader：：Close()函数**是 PHP 中的一个内置函数，用于关闭当前正在解析的 XMLReader 对象的输入。

**语法：**

```php
*bool* XMLReader::close( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**XMLReader：：Close()函数**：

**程序 1：**

*   **data.xml**

    ```php
    <?xml version="1.0" encoding="utf-8"?>
    <root>
        <p> Hello world </p>
    </root>
    ```

*   **index.php**

    ```php
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Close the XML Reader before reading XML
    $XMLReader->close();

    // Move to the first node
    $XMLReader->read();

    // Read it as a string
    $string = $XMLReader->readString();

    // Output the string to the browser
    echo $string;
    ?>
    ```

*   **output:**

    ```php
    // Blank because we closed the input of the XMLReader before reading XML
    ```

**程序 2：**

*   **data.xml**

    ```php
    <?xml version="1.0" encoding="utf-8"?>
    <body>
        <h1> GeeksforGeeks </h1>
    </body>
    ```

*   **index.php**

    ```php
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Move to the first node
    $XMLReader->read();

    // Read it as a string
    $string = $XMLReader->readString();

    // Output the string to the browser
    echo $string;

    // Close the XML Reader after reading XML
    $XMLReader->close();
    ?>
    ```

*   **output:**

    ```php
    GeeksforGeeks
    ```

**引用：**[https://www.php.net/manual/en/xmlreader.close.php](https://www.php.net/manual/en/xmlreader.close.php)