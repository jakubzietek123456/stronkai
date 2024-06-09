---
layout: default
---

# Java - Podstawy

## Składnia
- Omówienie podstawowej składni języka Java.

## Zmienne w języku Java

Zmienne w języku Java są używane do przechowywania danych. Każda zmienna musi być zadeklarowana z określonym typem danych. Deklaracja zmiennej obejmuje podanie typu oraz opcjonalnie nazwy i wartości początkowej. Inicjalizacja zmiennej oznacza przypisanie jej początkowej wartości.

Zmienne mogą przechowywać różne rodzaje danych, takie jak liczby całkowite, liczby zmiennoprzecinkowe, znaki, ciągi znaków itp.

Wartość początkowa zmiennej może być zmieniana w trakcie działania programu.

Zmienne są podstawowymi elementami przechowywania danych w języku Java i są powszechnie wykorzystywane w tworzeniu aplikacji.

## Przykłady deklaracji zmiennych w języku Java

```java

int liczbaCalkowita; // Deklaracja zmiennej

double liczbaZmiennoprzecinkowa = 5.5; // Deklaracja i inicjalizacja w jednym kroku

String tekst = "To jest tekst"; // Deklaracja i inicjalizacja zmiennej typu String


## Typy danych w języku Java

Język Java posiada różnorodne typy danych, które służą do przechowywania różnych rodzajów informacji. Typy te można podzielić na dwa główne rodzaje: **typy proste** (primitive types) i **typy referencyjne** (reference types).

### Typy proste (primitive types)

Typy proste w języku Java są podstawowymi typami danych, które przechowują wartości bezpośrednio. Są one dzielone na kilka podstawowych kategorii:

1. **Liczby całkowite**:
   - `byte`: 8-bitowa liczba całkowita.
   - `short`: 16-bitowa liczba całkowita.
   - `int`: 32-bitowa liczba całkowita.
   - `long`: 64-bitowa liczba całkowita.

2. **Liczby zmiennoprzecinkowe**:
   - `float`: 32-bitowa liczba zmiennoprzecinkowa.
   - `double`: 64-bitowa liczba zmiennoprzecinkowa.

3. **Typ logiczny**:
   - `boolean`: Przechowuje wartość logiczną `true` lub `false`.

4. **Znak**:
   - `char`: Przechowuje pojedynczy znak Unicode.

### Typy referencyjne (reference types)

Typy referencyjne w języku Java służą do przechowywania referencji do obiektów. Są one używane do tworzenia złożonych struktur danych i obiektów. Niektóre z najczęściej używanych typów referencyjnych to:

- `String`: Reprezentuje ciąg znaków.
- `Arrays`: Służy do manipulowania tablicami.
- `Classes`: Reprezentuje klasy.
- `Interfaces`: Reprezentuje interfejsy.
- `Enumerations`: Reprezentuje typ wyliczeniowy.

## Przykłady deklaracji zmiennych z różnymi typami danych w języku Java

```java

int liczbaCalkowita; // Deklaracja zmiennej typu całkowitego

double liczbaZmiennoprzecinkowa = 5.5; // Deklaracja i inicjalizacja zmiennej typu zmiennoprzecinkowego

String tekst = "To jest tekst"; // Deklaracja i inicjalizacja zmiennej typu String

char znak = 'A'; // Deklaracja i inicjalizacja zmiennej typu znakowego

boolean czyPrawda = true; // Deklaracja i inicjalizacja zmiennej typu logicznego

## Operatory w języku Java

Operatory w języku Java są używane do wykonywania różnych operacji na zmiennych i wartościach. Istnieje kilka rodzajów operatorów, z których każdy ma swoje specyficzne zastosowanie.

### Operatory arytmetyczne

Operatory arytmetyczne służą do wykonywania podstawowych operacji arytmetycznych na liczbach. Oto lista operatorów arytmetycznych w języku Java:

- `+`: Dodawanie.
- `-`: Odejmowanie.
- `*`: Mnożenie.
- `/`: Dzielenie.
- `%`: Reszta z dzielenia (modulo).

### Operatory przypisania

Operatory przypisania służą do przypisywania wartości do zmiennych. Oto lista operatorów przypisania w języku Java:

