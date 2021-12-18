# PHP|Imagick profileImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-profileimage-function/](https://www.geeksforgeeks.org/php-imagick-profileimage-function/)

Imagick：：profileImage()函数是 PHP 中的一个内置函数，用于在图像中添加或删除配置文件。 如果配置文件为空，则将其从以其他方式添加的映像中删除。
**关于 ICC 图像配置文件：**在色彩管理中，ICC 配置文件是根据国际色彩联盟(ICC)发布的标准描述色彩输入或输出设备或色彩空间的一组数据。 颜色空间是指颜色的特定组织。
**语法：**和

```php
*bool* Imagick::profileImage( $name, $profile )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$name：**此参数保存图像配置文件的名称。
*   **$profile：**此参数保存配置文件的内容。

**返回值：**如果成功，此函数返回 TRUE。
下面的程序说明了 PHP：
**程序：**和
中的 Imagick：：profileImage()函数

## PHP

```php
<?php

// Create an Imagick object
$image = new Imagick(
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png");

// Get profiles attached to the image
$profiles = $image->getImageProfiles('*', false);

// Checking for any icc profile added to the image
$has_icc_profile = (array_search('icc', $profiles) !== false);

if ($has_icc_profile === false) {

    // If image does not have ICC profile, then add one
    $icc = file_get_contents('D:\\Merawamp\\www\\New\\to\\icc\\CMYK.icc');

    // Use Imagick::profileimage() function to add the
    // profile to an image the profile added to the
    // image is the file D:\\Merawamp\\www\\New\\to\\icc\\CMYK.icc
    $trip1 = $image->profileImage('icc', $icc);
}

// If method runs successfully it returns true
if($trip1 == true) {
    echo "Profile added to image successfully";
}

?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/b462a21d1bc5284e593629ff3d60bedb.png)