# PHP|ReflectionExtension__toString()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-__tostring-function/](https://www.geeksforgeeks.org/php-reflectionextension-__tostring-function/)

**ReflectionExtension：：__toString()函数**是 PHP 中的内置函数，用于返回指定扩展对象的字符串表示形式。

**语法：**

```
ReflectionExtension::__toString()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定扩展对象的字符串表示形式。

以下程序说明 PHP：
**Program_1：**中的 ReflectionExtension：：__toString()函数

```
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the __toString() function
$B = $extension->__toString();

// Getting the string representation of
// the specified extension object.
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```
string(98219) "Extension [ <persistent> extension #18 dom version 20031129 ] {

  - Dependencies {
    Dependency [ libxml (Required) ]
    Dependency [ domxml (Conflicts) ]
  }

  - Constants [45] {
    Constant [ integer XML_ELEMENT_NODE ] { 1 }
    . . .
    Constant [ integer DOM_VALIDATION_ERR ] { 16 }
  }

        Method [ <internal:dom, inherits DOMNode> public method setUserData ] {

          - Parameters [3] {
            Parameter #0 [ <required> $key ]
            Parameter #1 [ <required> $data ]
            Parameter #2 [ <required> $handler ]
          }
        }
        . . .

        Method [ <internal:dom> public method registerPhpFunctions ] {

          - Parameters [0] {
          }
        }
      }
    }
  }
}
"

```

**程序 _2：**

```
<?php

// Using ReflectionExtension() over 
// an extension xml
$extension = new ReflectionExtension('xml');

// Calling the __toString() function and
// Getting the string representation of
// the specified extension object.
var_dump($extension->__toString());
?>
```

发帖主题：Re：Колибри0.7.0

```
string(6209) "Extension [ <persistent> extension #15 xml version 7.0.33-0ubuntu0.16.04.7 ] {

  - Dependencies {
    Dependency [ libxml (Required) ]
  }

  - Constants [27] {
    Constant [ integer XML_ERROR_NONE ] { 0 }
    . . .
    Constant [ string XML_SAX_IMPL ] { libxml }
  }

  - Functions {
    Function [ <internal:xml> function xml_parser_create ] {

      - Parameters [1] {
        Parameter #0 [ <optional> $encoding ]
      }
    }
    . . . 
    Function [ <internal:xml> function utf8_decode ] {

      - Parameters [1] {
        Parameter #0 [ <required> $data ]
      }
    }
  }
}
"

```

**引用：**[https://www.php.net/manual/en/reflectionextension.tostring.php](https://www.php.net/manual/en/reflectionextension.tostring.php)