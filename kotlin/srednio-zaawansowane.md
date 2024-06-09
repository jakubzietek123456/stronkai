---
layout: default
---

# Kotlin - Średnio zaawansowane

## Klasy i obiekty
Kotlin umożliwia tworzenie klas i obiektów w sposób wyraźny i wygodny. Klasy mogą zawierać właściwości (pola) i metody. Wartości przypisane do właściwości mogą być zmienne lub niezmienne. Obiekty są instancjami klas i mogą być tworzone bezpośrednio w czasie działania programu.

## Dziedziczenie
Dziedziczenie w Kotlinie pozwala na tworzenie hierarchii klas, w których jedna klasa (klasa pochodna) może dziedziczyć cechy i funkcjonalności po innej klasie (klasie bazowej). Kotlin wspiera dziedziczenie jednokrotne, co oznacza, że ​​klasa może dziedziczyć tylko od jednej klasy bazowej.

## Interfejsy
Interfejsy w Kotlinie są zbliżone do interfejsów w innych językach programowania. Mogą zawierać deklaracje metod, ale także mogą zawierać implementacje metod (od Kotlin 1.0). Klasy implementujące interfejs muszą dostarczyć implementacje dla wszystkich jego metod.

## Korutyny
Korutyny są nowym podejściem do wielowątkowości w Kotlinie. Pozwalają one na asynchroniczne i nieblokujące wykonywanie operacji. Korutyny pozwalają na bardziej ekspresywny sposób definiowania operacji współbieżnych niż tradycyjne podejścia oparte na wątkach.

## Funkcje rozszerzające
Funkcje rozszerzające pozwalają na dodanie nowej funkcjonalności do istniejących klas bez modyfikowania ich kodu. W Kotlinie możemy definiować funkcje rozszerzające, które wydają się być częścią klasy, chociaż są zdefiniowane poza nią.

import kotlinx.coroutines.*

fun main() {
    // Klasy i obiekty
    val samochod = Samochod("Toyota", "Corolla")
    println("Marka samochodu: ${samochod.marka}, Model: ${samochod.model}")

    // Dziedziczenie
    val kot = Kot("Mruczek")
    kot.dzwiek()

    // Interfejsy
    val pies = Pies("Burek")
    pies.dzwiek()

    // Korutyny
    println("Początek wykonywania korutyny")
    GlobalScope.launch {
        delay(1000)
        println("Zakończenie korutyny po opóźnieniu 1 sekundy")
    }
    println("Kontynuacja wykonywania programu")

    // Funkcje rozszerzające
    val liczba = 5
    println("Liczba $liczba jest parzysta: ${liczba.czyParzysta()}")
}

// Klasy i obiekty
class Samochod(val marka: String, val model: String)

// Dziedziczenie
open class Zwierze(val imie: String) {
    open fun dzwiek() {
        println("$imie wydaje dźwięk")
    }
}

class Kot(imie: String) : Zwierze(imie)

// Interfejsy
interface Dzwiek {
    fun dzwiek()
}

class Pies(val imie: String) : Dzwiek {
    override fun dzwiek() {
        println("$imie szczeka")
    }
}

// Funkcje rozszerzające
fun Int.czyParzysta(): Boolean {
    return this % 2 == 0
}


[Powrót](../)
