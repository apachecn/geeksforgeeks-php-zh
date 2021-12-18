# 如何用 HTML 和 PHP 选择上传多个文件，使用 HTTP POST？

> 原文:[https://www . geesforgeks . org/如何使用-http-post/](https://www.geeksforgeeks.org/how-to-select-and-upload-multiple-files-with-html-and-php-using-http-post/) 使用-html 和-php 选择和上传多个文件

在本文中，我们将看看如何用 HTML 和 PHP 上传多个文件。多重图像上传允许用户一次选择多个文件，并将所有文件上传到服务器。

**index.html**创建一个简单的 HTML 页面，选择多个文件，提交到服务器上传文件。这里，HTML 文件包含一个表单，可以使用 POST 方法选择和上传文件。

## HTML

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Select and upload multiple
        files to the server
    </title>
</head>

<body>

    <!-- multipart/form-data ensures that form
    data is going to be encoded as MIME data -->
    <form action="file_upload.php" method="POST"
            enctype="multipart/form-data">

        <h2>Upload Files</h2>

<p>
            Select files to upload:

            <!-- name of the input fields are going to
                be used in our php script-->
            <input type="file" name="files[]" multiple>

            <br><br>

            <input type="submit" name="submit" value="Upload" >
        </p>

    </form>
</body>

</html>                   
```

**file _ upload . PHP**file _ upload . PHP 脚本将处理文件上传并显示上传状态。

## PHP

```
<?php

// Check if form was submitted
if(isset($_POST['submit'])) {

    // Configure upload directory and allowed file types
    $upload_dir = 'uploads'.DIRECTORY_SEPARATOR;
    $allowed_types = array('jpg', 'png', 'jpeg', 'gif');

    // Define maxsize for files i.e 2MB
    $maxsize = 2 * 1024 * 1024;

    // Checks if user sent an empty form
    if(!empty(array_filter($_FILES['files']['name']))) {

        // Loop through each file in files[] array
        foreach ($_FILES['files']['tmp_name'] as $key => $value) {

            $file_tmpname = $_FILES['files']['tmp_name'][$key];
            $file_name = $_FILES['files']['name'][$key];
            $file_size = $_FILES['files']['size'][$key];
            $file_ext = pathinfo($file_name, PATHINFO_EXTENSION);

            // Set upload file path
            $filepath = $upload_dir.$file_name;

            // Check file type is allowed or not
            if(in_array(strtolower($file_ext), $allowed_types)) {

                // Verify file size - 2MB max
                if ($file_size > $maxsize)        
                    echo "Error: File size is larger than the allowed limit.";

                // If file with name already exist then append time in
                // front of name of the file to avoid overwriting of file
                if(file_exists($filepath)) {
                    $filepath = $upload_dir.time().$file_name;

                    if( move_uploaded_file($file_tmpname, $filepath)) {
                        echo "{$file_name} successfully uploaded <br />";
                    }
                    else {                    
                        echo "Error uploading {$file_name} <br />";
                    }
                }
                else {

                    if( move_uploaded_file($file_tmpname, $filepath)) {
                        echo "{$file_name} successfully uploaded <br />";
                    }
                    else {                    
                        echo "Error uploading {$file_name} <br />";
                    }
                }
            }
            else {

                // If file extension not valid
                echo "Error uploading {$file_name} ";
                echo "({$file_ext} file type is not allowed)<br / >";
            }
        }
    }
    else {

        // If no files selected
        echo "No files selected.";
    }
}

?>
```