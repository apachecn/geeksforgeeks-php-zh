# PHP|封装

> Original: [https://www.geeksforgeeks.org/php-encapsulation/](https://www.geeksforgeeks.org/php-encapsulation/)

在当今的技术世界，维护隐私已成为保护重要数据的苛刻需求之一。 每当在一个函数中修改的数据影响到其他函数时，就会在任何软件中造成很多问题。 为了解决这个问题，PHP 中的面向对象编程使用了封装的概念。

因此，PHP 中封装的 OOPS 概念意味着，封装对象的内部细节以保护其不受外部来源的影响。 它描述了将类、数据变量和成员函数结合在一起在单个单元内处理数据以形成一个对象。 否则，它就是在单个类单元中捆绑属性和行为。

数据不是直接访问的，事实上，它们是通过类中编写的函数(get 或 set)访问的。 属性是私有的，但 getter(Get)和 setter(Set)方法是公共的，用于操作这些属性。

**PHP 封装程序：**以下程序中的方法或函数是更新密码和检查课程名称。 GFG 类定义了与 GFG 用户相关的所有操作。

```php
<?php

// PHP program to implements encapsulation
class GFG {

    private $userId;
    private $pwd;

    // Update GFG password
    public function updatePwd($userId, $pwd) {

        // Write function body
        echo("Function to update password '"
                . $pwd . "' for user " . $userId);

        echo "<br>";
    }

    // Check account balance
    public function courseName($userId) {

        // Write function body
        echo("Function to check course name of user "
                . $userId);

        echo "<br>";
    }
}

$obj = new GFG();
$obj -> updatePwd('GFG12', 'geeks54321');
$obj -> courseName('GFG06');

?>
```

发帖主题：Re：Колибри0.7.0

```php
Function to update password 'geeks54321' for user GFG12
Function to check course name of user GFG06

```

**注意：**外部最终用户无法访问数据成员和类属性。 因此他们不能更改属性。

**访问变量**的程序

```php
<?php

class Student {
    private $firstname;
    private $gender;

    public function getFirstName() {
        return $this->firstname;
    }

    public function setFirstName($firstname) {
        $this->firstname = $firstname;
        echo("First name is set to ".$firstname);
        echo("<br>");
    }

    public function getGender() {
        return $this->gender;
    }

    public function setGender($gender) {
        if ('Male' !== $gender and 'Female' !== $gender) {
            echo('Set gender as Male or Female for gender');
        }

        $this->gender = $gender;
        echo("Gender is set to ".$gender);
        echo("<br>");
    }
}

$student = new Student();
$student->setFirstName('Meena');
$student->setGender('Female');

?>
```

发帖主题：Re：Колибри0.7.0

```php
First name is set to Meena
Gender is set to Female

```

**注：**

*   如果对象的属性是私有的，并通过公共方法更新它们，则可以使用封装。
*   PHP 中的封装可以通过实现访问说明符来实现。
*   OOPS 的继承概念非常谨慎，因为很多时候继承都会破坏封装的概念。
*   继承公开了父类的一些细节，有效地打破了封装。

**封装优势：**

*   **Data Hiding and Abstraction:** Unnecessary details, internal representation and implementation are hidden from the end-users for protection of data structure and the Class. Data access is prohibited from members of other classes by creating private methods. It protects the internal state of any object by keeping member variables private and preventing any inconsistent state. It is the enclosing of data and related operations into that object.

    **注意：**封装用于对客户端隐藏内部视图。

*   **数据安全性：**封装有助于使数据非常健壮和安全，因为数据和成员函数被包装在一起形成一个对象。 所有的任务都是在里面完成的，没有任何外界的担忧，这也让生活变得非常容易。
*   **降低复杂性：**封装通过隐藏实现的细节并公开方法或操作，有助于降低软件的开发复杂性。
*   **可重用性：**有一些实例，您不必重写从父类继承的相同功能。
*   **可靠性：**您可以通过编写 set 或 get 方法使类成为只读或只写。
*   **更容易测试代码：**封装的 PHP 代码很容易测试，因为用于测试子类的函数也确保了父类函数的测试。
*   **更高的灵活性：**可以通过 GET 或 SET 方法访问类变量，提高了灵活性。 它易于维护，因为可以在不更改代码的情况下更改内部实现。

**结论：**PHP 中的面向对象编程是利用信息隐藏中的封装概念来实现的。 它降低了当前类的属性的易访问性。 Getter 和 Setter 方法用于避免外部不需要的访问。 它还有助于验证分配给属性的新值。
简而言之，PHP 中的封装是隐藏对象的所有秘密细节的过程，这些细节实际上对类的关键特征没有太大影响。