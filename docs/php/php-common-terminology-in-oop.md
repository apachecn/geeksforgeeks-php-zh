# PHP | OOP 中的常用术语

> 原文:[https://www . geesforgeks . org/PHP-common-terminal-in-OOP/](https://www.geeksforgeeks.org/php-common-terminology-in-oop/)

**面向对象编程**是程序员解决现实问题非常重要的概念。本文解释了面向对象编程的概念及其特点。

*   **Object:** Everything in this world is surrounded with objects. Table, chair, monitor, cellphone everything is an object. There are two things in an object to remember to solve real-life problems. One is attribute and the other one is behavior. If we talk about monitor so…model number, screen size all these are attributes. On the other hand, the features like volume up or volume down are behavior for the monitor. In programming, variables are attributes and functions are behavior.

    **示例:**

    ```php
    <?php 

    // Class definition
    class TV {

        // Member variables
        public $model = 'xyz';
        public $volume = 1;

        // Member Functions
        function volumeUp() {
            $this->volume++;
        }

        function volumeDown() {
            $this->volume--;
        }
    }

    // Create new object
    $tv_one = new TV;

    // Calling member function
    $tv_one->volumeUp();
    echo $tv_one->volume;

    ?>
    ```

    **Output:**

    ```php
    2

    ```

    在上面的例子中，创建了一个电视类的对象$tv_one，并实现了显示该对象行为的函数。最初$tv_one->音量为 1。调用其函数后，音量已增大并显示更新结果。$这是指特定的或当前的对象。您可以创建多个对象并显示其行为。实现这些代码将会有代码重用的好处，并且代码在将来会很容易管理。

*   **Constructor function:** Constructor function is an special function for which do not need to call the function like earlier we were doing after creating an object.

    **示例:**

    ```php
    <?php 

    // Class definition
    class TV {

        // Member variables
        public $model;
        public $volume;

        // Member Functions
        function volumeUp() {
            $this->volume++;
        }

        function volumeDown() {
            $this->volume--;
        }
        function __construct($m, $v) {
         $this->model = $m; 
         $this->volume= $v;
       }
    }

    // Create new object
    $tv = new TV('xyz', 2);

    echo $tv->model;

    ?>
    ```

    **Output:**

    ```php
    xyz

    ```