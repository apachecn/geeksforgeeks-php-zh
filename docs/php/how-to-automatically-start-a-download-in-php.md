# 如何在 PHP 中自动开始一次下载？

> 原文:[https://www . geesforgeks . org/如何自动启动 php 下载/](https://www.geeksforgeeks.org/how-to-automatically-start-a-download-in-php/)

这篇文章涉及创建一个开始使用 PHP 下载文件。这个想法是做一个下载按钮，它会将你重定向到另一个页面，PHP 脚本会自动开始下载。

**创建下载按钮:**

```html
<!DOCTYPE html>
<html>

<head>
    <meta name="viewport" content=
        "width=device-width, initial-scale=1">
    <style>
        .btn {
            background-color: limeGreen;
            border: none;
            color: white;
            padding: 12px 30px;
            cursor: pointer;
            font-size: 20px;
        }

        .btn:hover {
            background-color: green;
        }
    </style>
</head>

<body>
    <center>
        <p>Auto width:</p>
        <button class="btn">
            <i class="fa fa-download">Download</i>
        </button>
        <p>Full width:</p>
        <button class="btn" style="width:100%">
            <i class="fa fa-download">Download</i>
        </button>
    </center>
</body>

</html>
```

**输出:**
![](img/27f9dbfecb83252cb8b4a409554531c9.png)

要重定向到要下载文件的某个文件，请创建一个如下所示的 HTML 表单。

```html
<form action="downloadFile.php" method="post">
 <input type="submit" name="submit" value="Download" />
</form>
```

**输出:**
![](img/1a27f52b695733697d54bce90c07041f.png)

**要下载的 PHP 代码:**当用户点击上述按钮时，代码将被重定向到“downloadFile.php”文件。现在，使用文件的网址和 PHP **file_get_contents()** 函数下载文件。

```html
<?php 

// Initialize a file URL to 
// the variable 
$url = 
'https://contribute.geeksforgeeks.org/wp-content/uploads/gfg-40.png'; 

// Use basename() function to 
// return the file  
$file_name = basename($url); 

// Use file_get_contents() function 
// to get the file from url and use 
// file_put_contents() function to 
// save the file by using base name 
if(file_put_contents( $file_name, 
      file_get_contents($url))) { 
    echo "File downloaded successfully"; 
} 
else { 
    echo "File downloading failed."; 
}
?> 
```

**输出:**

*   **运行程序前:**
    ![](img/7072ad91decbdddbf2f10a310003d67f.png)
*   **运行程序后:**
    ![](img/e2d136d28363514d6f1434bbadfdae66.png)