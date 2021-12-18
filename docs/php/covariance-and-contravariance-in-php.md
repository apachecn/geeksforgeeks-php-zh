# PHP 中的协方差和逆变

> 原文:[https://www . geeksforgeeks . org/compression-and-contra variation-in-PHP/](https://www.geeksforgeeks.org/covariance-and-contravariance-in-php/)

**协方差:**在 PHP 中，属于子方法的返回类型可以比父方法的返回类型更具体。这是通过协方差实现的。例如，考虑父类“Bank”，将“SB”和“BOI”作为其子类。

```php
<?php

// Parent class declared
abstract class bank {
    protected  $name;

    public function __construct( $name) {
        $this->name = $name;
    }

    abstract public function account();
}

// Child 1
class SBI extends bank {
    public function account() {
        echo $this->name . " has an SBI account";
    }
}

// Chil2
class BOI extends bank {
    public function account() {
        echo $this->name . " has a BOI account";
    }
}

interface acc_open {
    public function open($name): bank;
}

class SBI_acc_open implements acc_open {

    // Not returning the parent class 
    // type but the child's return 
    // type instead 
    public function open($name): SBI {
        return new SBI($name);
    }
}

class BOI_acc_open implements acc_open {

    // Not returning the parent class
    // type but the child's return
    // type instead
    public function open( $name) : BOI {
        return new BOI($name);
    }
}

$a = (new SBI_acc_open)->open("Arshit");
$a->account();
echo "\n";

$b = (new BOI_acc_open)->open("Simon");
$b->account();
?>
```

**输出:**

```php
Arshit has an SBI account
Simon has a BOI account

```

**对比:**在 PHP 中，与父方法的参数相比，属于子方法的参数可能不太具体。这是通过对比来完成的。

```php
<?php

// Parent class declared
abstract class bank {
    protected  $name;

    public function __construct( $name) {
        $this->name = $name;
    }

    public function acc_no(account_no $n) {
        echo $this->name . " has " . get_class($n);
    }
}

// Child 1
class SBI extends bank {
    public function account() {
        echo $this->name . " has an SBI account ";
    }

    // The function acc_no is overridden in 
    // the class SBI that allows any 
    // account_detail type object, it will 
    // show contravariance behavior
    public function acc_no(account_detail $n) {
        echo $this->name . " has an SBI "
                . get_class($n);
    }
}

// Child2
class BOI extends bank {
    public function account() {
        echo $this->name . " has a BOI account";
    }
}

interface acc_open {
    public function open($name): bank;
}

class SBI_acc_open implements acc_open {

    // Not returning the parent class type
    // but the child's return type instead
    public function open($name): SBI {
        return new SBI($name);
    }
}

class BOI_acc_open implements acc_open {

    // Not returning the parent class type 
    // but the child's return type instead
    public function open( $name) : BOI {
        return new BOI($name);
    }
}

class account_detail{} 
class account_no extends account_detail{}

$k = (new BOI_acc_open)->open("Shreyank");
$c = new account_no();
$k->acc_no($c);
echo("\n");

$y = (new SBI_acc_open)->open("Shrey");
$d = new account_detail();
$y->acc_no($d);
?>
```

**输出:**

```php
Shreyank has account_no
Shrey has an SBI account_detail

```

**注意:**通过排除子方法参数的类型限制，在 PHP 7 . 2 . 0 版本中实现了部分逆变。在 PHP 7 . 4 . 0 版本中，实现了完全的方差和协方差。7.2.0 版之前的所有旧版本都将显示错误。