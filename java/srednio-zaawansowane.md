---
layout: default
---

# Java - Średnio zaawansowane

## Klasy

W języku Java, klasa jest szablonem lub wzorcem, który definiuje cechy i zachowanie obiektów. Klasa może zawierać pola (zmienne) i metody (funkcje). Definicja klasy zazwyczaj zawiera:

- **Deklarację klasy**: Określa nazwę klasy i, opcjonalnie, klasę nadrzędną, jeśli dziedziczy po innej klasie.
- **Pola (zmienne instancyjne)**: Przechowują stan obiektu.
- **Metody**: Określają zachowanie obiektu.

Przykładowa definicja klasy w języku Java:

```java

public class Car {

    // Pola klasy Car

    String brand;

    String model;

    int year;

    // Metoda klasy Car

    public void displayInfo() {

        System.out.println("Brand: " + brand + ", Model: " + model + ", Year: " + year);
    }
}

## Obiekty

Obiekt jest instancją klasy. Oznacza to, że gdy klasa jest zdefiniowana, nie zajmuje żadnej pamięci; jednak, gdy tworzysz obiekt (instancję) danej klasy, zajmuje on pamięć. Każdy obiekt ma własny zestaw pól, ale współdzieli kod (metody) z innymi instancjami tej samej klasy.

Przykładowe tworzenie i używanie obiektu klasy `Car`:

```java

public class Main {

    public static void main(String[] args) {

        // Tworzenie obiektu klasy Car

        Car myCar = new Car();

        // Ustawianie wartości pól obiektu

        myCar.brand = "Toyota";

        myCar.model = "Corolla";

        myCar.year = 2020;

        // Wywołanie metody obiektu

        myCar.displayInfo();
    }
}

## Dziedziczenie

Dziedziczenie jest jednym z podstawowych konceptów programowania obiektowego, który umożliwia tworzenie nowych klas na podstawie istniejących klas. Klasa dziedzicząca, zwana podklasą lub klasą potomną, może odziedziczyć pola i metody z klasy nadrzędnej, zwanej superklasą lub klasą nadrzędną. Dziedziczenie umożliwia ponowne wykorzystanie kodu oraz tworzenie hierarchii klas.

W języku Java dziedziczenie jest obsługiwane za pomocą słowa kluczowego `extends`. Klasa potomna rozszerza klasę nadrzędną, co oznacza, że dziedziczy po niej wszystkie jej pola i metody, a także może definiować nowe pola i metody.

Przykład dziedziczenia w języku Java:

```java

// Klasa nadrzędna

class Vehicle {

    String brand;

    int year;

    void displayInfo() {

        System.out.println("Brand: " + brand + ", Year: " + year);
    }
}

// Klasa potomna dziedzicząca po klasie Vehicle

class Car extends Vehicle {

    String model;

    void setModel(String model) {

        this.model = model;
    }

    void displayCarInfo() {

        System.out.println("Brand: " + brand + ", Model: " + model + ", Year: " + year);
    }
}

public class Main {

    public static void main(String[] args) {

        Car myCar = new Car();

        myCar.brand = "Toyota";

        myCar.setModel("Corolla");

        myCar.year = 2020;

        myCar.displayInfo(); // Wywołanie metody z klasy nadrzędnej

        myCar.displayCarInfo(); // Wywołanie metody z klasy potomnej
    }
}


## Polimorfizm

Polimorfizm jest jednym z kluczowych konceptów programowania obiektowego, który umożliwia przetwarzanie różnych typów obiektów w sposób jednolity. Oznacza to, że ten sam kod może zachowywać się inaczej w zależności od typu obiektu, na którym jest wywoływany.

W języku Java, polimorfizm jest często osiągany poprzez mechanizm przeciążania metod (overloading) oraz przesłaniania metod (overriding).

### Przeciążanie metod (Overloading)

Przeciążanie metod polega na definiowaniu wielu metod o tej samej nazwie, ale różniących się listą parametrów. Dzięki temu możemy wywoływać tę samą metodę za pomocą różnych zestawów parametrów. Przeciążanie metod jest formą statycznego (czyli kompilacyjnego) polimorfizmu.

```java

