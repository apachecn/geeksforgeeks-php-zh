# PHP|DOMDocument RELANGVALIDATE()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-relaxngvalidate-function/](https://www.geeksforgeeks.org/php-domdocument-relaxngvalidate-function/)

**DOMDocument：：relasNGValify()函数**是 PHP 中的一个内置函数，用于对文档执行 RELANNG 验证。 松弛 NG 是 DDT 的替代方法，它定义了 XML 文档需要遵循的结构。

**语法：**

```php
*bool* DOMDocument::relaxNGValidate( *string* $filename )
```

**参数：**此函数接受保存 RNG 文件的单个参数**$fileName**。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序说明了 PHP 中的**DOMDocument：：relasNGValify()函数**：

**程序 1：**

*   **File name: rule.rng**

    ```php
    <element name="college" 
      xmlns="http://relaxng.org/ns/structure/1.0">
      <zeroOrMore>
        <element name="rollno">
          <element name="name">
            <text/>
          </element>
          <element name="subject">
            <text/>
          </element>
        </element>
      </zeroOrMore>
    </element>
    ```

*   **File name: index.php**

    ```php
    <?php

    // Create a new DOMDocument
    $doc = new DOMDocument;

    // Load the XML
    $doc->loadXML("<?xml version=\"1.0\"?>
    <college>
      <rollno>
        <name>John Smith</name>
        <subject>Web</subject>
      </rollno>
      <rollno>
        <name>John Doe</name>
        <subject>CSE</subject>
      </rollno>
    </college>");

    // Check if XML follows the relaxNG rule
    if ($doc->relaxNGValidate('rule.rng')) {
        echo "This document is valid!\n";
    }
    ?>
    ```

*   **output:**

    ```php
    This document is valid!
    ```

**程序 2：**

*   **File name: rule.rng**

    ```php
    <element name="company" 
      xmlns="http://relaxng.org/ns/structure/1.0">
      <zeroOrMore>
        <element name="employee">
          <element name="name">
            <text/>
          </element>
          <element name="salary">
            <text/>
          </element>
        </element>
      </zeroOrMore>
    </element>
    ```

*   **File name: index.php**

    ```php
    <?php

    // Create a new DOMDocument
    $doc = new DOMDocument;

    // Load the XML
    $doc->loadXML("<?xml version=\"1.0\"?>
    <company>
      <employee>
        <name>John Smith</name>
        <salary>Web</salary>
      </employee>
      <employee>
        <!-- Do not add salary to voilate rule -->
        <name>John Doe</name>
      </employee>
    </company>");

    // Check if XML doesn't follows the relaxNG rule
    if (!$doc->relaxNGValidate('rule.rng')) {
        echo "This document is not valid!\n";
    }
    ?>
    ```

*   **output:**

    ```php
    This document is not valid!
    ```

**引用：**[https://www.php.net/manual/en/domdocument.relaxngvalidate.php](https://www.php.net/manual/en/domdocument.relaxngvalidate.php)