---
layout: default
---

# JavaScript - Podstawy

## Składnia
Składnia języka JavaScript jest podobna do języków takich jak Java czy C, ale jest bardziej luźna i elastyczna. Instrukcje są zazwyczaj zakończone średnikiem, ale czasami nie jest to wymagane. Bloki kodu są definiowane za pomocą nawiasów klamrowych {}. JavaScript jest językiem skryptowym, co oznacza, że ​​kod może być wykonywany bezpośrednio w przeglądarce internetowej.

## Zmienne
W JavaScript deklaracja zmiennych odbywa się za pomocą słów kluczowych `var`, `let` lub `const`. `var` było tradycyjnie używane do deklarowania zmiennych, ale od ES6 wprowadzono `let` i `const`. `let` pozwala na deklarowanie zmiennych, których wartość może się zmieniać, podczas gdy `const` tworzy zmienne, których wartość nie może się zmieniać.

## Typy danych
JavaScript jest językiem dynamicznym, co oznacza, że typ danych zmiennej jest określany automatycznie na podstawie wartości, jaką przechowuje. Podstawowe typy danych to liczby, ciągi znaków, wartości logiczne, undefined i null. Istnieją również bardziej skomplikowane typy danych, takie jak tablice i obiekty.

## Operatory
JavaScript posiada wiele operatorów, zarówno arytmetycznych (+, -, *, /), jak i logicznych (&&, ||, !), porównania (==, !=, <, >, <=, >=), przypisania (=), itp. Operatorzy są używane do wykonywania operacji na zmiennych i wartościach.

## Instrukcje sterujące
Instrukcje warunkowe (if, else if, else) i pętle (for, while, do while) są kluczowymi elementami sterowania przepływem w JavaScript. Pozwalają one na wykonanie określonych fragmentów kodu w zależności od warunków logicznych oraz na iterację przez kolekcje danych lub wykonanie określonych działań określoną ilość razy.

// Składnia
console.log("Witaj w programie w języku JavaScript!");

// Zmienne
var liczba = 10;
let pi = 3.14;
const imie = "Jan";
console.log("Liczba:", liczba, ", PI:", pi, ", Imie:", imie);

// Typy danych
let znak = 'A';
let prawda = true;
console.log("Znak:", znak, ", Prawda:", prawda);

// Operatory
let a = 5;
let b = 3;
let suma = a + b;
console.log("Suma:", suma);

// Instrukcje sterujące
if (liczba > 5) {
    console.log(liczba, "jest większa od 5.");
} else {
    console.log(liczba, "nie jest większa od 5.");
}

[Powrót](../)
