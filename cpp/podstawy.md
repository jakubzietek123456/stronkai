---
layout: default
---

# C++ - Podstawy

## Składnia
Składnia języka C++ jest podobna do języka C, ale dodaje wiele nowych funkcji i konstrukcji. W C++ kod jest organizowany w funkcje, które mogą być wywoływane w programie głównym lub w innych funkcjach. Bloki kodu są oznaczone klamrami {}, a każda instrukcja kończy się średnikiem ;.

## Zmienne
Deklaracja i inicjalizacja zmiennych w C++ jest podobna do innych języków programowania. Zmienne muszą być zadeklarowane przed użyciem, a typ danych może być jawnie określony lub automatycznie wywnioskowany.

## Typy danych
C++ oferuje wiele podstawowych typów danych, takich jak liczby całkowite (int, long), liczby zmiennoprzecinkowe (float, double), znaki (char), ciągi znaków (string), wartości logiczne (bool) itp. Istnieją również różne modyfikatory typów danych, takie jak signed, unsigned, short, long itp.

## Operatory
C++ posiada bogaty zestaw operatorów, zarówno arytmetycznych, logicznych, przypisania, porównania, jak i bitowych. Operatorów używa się do wykonywania operacji na zmiennych i wartościach.

## Struktury sterujące
Instrukcje warunkowe (if, else if, else) i pętle (for, while, do while) są podstawowymi mechanizmami kontroli przepływu w C++. Pozwalają one na wykonywanie określonych fragmentów kodu w zależności od warunków logicznych oraz na iterację przez kolekcje danych lub wykonanie określonych działań określoną ilość razy.

#include <iostream>
#include <string>

using namespace std;

// Deklaracja funkcji
void przywitaj(string imie);

int main() {
    // Składnia
    cout << "Witaj w programie w jezyku C++!" << endl;

    // Zmienne
    int liczba = 10;
    const double pi = 3.14;
    cout << "Liczba: " << liczba << ", PI: " << pi << endl;

    // Typy danych
    char znak = 'A';
    bool prawda = true;
    cout << "Znak: " << znak << ", Prawda: " << prawda << endl;

    // Operatory
    int a = 5, b = 3;
    int suma = a + b;
    cout << "Suma: " << suma << endl;

    // Struktury sterujące
    if (liczba > 5) {
        cout << liczba << " jest wieksza od 5." << endl;
    } else {
        cout << liczba << " nie jest wieksza od 5." << endl;
    }

    // Wywołanie funkcji
    przywitaj("Jan");

    return 0;
}

// Definicja funkcji
void przywitaj(string imie) {
    cout << "Witaj, " << imie << "!" << endl;
}

[Powrót](../)