- `=`: Przypisanie wartości.
- `+=`: Dodanie wartości i przypisanie.
- `-=`: Odjęcie wartości i przypisanie.
- `*=`: Pomnożenie wartości i przypisanie.
- `/=`: Podzielenie wartości i przypisanie.

### Operatory porównania

Operatory porównania są używane do porównywania wartości dwóch zmiennych. Oto lista operatorów porównania w języku Java:

- `==`: Czy równa się.
- `!=`: Czy nie równa się.
- `>`: Większe niż.
- `<`: Mniejsze niż.
- `>=`: Większe lub równe.
- `<=`: Mniejsze lub równe.

### Operatory logiczne

Operatory logiczne są używane do wykonywania operacji logicznych na wartościach logicznych. Oto lista operatorów logicznych w języku Java:

- `&&`: Logiczne AND.
- `||`: Logiczne OR.
- `!`: Logiczne NOT.

### Operatory inkrementacji i dekrementacji

Operatory inkrementacji i dekrementacji służą do zwiększania lub zmniejszania wartości zmiennej o jeden. Oto lista operatorów inkrementacji i dekrementacji w języku Java:

- `++`: Inkrementacja.
- `--`: Dekrementacja.

To jest przegląd operatorów w języku Java. Każdy z tych operatorów może być używany w różnych kontekstach programistycznych do wykonania określonych operacji.

## Przykład użycia operatorów w języku Java

```java

int a = 5;

int b = 3;

// Operatory arytmetyczne

int suma = a + b;

int roznica = a - b;

int iloczyn = a * b;

int iloraz = a / b;

int reszta = a % b;

// Operatory przypisania

a += b;

b -= a;

a *= b;

b /= a;

a %= b;

// Operatory porównania

boolean czyRowne = (a == b);

boolean czyWieksze = (a > b);

boolean czyMniejsze = (a < b);

boolean czyRowneLubWieksze = (a >= b);

boolean czyRowneLubMniejsze = (a <= b);

boolean czyRozne = (a != b);

// Operatory logiczne

boolean czyPrawda = true;

boolean czyFalsz = false;

boolean logiczneAND = czyPrawda && czyFalsz;

boolean logiczneOR = czyPrawda || czyFalsz;

boolean logiczneNOT = !czyPrawda;

## Instrukcje sterujące w języku Java

### Instrukcje warunkowe

Instrukcje warunkowe pozwalają na wykonanie różnych działań w zależności od warunków logicznych. W języku Java najczęściej używane są instrukcje `if`, `else if` i `else`.

- Instrukcja `if` wykonuje blok kodu, jeśli warunek jest prawdziwy.
- Instrukcja `else if` wykonuje alternatywny blok kodu, jeśli poprzedni warunek jest fałszywy i obecny warunek jest prawdziwy.
- Instrukcja `else` wykonuje blok kodu, jeśli żaden z poprzednich warunków nie jest prawdziwy.

### Pętle

Pętle pozwalają na wielokrotne wykonanie bloku kodu. W języku Java najczęściej używane są pętle `for`, `while` i `do-while`.

- Pętla `for` wykonuje określoną liczbę iteracji na podstawie warunku początkowego, warunku zakończenia i inkrementacji/dekrementacji.
- Pętla `while` wykonuje blok kodu dopóki warunek jest prawdziwy.
- Pętla `do-while` wykonuje blok kodu przynajmniej raz, a następnie sprawdza warunek.

Instrukcje sterujące są kluczowymi elementami w programowaniu, pozwalającymi na kontrolowanie przepływu wykonania programu i umożliwiającymi tworzenie bardziej elastycznych i dynamicznych aplikacji.

## Przykład użycia instrukcji sterujących w języku Java

```java

int liczba = 10;

// Instrukcja warunkowa if-else

if (liczba > 0) {
    System.out.println("Liczba jest dodatnia");
} else if (liczba < 0) {
    System.out.println("Liczba jest ujemna");
} else {
    System.out.println("Liczba jest równa zero");
}

// Pętla for

for (int i = 0; i < 5; i++) {
    System.out.println("Wartość i: " + i);
}

// Pętla while

int j = 0;
while (j < 5) {
    System.out.println("Wartość j: " + j);
    j++;
}

// Pętla do-while

int k = 0;

do {
    System.out.println("Wartość k: " + k);
    k++;
} while (k < 5);

[Powrót](../)
