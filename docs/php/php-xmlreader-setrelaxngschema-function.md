# PHP|XMLReader setRelaxNGSchema()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-setrelaxngschema-function/](https://www.geeksforgeeks.org/php-xmlreader-setrelaxngschema-function/)

**XMLReader：：setRelaxNGSchema()函数**是 PHP 中的一个内置函数，用于设置用于验证的 RelaxNG 模式的文件名或 URI。

**语法：**

```php
*bool* XMLReader::setRelaxNGSchema( *string* $filename )
```

**参数：**此函数接受单个参数**$filename**，该参数保存指向 RelaxNG 模式的文件名或 URI。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明 PHP 中的**XMLReader：：setRelaxNGSchema()函数**：

**Example 1:**
*   **data.xml**(待验证的 XML 文件)

    ```php
    <?xml version="1.0"?>
    <body>
        <div>
            <h1>Heading 1</h1>
            <h2>Heading 2</h2>
        </div>
        <div>
            <h1>Heading 3</h1>
            <h2>Heading 4</h2>
        </div>
    </body>
    ```

*   **rule.rng**(XML 文件要遵循的规则)

    ```php
    <element name="body" 
      xmlns="http://relaxng.org/ns/structure/1.0">
      <zeroOrMore>
        <element name="div">
          <element name="h1">
            <text/>
          </element>
          <element name="h2">
            <text/>
          </element>
        </element>
      </zeroOrMore>
    </element>
    ```

*   **index.php**(运行验证器的 PHP 脚本)

    ```php
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Load the rule file
    $XMLReader->setRelaxNGSchema('rule.rng');

    // Iterate through the XML nodes
    // and validate each node
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

*   发帖主题：Re：Колибри0.7.8.0

**程序 2：**

*   **data.xml**

    ```php
    <?xml version="1.0"?>
    <body>
        <div>
            <!--Remove Heading 1
              to violate rule-->
            <h2>Heading 2</h2>
        </div>
        <div>
            <h1>Heading 3</h1>
            <h2>Heading 4</h2>
        </div>
    </body>
    ```

*   **rule.rng**

    ```php
    <element name="body"
      xmlns="http://relaxng.org/ns/structure/1.0">
      <zeroOrMore>
        <element name="div">
          <element name="h1">
            <text/>
          </element>
          <element name="h2">
            <text/>
          </element>
        </element>
      </zeroOrMore>
    </element>
    ```

*   **index.php**

    ```php
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Load the rule file
    $XMLReader->setRelaxNGSchema('rule.rng');

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

**引用：**[https://www.php.net/manual/en/xmlreader.setrelaxngschema.php](https://www.php.net/manual/en/xmlreader.setrelaxngschema.php)