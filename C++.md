---
layout: default
---

[Strona Główna](index.md) | [Kotlin](Kotlin.md) | [Python](Python.md)

# C++

## Podstawy C++

###  Wprowadzenie do C++

C++ jest językiem programowania ogólnego przeznaczenia, który wspiera programowanie proceduralne, obiektowe i generyczne. Jest rozszerzeniem języka C i zawiera wiele jego funkcji.

### Podstawowa składnia

#### Program Hello World

Najprostszy program w C++ wypisujący "Hello, World!" wygląda tak:

```cpp
#include <iostream> // Biblioteka do wejścia/wyjścia

int main() {
    std::cout << "Hello, World!" << std::endl; // Wypisanie tekstu
    return 0; // Zakończenie programu
}

```
### Typy danych

C++ oferuje kilka podstawowych typów danych:

- **Liczby całkowite:** `int`, `short`, `long`, `long long`
- **Liczby zmiennoprzecinkowe:** `float`, `double`, `long double`
- **Znaki:** `char`
- **Boolowskie:** `bool`
- **Typy bez znaku:** `unsigned int`, `unsigned char`, itp.

### Zmienne i stałe

#### Deklarowanie i inicjalizowanie zmiennych

##### Zmienne

Zmienną można zadeklarować i jednocześnie zainicjalizować, przypisując jej wartość :
```cpp
int myNumber = 5;
char myCharacter = 'A';
bool isReady = true;
```
##### Stałe

Stałe to zmienne, których wartość nie może zostać zmieniona po inicjalizacji. Deklaruje się je przy użyciu słowa kluczowego const:
```cpp
const int DAYS_IN_WEEK = 7;
```
### Operatory

#### Aritmetyczne

- `+` (dodawanie)
- `-` (odejmowanie)
- `*` (mnożenie)
- `/` (dzielenie)
- `%` (modulo)

#### Porównania

- `==` (równe)
- `!=` (różne)
- `<` (mniejsze)
- `>` (większe)
- `<=` (mniejsze lub równe)
- `>=` (większe lub równe)

#### Logiczne

- `&&` (logiczne AND)
- `||` (logiczne OR)
- `!` (logiczne NOT)

#### Przypisania

- `=` (przypisanie)
- `+=` (dodaj i przypisz)
- `-=` (odejmij i przypisz)
- `*=` (pomnóż i przypisz)
- `/=` (podziel i przypisz)
- `%=` (modulo i przypisz)

### Struktury sterujące

#### Instrukcje warunkowe

```cpp
int a = 10;
if (a > 5) {
    std::cout << "A jest większe niż 5" << std::endl;
} else {
    std::cout << "A nie jest większe niż 5" << std::endl;
}
```
Krótko opisując:

* Zmienna a jest inicjalizowana wartością 10.

* Warunek if (a > 5) sprawdza, czy wartość zmiennej a jest większa od 5.

* Jeśli warunek jest spełniony (czyli a jest większe od 5), wyświetlany jest komunikat "A is greater than 5".

* W przeciwnym razie (gdy a nie jest większe od 5), wyświetlany jest komunikat "A is not greater than 5".

* W ten sposób program decyduje, który komunikat powinien zostać wyświetlony na podstawie wartości zmiennej a.


#### Pętle

##### Pętla for:
Pętla for:
Pętla for jest używana do iteracji przez zestaw instrukcji określoną liczbę razy, kontrolując zmienną iteracyjną. Składa się z trzech głównych części: inicjalizacji (ustawienie początkowej wartości zmiennej), warunku (określenia kiedy pętla powinna się zakończyć) oraz kroku (zmiany wartości zmiennej iteracyjnej po każdej iteracji). Jest idealna do sytuacji, gdzie liczba iteracji jest znana przed jej rozpoczęciem.
```cpp
for (int i = 0; i < 10; i++) {
    std::cout << i << std::endl;
}
```
##### Pętla while:
Pętla while wykonuje blok kodu, dopóki podany warunek jest prawdziwy. Jest bardziej ogólna niż pętla for i używana, gdy nie jest z góry znana liczba iteracji. Wymaga ustawienia warunku przed jej rozpoczęciem, a następnie powtarza wykonanie kodu dopóki warunek jest spełniony. Może być stosowana w sytuacjach, gdzie warunek powtarzania może zmieniać się podczas działania programu.
```cpp
int i = 0;
while (i < 10) {
    std::cout << i << std::endl;
    i++;
}
```
##### Pętla do-while:
Pętla do-while jest podobna do pętli while, jednak różni się tym, że sprawdzenie warunku występuje po wykonaniu kodu w bloku pętli. Oznacza to, że kod w bloku wykona się przynajmniej raz, niezależnie od tego, czy warunek jest spełniony czy nie. Jest przydatna, gdy chcemy, aby kod w pętli został wykonany przynajmniej raz, zanim sprawdzimy warunek kontynuacji pętli.
```cpp
int i = 0;
do {
    std::cout << i << std::endl;
    i++;
} while (i < 10);
```
### Funkcje

