# PHP|DOMDocument xinclude()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-xinclude-function/](https://www.geeksforgeeks.org/php-domdocument-xinclude-function/)

**DOMDocument：：xinclude()函数**是 PHP 中的一个内置函数，用于替换 DOMDocument 对象中的 XIncludes。

**语法：**

```
*int* DOMDocument::xinclude( *int* $options = 0 )
```

**参数：**此函数接受一个可选的单个参数**$options**，该参数保存 libxml 参数。

**返回值：**此函数返回文档中的 XIncludes 数，如果某些处理失败，则返回-1；如果没有替换，则返回 False。

下面的示例说明了 PHP 中的**DOMDocument：：xinclude()函数**：

**示例 1：**在本程序中，我们将包含从 new.xml 到 index.php 的 XML。

*   **new.xml**

    ```
    <?xml version='1.0'?>
    <disclaimer>
      <p>
        This is the content from new.xml
        included using xinclude.
      </p>
    </disclaimer>
    ```

*   **index.php**

    ```
    <?php
    $xml = <<<EOD
    <?xml version="1.0" ?>
    <root xmlns:xi="http://www.w3.org/2001/XInclude">
      <xi:include href="new.xml">
      </xi:include>
    </root>
    EOD;

    // Create a new DOMDocument
    $dom = new DOMDocument();

    // let's have a nice output
    $dom->preserveWhiteSpace = false;
    $dom->formatOutput = true;

    // load the XML string defined above
    $dom->loadXML($xml);

    // substitute xincludes
    $dom->xinclude();

    echo $dom->saveXML();
    ?>
    ```

*   **output:**

    ```
    This is the content from new.xml included using xinclude.
    ```

**示例 2：**在此程序中，如果 xinclude 失败，我们将添加一个后备。

*   **index.php**

    ```
    <?php
    $xml = <<<EOD
    <?xml version="1.0" ?>
    <root xmlns:xi="http://www.w3.org/2001/XInclude">
      <xi:include href="wrong_name.xml">
       <xi:fallback>
        <error>xml not found</error>
       </xi:fallback>
      </xi:include>
    </root>
    EOD;

    // Create a new DOMDocument
    $dom = new DOMDocument();

    // let's have a nice output
    $dom->preserveWhiteSpace = false;
    $dom->formatOutput = true;

    // load the XML string defined above
    $dom->loadXML($xml);

    // substitute xincludes
    $dom->xinclude();

    echo $dom->saveXML();
    ?>
    ```

*   **output:**

    ```
    xml not found
    ```

**引用：**[https://www.php.net/manual/en/domdocument.xinclude.php](https://www.php.net/manual/en/domdocument.xinclude.php)