class Calculator {

    int add(int x, int y) {

        return x + y;
    }

    double add(double x, double y) {

        return x + y;
    }
}

public class Main {

    public static void main(String[] args) {

        Calculator calc = new Calculator();

        System.out.println(calc.add(5, 10)); // Wywołanie pierwszej metody add

        System.out.println(calc.add(3.5, 7.2)); // Wywołanie drugiej metody add
    }
}

## Przesłanianie metod (Overriding)

Przesłanianie metod polega na definiowaniu metody w klasie potomnej, która ma taką samą sygnaturę jak metoda w klasie nadrzędnej. Dzięki temu możemy zmienić zachowanie metody w klasie potomnej. Przesłanianie metod jest formą dynamicznego (czyli wykonawczego) polimorfizmu.

```java

class Animal {

    void makeSound() {

        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {

    @Override

    void makeSound() {

        System.out.println("Dog barks");
    }
}

public class Main {

    public static void main(String[] args) {

        Animal animal = new Dog();

        animal.makeSound(); // Wywołanie metody makeSound z klasy Dog
    }
}

## Klasy abstrakcyjne

Klasy abstrakcyjne są klasami, które same w sobie nie mogą być instancjonowane, ale mogą zawierać metody abstrakcyjne oraz metody z implementacją. Metoda abstrakcyjna jest deklaracją metody bez jej implementacji. Klasy abstrakcyjne są wykorzystywane do definiowania interfejsu dla klas potomnych oraz do zapewnienia wspólnej funkcjonalności dla tych klas.

W języku Java, klasy abstrakcyjne są oznaczane słowem kluczowym `abstract`. Klasa abstrakcyjna może zawierać zarówno metody abstrakcyjne, jak i metody z implementacją. Klasa potomna dziedzicząca po klasie abstrakcyjnej musi zaimplementować wszystkie metody abstrakcyjne z klasy nadrzędnej.

### Przykład klasy abstrakcyjnej

```java

abstract class Shape {

    abstract void draw(); // Metoda abstrakcyjna

    void display() { // Metoda z implementacją

        System.out.println("Displaying shape");
    }
}

class Circle extends Shape {

    @Override

    void draw() {

        System.out.println("Drawing circle");
    }
}

class Rectangle extends Shape {

    @Override

    void draw() {

        System.out.println("Drawing rectangle");
    }
}

public class Main {

    public static void main(String[] args) {

        Shape circle = new Circle();

        Shape rectangle = new Rectangle();

        circle.draw();

        circle.display();

        rectangle.draw();

        rectangle.display();
    }
}


## Interfejsy

Interfejsy w języku Java są abstrakcyjnymi typami danych, które definiują zestaw metod, które muszą zostać zaimplementowane przez każdą klasę, która implementuje ten interfejs. Interfejsy umożliwiają definiowanie kontraktu dla klas implementujących, bez określania szczegółów implementacji.

W języku Java, interfejsy są deklarowane za pomocą słowa kluczowego `interface`. Interfejsy mogą zawierać metody abstrakcyjne, metody z domyślną implementacją, stałe oraz metody statyczne.

### Przykład interfejsu

```java

interface Vehicle {

    void start(); // Metoda abstrakcyjna

    default void stop() { // Metoda z domyślną implementacją

        System.out.println("Stopping vehicle");
    }

    static void honk() { // Metoda statyczna

        System.out.println("Honking horn");
    }
}

class Car implements Vehicle {

    @Override

    public void start() {

        System.out.println("Starting car");
    }
}

class Motorcycle implements Vehicle {

    @Override

    public void start() {

        System.out.println("Starting motorcycle");
    }
}

public class Main {

    public static void main(String[] args) {

        Vehicle car = new Car();

        Vehicle motorcycle = new Motorcycle();

        car.start();

        car.stop();

        Vehicle.honk(); // Wywołanie metody statycznej

        motorcycle.start();

        motorcycle.stop();
    }
}


[Powrót](../)
