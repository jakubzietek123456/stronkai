---
layout: default
---

# JavaScript - Średnio zaawansowane

## Funkcje
Funkcje w JavaScript są obiektami, co oznacza, że mogą być przypisywane do zmiennych, przechowywane w tablicach, przekazywane jako argumenty do innych funkcji itp. Funkcje mogą być definiowane za pomocą słowa kluczowego `function` lub jako wyrażenia funkcyjne.

## Obiekty
W JavaScript obiekty są kolekcjami właściwości, które mają wartości lub funkcje. Obiekty mogą być tworzone za pomocą literału obiektowego `{}`, konstruktora `new Object()`, lub za pomocą funkcji konstruktora. Obiekty mogą być rozszerzane poprzez dodawanie nowych właściwości i metod.

## Asynchroniczność
JavaScript obsługuje asynchroniczność za pomocą mechanizmów takich jak funkcje zwrotne (callbacks), obietnice (promises) i funkcje async/await. Asynchroniczne operacje są używane do wykonywania zadań, które mogą zająć pewien czas, takich jak pobieranie danych z serwera, operacje sieciowe itp.

## DOM Manipulacja
Document Object Model (DOM) jest interfejsem reprezentującym strukturę dokumentu HTML lub XML. JavaScript może być używany do manipulowania DOM, co oznacza dodawanie, usuwanie lub zmienianie elementów na stronie internetowej. Manipulacja DOM jest często stosowana w celu tworzenia interaktywnych stron internetowych.

## Prototypy
Prototypy są fundamentalnym mechanizmem dziedziczenia w JavaScript. Każdy obiekt w JavaScript ma odwołanie do swojego prototypu, który jest obiektem samym w sobie. Dzięki prototypom, właściwości i metody mogą być dziedziczone przez inne obiekty.

// Funkcje
function powitanie(imie) {
    return "Witaj, " + imie + "!";
}

let komunikat = powitanie("Jan");
console.log(komunikat);

// Obiekty
let samochod = {
    marka: "Toyota",
    model: "Corolla",
    rocznik: 2020,
    informacje: function() {
        return this.marka + " " + this.model + ", rocznik " + this.rocznik;
    }
};

console.log("Informacje o samochodzie:", samochod.informacje());

// Asynchroniczność
function pobierzDane() {
    setTimeout(function() {
        console.log("Pobrano dane z serwera.");
    }, 2000);
}

pobierzDane();

// DOM Manipulacja
document.getElementById("przycisk").addEventListener("click", function() {
    document.getElementById("tekst").innerHTML = "Kliknięto przycisk!";
});

// Prototypy
function Ksiazka(tytul, autor) {
    this.tytul = tytul;
    this.autor = autor;
}

Ksiazka.prototype.informacje = function() {
    return this.tytul + " - " + this.autor;
};

let ksiazka = new Ksiazka("W pustyni i w puszczy", "Henryk Sienkiewicz");
console.log("Informacje o książce:", ksiazka.informacje());

[Powrót](../)
