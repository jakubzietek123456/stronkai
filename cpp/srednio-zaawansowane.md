---
layout: default
---

# C++ - Średnio zaawansowane

## Klasy i obiekty
W C++ klasy są podstawowymi jednostkami programowania obiektowego. Są to struktury, które mogą zawierać pola (zmienne składowe) i metody (funkcje składowe). Obiekty są instancjami klas, co oznacza, że reprezentują konkretne egzemplarze danej klasy. C++ umożliwia definiowanie konstruktorów, destruktorów, funkcji składowych, zmiennych prywatnych, chronionych i publicznych.

## Dziedziczenie
Dziedziczenie w C++ pozwala na tworzenie hierarchii klas, w których jedna klasa (klasa pochodna) może dziedziczyć cechy i funkcjonalności po innej klasie (klasie bazowej). Dziedziczenie może być publiczne, chronione lub prywatne, co wpływa na dostępność dziedziczonych składników klasy bazowej w klasie pochodnej.

## Polimorfizm
Polimorfizm w C++ pozwala na przesłanianie metod klasy bazowej przez klasy pochodne oraz na wykonywanie różnych działań w zależności od typu obiektu w czasie wykonania. Polimorfizm jest często realizowany poprzez dziedziczenie klas oraz używanie wskaźników lub referencji do obiektów.

## Szablony
Szablony w C++ umożliwiają tworzenie ogólnych typów i funkcji, które mogą być parametryzowane typami danych. Szablony pozwalają na elastyczne programowanie, ponieważ kod szablonowy może być używany do obsługi różnych typów danych bez konieczności powielania kodu.

## Standardowa Biblioteka Szablonów (STL)
STL jest zestawem bibliotek szablonów, które dostarczają wiele przydatnych kontenerów danych, algorytmów i narzędzi do programowania w C++. STL zawiera m.in. wektory, listy, mapy, stosy, kolejki, a także algorytmy sortowania, wyszukiwania, manipulacji danymi itp. Używanie STL może znacząco ułatwić i przyspieszyć pisanie kodu w C++.

#include <iostream>
#include <vector>

using namespace std;

// Klasy i obiekty
class Figura {
public:
    virtual void wyswietl() {
        cout << "To jest figura." << endl;
    }
};

class Kolo : public Figura {
public:
    void wyswietl() override {
        cout << "To jest kolo." << endl;
    }
};

// Dziedziczenie

// Polimorfizm
void wyswietlFigure(Figura* figura) {
    figura->wyswietl();
}

// Szablony
template<typename T>
T suma(T a, T b) {
    return a + b;
}

// Standardowa Biblioteka Szablonów (STL)
int main() {
    // Kolekcje z STL
    vector<int> liczby = {1, 2, 3, 4, 5};
    for (int liczba : liczby) {
        cout << liczba << " ";
    }
    cout << endl;

    // Wywołanie funkcji szablonowej
    cout << "Suma: " << suma(3, 5) << endl;

    // Polimorfizm
    Figura* figura = new Kolo();
    wyswietlFigure(figura);

    delete figura;

    return 0;
}

[Powrót](../)