### Deklarowanie i definiowanie funkcji:

Deklarowanie funkcji w C++ polega na określeniu jej istnienia poprzez podanie sygnatury funkcji (nazwy funkcji oraz typów jej parametrów i zwracanej wartości) bez implementacji. Definiowanie funkcji natomiast obejmuje dostarczenie dokładnej implementacji, która określa, jak funkcja ma działać, tj. zawiera blok kodu realizujący jej funkcjonalność. Deklarowanie umożliwia używanie funkcji w innych częściach programu, podczas gdy definiowanie jest konieczne do określenia szczegółów jej działania.
```cpp
#include <iostream>

// Deklaracja funkcji
int add(int a, int b);

int main() {
    int sum = add(5, 3); // Wywołanie funkcji
    std::cout << "Sum: " << sum << std::endl;
    return 0;
}

// Definicja funkcji
int add(int a, int b) {
    return a + b;
}
```
### Klasy i obiekty
Klasy i obiekty są fundamentalnymi pojęciami programowania obiektowego w C++:

- **Klasa**: Jest to szablon lub wzorzec definiujący właściwości i zachowania obiektów. Zawiera deklaracje danych (pola) oraz funkcji (metody), które mogą operować na tych danych. Klasa określa, jakie cechy mają obiekty tworzone na jej podstawie.

- **Obiekt**: Jest instancją klasy, czyli konkretnym przypadkiem lub reprezentacją klasy w czasie działania programu. Obiekt przechowuje własne kopie zmiennych składowych (pól) klasy i może wywoływać metody zdefiniowane w klasie.

W praktyce, klasy i obiekty pozwalają na strukturalne organizowanie kodu, dzięki czemu można tworzyć modularne i łatwe w zarządzaniu aplikacje. Programowanie obiektowe opiera się na koncepcji enkapsulacji, dziedziczenia i polimorfizmu, które umożliwiają tworzenie bardziej elastycznych i rozszerzalnych rozwiązań programistycznych.

### Podstawowa klasa:

```cpp
#include <iostream>

// Definicja klasy
class Car {
public:
    std::string brand;
    std::string model;
    int year;

    void displayInfo() {
        std::cout << "Brand: " << brand << ", Model: " << model << ", Year: " << year << std::endl;
    }
};

int main() {
    Car myCar; // Utworzenie obiektu
    myCar.brand = "Toyota";
    myCar.model = "Corolla";
    myCar.year = 2020;

    myCar.displayInfo(); // Wywołanie metody obiektu
    return 0;
}
```
### Wskaźniki i referencje

#### Wskaźniki:

* Definicja: Wskaźniki są zmiennymi, które przechowują adres pamięci komputera, zamiast bezpośredniej wartości.

* Użycie: Są używane do bezpośredniego manipulowania pamięcią komputera oraz do przekazywania adresów zmiennych do funkcji.

* Dereferencja: Operator * używany jest do dostępu do wartości przechowywanej pod adresem, który wskaźnik przechowuje.
```cpp
int a = 10;
int *ptr = &a; // Wskaźnik przechowujący adres zmiennej 'a'
std::cout << "Value of a: " << *ptr << std::endl; // Dereferencja wskaźnika
```
#### Referencje
* Definicja: Referencje są aliasami istniejących zmiennych. Po zainicjowaniu referencji, może być używana zamiennie z oryginalną zmienną.

* Charakterystyka: Są bezpieczniejsze w użyciu niż wskaźniki, ponieważ nie mogą być nullami ani zmieniać referencji na inne obiekty po zainicjowaniu.

* Sposób działania: Zmiany dokonywane na referencji bezpośrednio wpływają na zmienną, do której się odwołuje.

```cpp
int a = 10;
int &ref = a; // Referencja do zmiennej 'a'
ref = 20; // Zmienia wartość 'a' na 20
std::cout << "Value of a: " << a << std::endl;
```
### Podstawowe biblioteki standardowe

- **Biblioteka wejścia/wyjścia:** `<iostream>` (`std::cin`, `std::cout`, `std::cerr`)
- **Biblioteka łańcuchów znaków:** `<string>`
- **Biblioteka kontenerów:** `<vector>`, `<array>`, `<map>`, `<set>`, itp.
- **Biblioteka algorytmów:** `<algorithm>`

Te podstawowe elementy C++ stanowią solidny fundament do nauki i rozwoju w programowaniu w tym języku. Na ich bazie można budować bardziej zaawansowane umiejętności i projekty.
