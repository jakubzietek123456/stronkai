---
layout: default
---

# Python - Średnio zaawansowane

## Funkcje
Funkcje w Pythonie są blokami kodu, które wykonują określone zadania. Mogą przyjmować argumenty i zwracać wartości. Funkcje można definiować i wywoływać w dowolnym miejscu programu. W Pythonie istnieje wiele wbudowanych funkcji, ale możemy również definiować własne funkcje za pomocą słowa kluczowego `def`.

## Moduły
Moduły w Pythonie są plikami zawierającymi kod, który można importować do innych programów. Pozwalają one na organizację kodu na bardziej modularny sposób i ponowne wykorzystanie kodu. W Pythonie istnieje wiele wbudowanych modułów, a także możliwość tworzenia własnych modułów.

## Obsługa wyjątków
Obsługa wyjątków w Pythonie pozwala na zarządzanie błędami i nieoczekiwanymi sytuacjami w trakcie wykonywania programu. Dzięki instrukcji `try`, `except`, `else` i `finally` możemy kontrolować działanie programu nawet w przypadku wystąpienia błędu.

## Praca z plikami
Operacje na plikach są często wykonywane w programowaniu. W Pythonie mamy wiele wbudowanych funkcji do pracy z plikami, takich jak `open()`, `read()`, `write()`, `close()`, które pozwalają na otwieranie, czytanie, zapisywanie i zamykanie plików.

## Klasy i obiekty
Programowanie obiektowe jest silnie wspierane w Pythonie. Klasy są szablonami do tworzenia obiektów, które mogą zawierać atrybuty (zmienne) i metody (funkcje). Obiekty są instancjami klas, co oznacza, że ​​reprezentują konkretne egzemplarze danej klasy. W Pythonie dziedziczenie, polimorfizm i enkapsulacja są podstawowymi mechanizmami programowania obiektowego.

# Funkcje
def dodaj(a, b):
    return a + b

def odejmij(a, b):
    return a - b

def pomnoz(a, b):
    return a * b

print("Wynik dodawania:", dodaj(5, 3))
print("Wynik odejmowania:", odejmij(5, 3))
print("Wynik mnożenia:", pomnoz(5, 3))

# Moduły
import math
print("Wartość pi:", math.pi)

# Obsługa wyjątków
try:
    dzielenie = 10 / 0
except ZeroDivisionError:
    print("Nie można dzielić przez zero.")

# Praca z plikami
with open("plik.txt", "w") as plik:
    plik.write("To jest przykładowy tekst.")

with open("plik.txt", "r") as plik:
    print("Zawartość pliku:", plik.read())

# Klasy i obiekty
class Samochod:
    def __init__(self, marka, model):
        self.marka = marka
        self.model = model

    def info(self):
        print("Marka:", self.marka)
        print("Model:", self.model)

samochod = Samochod("Toyota", "Corolla")
samochod.info()

[Powrót](../)
