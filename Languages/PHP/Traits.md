### Traits

- Traits essentially are: **language assisted copy and paste**
- Unlike inheritance: if trait has a static properties, each class using that has independent instances of those properties

```php

trait Info {

    private $msg = "I AM TRAIT";

    public function printMessage($message) : void {
        echo PHP_EOL . "------------" . PHP_EOL;
        echo $message;
        echo PHP_EOL . "------------" . PHP_EOL;
    }

    public function getSecretMessage() : string {
        return $this->msg;
    }
}

class Man {

    use Info;

    private $name;
    private $surname;

    public function setName($name) {
        return $this->name = $name;
    }

    public function setSurname($surname) {
        return $this->surname = $surname;
    }


    public function getName() {
        return $this->name;
    }
}

class Woman extends Man {

    public function sayHello() : void {
        echo PHP_EOL . "Hello, I am " . $this->getName() . PHP_EOL;
    }
}

$m = new Man;
$m->setName("Peter");
$m->setSurname("Peterson");

echo $m->getName(); // Peter
$m->printMessage("Hello from trait"); // Hello from trait
echo PHP_EOL .  $m->getSecretMessage() . PHP_EOL; // I AM TRAIT

$w = new Woman;
$w->setName("Jenna");
$w->setSurname("Doe");

echo $w->getName(); // Jenna
$w->printMessage("Hello from trait"); // Hello from trait
echo PHP_EOL .  $w->getSecretMessage() . PHP_EOL; // I AM TRAIT
$w->sayHello(); // Hello, I am Jenna

```
