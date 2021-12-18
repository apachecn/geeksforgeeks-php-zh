# PHP | $_FILES 数组(HTTP 文件上传变量)

> 原文:[https://www . geesforgeks . org/PHP-_ files-array-http-file-upload-variables/](https://www.geeksforgeeks.org/php-_files-array-http-file-upload-variables/)

PHP 文件句柄是如何知道一些基本信息的，比如文件名、文件大小、文件类型以及关于选择上传的文件的一些属性？让我们看看幕后在演什么。
**$_FILES** 是通过 [HTTP POST](https://www.geeksforgeeks.org/http-get-post-methods-php/) 方法上传的项目的二维关联全局数组，保存文件的属性，例如:

| 属性 | 描述 |
| --- | --- |
| [姓名] | 正在上传的文件的名称 |
| [尺寸] | 文件的大小 |
| [类型] | 文件的类型(如。pdf，。拉上拉链。jpeg…..等等) |
| [tmp_name] | 处理上传请求前文件所在的临时地址 |
| [错误] | 上传文件时出现的错误类型 |

现在看看这个数组是什么样子的？？

```
 *   $ _ FILES[输入字段名称][名称]
*   $ _ FILES[输入字段名][tmp_name]
*   $ _ FILES[输入字段名称][大小]
*   $ _ FILES[输入字段名称][类型]
*   $ _ FILES[输入字段名称][错误] 
```

让我们看一下例子，在第一个例子中这个数组是如何工作的。
**例 1 :**

```
<?php
   echo "<pre>";
   print_r($_FILES);
   echo "</pre>";
   ?>
<form action="" method="post" enctype="multipart/form-data">
   <input type="file" name="file">
   <input type="submit" value="Upload Image">
</form>
```

在上面的脚本中，在上传文件之前

当我们选择文件并上传后，函数 **[print_r](https://www.geeksforgeeks.org/php-print_r-function/)** 将显示 PHP 超全局关联数组$_FILES 的信息。

**示例 2 :** 添加 html 代码后跟 PHP 脚本不同的文件。让我们制作一个上传文件的 HTML 表单
T3【index.html】T4

```
<!DOCTYPE html>
<html>
  <head>
    <title>GeeksForGeeks</title>
    <style type="text/css">
      div
      {
      background: #4CB974;
      text-align: center;
      font-size: 20px;
      padding: 30px;
      color: #fff;
      font-family: sans-serif;
      }
    </style>
  </head>
  <body>
    <form action="file-upload-manager.php" method="post" 
     enctype="multipart/form-data" style="border: 1px solid #1f1f1f;
       padding: 20px; position: absolute; top: 50%; left: 50%; 
          transform: translate(-50%, -50%);">
      <!--multipart/form-data ensures that form
        data is going to be encoded as MIME data-->

      <h2>Upload File</h2>
      <input type="file" name="photo" id="fileSelect"><br><br>
      <input type="submit" name="submit" value="Upload"><br><br>
      <!-- name of the input fields are going to be used in our php script-->
      <div> This Video is made for GFG</div>
    </form>
  </body>
</html>
```

现在，是时候编写一个能够处理文件上传系统的 php 脚本了。
**file-upload-manager.php**

```
<?php
// Check if the form was submitted
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    // Check if file was uploaded without errors
    if (isset($_FILES["photo"]) && $_FILES["photo"]["error"] == 0) {

        $file_name     = $_FILES["photo"]["name"];
        $file_type     = $_FILES["photo"]["type"];
        $file_size     = $_FILES["photo"]["size"];
        $file_tmp_name = $_FILES["photo"]["tmp_name"];
        $file_error    = $_FILES["photo"]["error"];

        echo "<div style='text-align: center; background: #4CB974; 
        padding: 30px 0 10px 0; font-size: 20px; color: #fff'>
        File Name: " . $file_name . "</div>";

        echo "<div style='text-align: center; background: #4CB974; 
        padding: 10px; font-size: 20px; color: #fff'>
        File Type: " . $file_type . "</div>";

        echo "<div style='text-align: center; background: #4CB974; 
        padding: 10px; font-size: 20px; color: #fff'>
        File Size: " . $file_size . "</div>";

        echo "<div style='text-align: center; background: #4CB974; 
        padding: 10px; font-size: 20px; color: #fff'>
        File Error: " . $file_error . "</div>";

        echo "<div style='text-align: center; background: #4CB974; 
        padding: 10px; font-size: 20px; color: #fff'>
        File Temporary Name: " . $file_tmp_name . "</div>";

    }
}
?>
```

在上面的脚本中，一旦我们提交了表单，稍后我们就可以通过一个 PHP 超全局关联数组$_FILES 访问信息。除了使用$_FILES 数组之外，许多内置函数也发挥了重要作用。在我们完成上传文件后，在脚本中我们将检查服务器的请求方法，如果是开机自检，那么它将继续，否则系统将抛出一个错误。稍后，我们访问了$_FILES 数组来获取文件名、文件大小和文件类型。一旦我们获得了这些信息，使用[回显](https://www.geeksforgeeks.org/php-echo-print/)打印文件的信息。

**输出:**

<video class="wp-video-shortcode" id="video-200827-1" width="665" height="233" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/uploads/file_array-1.webm?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/file_array-1.webm](https://media.geeksforgeeks.org/wp-content/uploads/file_array-1.webm)</video>

**参考:**T2】http://php.net/manual/en/reserved.variables.files.php