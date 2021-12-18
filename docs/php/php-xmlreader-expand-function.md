# PHP|XMLReader Expand()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-expand-function/](https://www.geeksforgeeks.org/php-xmlreader-expand-function/)

**XMLReader：：Expand()函数**是 PHP 中的一个内置函数，用于复制当前节点并返回适当的 DOM 对象。

**语法：**

```
*DOMNode* XMLReader::expand( *DOMNode* $basenode )
```

**参数：**此函数接受单个参数**$basenode**，该参数保存定义所创建 DOM 对象的目标 DOMDocument 的 DOMNode。

**返回值：**此函数成功时返回 DOMNode，失败时返回 False。

下面的示例说明了 PHP 中的**XMLReader：：Expand()函数**：

**示例 1：**

*   **data.xml**

    ```
    <?xml version="1.0" encoding="utf-8"?>
    <root>
        <div> This is a div </div>
    </root>
    ```

*   **index.php**

    ```
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Move to the first node
    $XMLReader->read();

    // Read it as a element
    $element = $XMLReader->expand();

    // Print the node value to the browser
    echo $element->nodeValue;
    ?>
    ```

*   发帖主题：Re：Колибри0.7.8.0

**示例 2：**

*   **data.xml**

    ```
    <?xml version="1.0" encoding="utf-8"?>
    <body>
        <h1 style="color:green; font-size:100px;"> 
          GeeksforGeeks 
        </h1>
    </body>
    ```

*   **index.php**

    ```
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Move to the first node
    $XMLReader->read();

    // Read it as a element
    $element = $XMLReader->expand();

    // Create a new DOMDocument instance
    $DOMDocument = new DOMDocument();

    // Append the child to the element
    $DOMDocument->appendChild($element);

    // Render the XML in browser
    echo $DOMDocument->saveXML();
    ```

*   **输出：**
    ![](img/bde3c1e2281f708b567c30dc1bbdffcb.png)

**引用：**[https://www.php.net/manual/en/xmlreader.expand.php](https://www.php.net/manual/en/xmlreader.expand.php)