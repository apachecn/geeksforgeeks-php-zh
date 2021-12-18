# PHP|Gmagick removeimageprofile()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-removeimageprofile-function/](https://www.geeksforgeeks.org/php-gmagick-removeimageprofile-function/)

**Gmagick：：removeimageprofile()函数**是 PHP 中的一个内置函数，用于删除命名的图像配置文件并返回它。 此函数的工作方式类似于堆栈数据结构的 POP 函数，因为它提供 Profile 的值并将其从图像中删除。

**语法：**

```
*string* Gmagick::removeimageprofile( *string* $name )
```

**参数：**此函数接受单个参数**$name**，该参数保存要删除的配置文件的名称。

**返回值：**此函数返回包含配置文件图像值的字符串值。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：removeimageprofile()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a profile
$gmagick->setimageprofile('profile_name', 'profile_value');

echo '<b>Before removing:</b> <br>';

// Test it using the function
testProfile($gmagick, 'profile_name');

// Remove the profile
$gmagick->removeimageprofile('profile_name');

echo '<b>After removing:</b> <br>';
// Test again if it is removed or not.
testProfile($gmagick, 'profile_name');

// Function to check if a profile is removed or not
function testProfile($gmagick, $name) {

    try {
        $value = $gmagick->getimageprofile('profile_name');
        echo 'Profile is available with name <i>' . $name .
                ' </i>and value <i>' . $value . '</i><br>';

    } catch (Exception $e) {
        echo 'Profile is not available.<br>';
    }
}
?>
```

发帖主题：Re：Колибри0.7.0

```
Before removing:
Profile is available with name *profile_name* and value *profile_value*
After removing:
Profile is not available.
```

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the Image Profiles
$gmagick->setimageprofile('borderColor1', 'green');
$gmagick->setimageprofile('borderColor2', 'red');

// Use the Image Profile
$gmagick->borderImage($gmagick->getImageProfile('borderColor1'), 6, 6);

// Use the Image Profile
$gmagick->borderImage($gmagick->getImageProfile('borderColor2'), 6, 6);

// Removing the profiles after use for memory efficiency
$gmagick->removeimageprofile('borderColor1');
$gmagick->removeimageprofile('borderColor2');

// Display the image
header("Content-Type: image/png");
echo $gmagick;
?>
```

**输出：**
![](img/0b724d65a0280d5550a521ab55b528dc.png)

**引用：**[https://www.php.net/manual/en/gmagick.removeimageprofile.php](https://www.php.net/manual/en/gmagick.removeimageprofile.php)