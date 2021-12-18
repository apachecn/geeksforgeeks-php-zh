# PHP|DOMDocument schemaValidation()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-schemavalidate-function/](https://www.geeksforgeeks.org/php-domdocument-schemavalidate-function/)

**DOMDocument：：schemaValify()函数**是 PHP 中的一个内置函数，用于根据给定的模式文件验证文档。 模式文件可以是 W3C(万维网联盟)推荐的 XSD 格式。

**语法：**

```php
*bool* DOMDocument::schemaValidate( *string* $filename, *int* $flags = 0 )
```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$filename:** it specifies the path to the schema.
*   **$FLAGS (optional):** it specifies the validation flag.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**DOMDocument：：schemaValify()函数**：

**程序 1：**

*   **File name: rule.xsd**

    ```php
    <?xml version="1.0"?>
    <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema"
    elementFormDefault="qualified">
        <xs:element name="student">
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="name" type="xs:string"/>
                    <xs:element name="rollno" type="xs:integer"/>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
    </xs:schema>
    ```

*   **File name: index.php**

    ```php
    <?php

    // Create a new DOMDocument
    $doc = new DOMDocument;

    // Load the XML
    $doc->loadXML("<?xml version=\"1.0\"?>
    <student>
        <name>Rahul </name>
        <rollno>34</rollno>
    </student>");

    // Check if XML follows the rule
    if ($doc->schemaValidate('rule.xsd')) {
        echo "This document is valid!\n";
    }
    ?>
    ```

*   **output:**

    ```php
    This document is valid!
    ```

**程序 2：**

*   **File name: rule.xsd**

    ```php
    <?xml version="1.0"?>
    <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema"
    elementFormDefault="qualified">
        <xs:element name="body">
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="h1" type="xs:string"/>
                    <xs:element name="strong" type="xs:integer"/>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
    </xs:schema>
    ```

*   **File name: index.php**

    ```php
    <?php

    // Create a new DOMDocument
    $doc = new DOMDocument;

    // Load the XML
    $doc->loadXML("<?xml version=\"1.0\"?>
    <student>
        <h1>Rahul </h1>
    </student>");

    // Check if XML follows the rule
    if (!$doc->schemaValidate('rule.xsd')) {
        echo "This document is not valid!\n";
    }
    ?>
    ```

*   **output:**

    ```php
    This document is not valid!
    ```

**引用：**[https://www.php.net/manual/en/domdocument.schemavalidate.php](https://www.php.net/manual/en/domdocument.schemavalidate.php)