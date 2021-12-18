# PHP|XMLReader setRelaxNGSchemaSource()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-setrelaxngschemasource-function/](https://www.geeksforgeeks.org/php-xmlreader-setrelaxngschemasource-function/)

**XMLReader：：setRelaxNGSchemaSource()函数**是 PHP 中的一个内置函数，用于设置包含 RelaxNG 模式的数据以用于验证。 *setRelaxNGSchemaSource()*函数与*setRelaxNGSchema()*函数不同，前者接受规则作为字符串变量，而后者接受.rng 文件形式的规则。

**语法：**

```
*bool* XMLReader::setRelaxNGSchemaSource( *string* $source )
```

**参数：**此函数接受单个参数**$source**，该参数保存包含 RelaxNG 模式的字符串。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明 PHP 中的**XMLReader：：setRelaxNGSchemaSource()函数**：

**示例 1：**

*   **data.xml**

    ```
    <?xml version="1.0"?>
    <body>
        <div>
            <h1>GeeksForGeeks</h1>
            <p>Portal for Geeks</p>
        </div>
        <div>
            <h1>Heading 3</h1>
            <p>Heading 4</p>
        </div>
    </body>
    ```

*   **index.php**

    ```
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Create rule as a string
    $RNG = "<element name=\"body\"
    xmlns=\"http://relaxng.org/ns/structure/1.0\">
    <zeroOrMore>
      <element name=\"div\">
        <element name=\"h1\">
          <text/>
        </element>
        <element name=\"p\">
          <text/>
        </element>
      </element>
    </zeroOrMore>
    </element>";

    // Load the rule
    $XMLReader->setRelaxNGSchemaSource($RNG);

    // Iterate through the XML nodes
    while ($XMLReader->read()) {
        if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

            // Check if XML follows the relaxNG rule
            if ($XMLReader->isValid()) {
                echo "This document is valid!<br>";
            }

        }
    }
    ?>
    ```

*   **output:**

    ```
    This document is valid!
    This document is valid!
    This document is valid!
    This document is valid!
    This document is valid!
    This document is valid!
    This document is valid!
    ```

示例 2：

*   **data.xml**

    ```
    <?xml version="1.0"?>
    <body>
        <div>
            <!--Create empty div element
               to violate rule-->
        </div>
        <div>
            <h1>Heading 3</h1>
            <h2>Heading 4</h2>
        </div>
    </body>
    ```

*   **index.php**

    ```
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Create rule as a string
    $RNG = "<element name=\"body\"
    xmlns=\"http://relaxng.org/ns/structure/1.0\">
    <zeroOrMore>
      <element name=\"div\">
        <element name=\"h1\">
          <text/>
        </element>
        <element name=\"h2\">
          <text/>
        </element>
      </element>
    </zeroOrMore>
    </element>";

    // Load the rule
    $XMLReader->setRelaxNGSchemaSource($RNG);

    // Iterate through the XML nodes
    while ($XMLReader->read()) {
        if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

            // Check if XML follows the relaxNG rule
            if (!$XMLReader->isValid()) {
                echo "This document is not valid!<br>";
            }

        }
    }
    ?>
    ```

*   **output:**

    ```
    This document is not valid!
    This document is not valid!
    This document is not valid!
    ```

**引用：**[https://www.php.net/manual/en/xmlreader.setrelaxngschemasource.php](https://www.php.net/manual/en/xmlreader.setrelaxngschemasource.php)