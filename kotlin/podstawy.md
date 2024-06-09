---
layout: default
---

# Kotlin - Podstawy

## Składnia
Składnia języka Kotlin jest wyraźna i czytelna. Bazuje na konstrukcji "wyrażenie-funkcja-ciało". Każde wyrażenie i instrukcja zakończona jest średnikiem (;).

## Zmienne
Deklaracja i inicjalizacja zmiennych są proste w Kotlinie. Możemy używać słowa kluczowego `var` dla zmiennych zmieniennych oraz `val` dla zmiennych niezmiennych. Typ zmiennej może być jawnie określony lub automatycznie wywnioskowany.

## Typy danych
Język Kotlin oferuje szeroki wybór wbudowanych typów danych, które ułatwiają pracę z różnymi rodzajami danych. Wśród typów dostępnych w Kotlinie są liczby całkowite, liczby zmiennoprzecinkowe, znaki, ciągi znaków, wartości logiczne itp.

## Instrukcje sterujące
Kotlin dostarcza standardowe instrukcje sterujące, takie jak instrukcje warunkowe (`if`, `else if`, `else`) oraz pętle (`for`, `while`, `do while`), które pozwalają na kontrolowanie przepływu programu.

## Funkcje
Definiowanie i używanie funkcji w Kotlinie jest łatwe i intuicyjne. Funkcje mogą przyjmować argumenty i zwracać wartości. Możliwe jest również zagnieżdżanie funkcji i deklarowanie ich jako wyrażeń.

```kotlin
fun main() {
    // Składnia
    println("Witaj w programie w języku Kotlin!")

    // Zmienne
    var liczba = 10
    val imie = "Jan"
    println("$imie ma $liczba lat.")

    // Typy danych
    val pi: Double = 3.14
    val znak: Char = 'A'
    val prawda: Boolean = true
    println("Wartość PI: $pi, Znak: $znak, Prawda: $prawda")

    // Instrukcje sterujące
    if (liczba > 5) {
        println("$liczba jest większa od 5.")
    } else {
        println("$liczba nie jest większa od 5.")
    }

    // Funkcje
    val wynik = dodaj(5, 3)
    println("Wynik dodawania: $wynik")
}

fun dodaj(a: Int, b: Int): Int {
    return a + b
}

[Powrót](../)
