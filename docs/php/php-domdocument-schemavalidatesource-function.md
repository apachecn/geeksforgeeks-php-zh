# PHP|DOMDocument schemaValidateSource()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-schemavalidatesource-function/](https://www.geeksforgeeks.org/php-domdocument-schemavalidatesource-function/)

**DOMDocument：：schemaValidateSource()函数**是 PHP 中的内置函数，用于根据给定字符串中定义的模式验证文档。 *schemaValidation()*和*schemaValidateSource()*的区别在于前者接受模式文件名，而后者可以接受字符串形式的模式。

**语法：**

```
*bool* DOMDocument::schemaValidateSource( *string* $source, *int* $flags = 0 )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$source:** it specifies the string that contains the schema.
*   **$FLAGS (optional):** it specifies the validation flag.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**DOMDocument：：schemaValidateSource()函数**：

**程序 1：**

```
<?php

// Create a new DOMDocument
$doc = new DOMDocument;

// XSD schema
$XSD = "<?xml version=\"1.0\"?>
<xs:schema xmlns:xs=\"http://www.w3.org/2001/XMLSchema\"
elementFormDefault=\"qualified\">
    <xs:element name=\"body\">
        <xs:complexType>
            <xs:sequence>
                <xs:element name=\"h1\" type=\"xs:string\"/>
                <xs:element name=\"strong\" type=\"xs:integer\"/>
            </xs:sequence>
        </xs:complexType>
    </xs:element>
</xs:schema>";

// Load the XML
$doc->loadXML("<?xml version=\"1.0\"?>
<body>
    <h1> Hello </h1>
    <strong> 22 </strong>
</body>");

// Check if XML follows the schema rule
if ($doc->schemaValidateSource($XSD)) {
    echo "This document is valid!\n";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new DOMDocument
$doc = new DOMDocument;

// RNG schema
$XSD = "<?xml version=\"1.0\"?>
<xs:schema xmlns:xs=\"http://www.w3.org/2001/XMLSchema\"
elementFormDefault=\"qualified\">
    <xs:element name=\"student\">
        <xs:complexType>
            <xs:sequence>
                <xs:element name=\"name\" type=\"xs:string\"/>
                <xs:element name=\"rollno\" type=\"xs:integer\"/>
            </xs:sequence>
        </xs:complexType>
    </xs:element>
</xs:schema>";

// Load the XML
$doc->loadXML("<?xml version=\"1.0\"?>
<student> 
    <!-- rollnow element is missing here -->
    <name> XYZ </name>
</student>
");

// Check if XML follows the relaxNG rule
if (!$doc->schemaValidateSource($XSD)) {
    echo "This document is not valid!\n";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domdocument.schemavalidatesource.php](https://www.php.net/manual/en/domdocument.schemavalidatesource.php)