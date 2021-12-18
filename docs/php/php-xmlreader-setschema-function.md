# PHP|XMLReader setSchema()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-setschema-function/](https://www.geeksforgeeks.org/php-xmlreader-setschema-function/)

**XMLReader：：setSchema()函数**是 PHP 中的一个内置函数，用于使用 XSD 模式验证文档。 这个 XSD 模式只是一个定义 XML 结构规则的文件，应该是.xsd 文件的形式。

**语法：**

```php
*bool* XMLReader::setSchema( *string* $filename )
```

**参数：**此函数接受保存 XSD 文件名的单个参数**$filename**。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**异常：**如果在没有架构支持的情况下编译 libxml 扩展，则此函数引发 E_WARNING。

下面的示例说明了 PHP 中的**XMLReader：：setSchema()函数**：

示例 1：

*   **data.xml** (XML file to be verified)

    ```php
    <?xml version="1.0"?>
    <student>
        <name>Rahul</name>
        <rollno>1726262</rollno>
    </student>
    ```

*   **rule.xsd** (rules to be followed by XML files)

    ```php
    <?xml version="1.0"?>
    <xs:schema xmlns:xs=
          "http://www.w3.org/2001/XMLSchema"
    elementFormDefault="qualified">
        <xs:element name="student">
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="name"
                        type="xs:string"/>
                    <xs:element name="rollno"
                       type="xs:integer"/>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
    </xs:schema>
    ```

*   **index.php** (the PHP script to run.

    ```php
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Load the rule
    $XMLReader->setSchema('rule.xsd');

    // Iterate through the XML nodes
    while ($XMLReader->read()) {
        if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

            // Check if XML follows the XSD rule
            if ($XMLReader->isValid()) {
                echo "This document is valid!<br>";
            }

        }
    }
    ?>
    ```

*   **output:**

    ```php
    This document is valid!
    This document is valid!
    This document is valid!
    ```

**示例 2：**

*   **data.xml**

    ```php
    <?xml version="1.0"?>
    <div>
        <phoneNo>This should not be text</phoneNo>
    </div>
    ```

*   **rule.xsd**

    ```php
    <?xml version="1.0"?>
    <xs:schema xmlns:xs=
          "http://www.w3.org/2001/XMLSchema"
    elementFormDefault="qualified">
        <xs:element name="div">
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="phoneNo"
                       type="xs:integer"/>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
    </xs:schema>
    ```

*   **index.php**

    ```php
    <?php

    // Create a new XMLReader instance
    $XMLReader = new XMLReader();

    // Open the XML file
    $XMLReader->open('data.xml');

    // Load the rule
    $XMLReader->setSchema('rule.xsd');

    // Iterate through the XML nodes
    while ($XMLReader->read()) {
        if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

            // Check if XML follows the XSD rule
            if (!$XMLReader->isValid()) {
                echo "This document is not valid!<br>";
            }

        }
    }
    ?>
    ```

*   **output:**

**引用：**[https://www.php.net/manual/en/xmlreader.setschema.php](https://www.php.net/manual/en/xmlreader.setschema.php)