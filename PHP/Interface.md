## PHP Interfaces

Interface vs. Abstract Classes

- Interfaces cannot have properties --- abstract classes can
- Interface methods must be public --- abstract classes methods are public or protected
- Interface methods are abstract
- Class can implement multiple interface
- Class can implement interface while extending another class

### Interface declaration

```php

interface Area {
	public function area();
}

```

### Interface implementation

```php

class Circle implements Area {
	...
}

```

### Code example

```php
<?php

interface Start {
  public function start();
}

interface Stop {
  public function stop();
}

interface Wheelie {
  public function wheelie();
}

class Vehicle {

  private $make;
  private $model;

  function __construct($make, $model) {
    $this->make = $make;
    $this->model = $model;
  }

  public function getMake() {
    echo $this->make . PHP_EOL;
  }

  public function getModel() {
    echo $this->model . PHP_EOL;
  }

}

class Motorcycle extends Vehicle implements Start, Stop, wheelie {

  private $make;
  private $model;

  function __construct($make, $model) {
    parent::__construct($make, $model);

    $this->make = $make;
    $this->model = $model;
  }

  public function start() {
    echo "Motorcycle " . $this->make . " " . $this->model . " started" . PHP_EOL;
  }

    public function stop() {
    echo "Motorcycle " . $this->make . " " . $this->model . " stopped" . PHP_EOL;
  }

  public function wheelie() {
    echo "Motorcycle " . $this->make . " " . $this->model . " does wheelie" . PHP_EOL;
  }
}

class Car extends Vehicle implements Start, Stop {
    private $make;
    private $model;

    function __construct($make, $model) {
        parent::__construct($make, $model);

        $this->make = $make;
        $this->model = $model;
    }

    public function start() {
        echo "Car " . $this->make . " " . $this->model . " started" . PHP_EOL;
    }

    public function stop() {
        echo "Car " . $this->make . " " . $this->model . " stopped" . PHP_EOL;
    }
}

$suzuki = new Motorcycle("Suzuki", "GSR600");
$volvo = new Car("Volvo", "C30");


$suzuki->start();
$suzuki->getModel();

$volvo->start();
$volvo->getModel();

?>
```
