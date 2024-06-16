---
layout: default
---

[Strona Główna](index.md) | [C++](C++.md)


## Podstawy Kotlin

Kotlin to nowoczesny język programowania stworzony przez JetBrains, zaprojektowany do działania na JVM (Java Virtual Machine), ale może być również kompilowany do JavaScriptu lub używany w natywnych aplikacjach dzięki Kotlin Native.

### Wprowadzenie do Kotlin

* Kotlin jest językiem statycznie typowanym, co oznacza, że wszystkie typy muszą być określone w momencie kompilacji, jednak jego składnia jest bardziej zwięzła i czytelna w porównaniu do Javy.

* Język ten promuje bezpieczeństwo typów i eliminuje typowe błędy, które mogą wystąpić w Javie, jak np. NPE (NullPointerException).

### Podstawowe typy danych

Kotlin oferuje podstawowe typy danych takie jak `Int`, `Double`, `Boolean`, `String`, `Char` oraz ich odpowiedniki bez znaku `UInt`, `UByte` itp.
Typy danych są przypisywane przy użyciu słowa kluczowego `var` (dla zmiennych, których wartość można zmieniać) lub `val` (dla stałych, których wartość jest jednorazowo przypisywana).

```kotlin
val number: Int = 42
var message: String = "Hello, Kotlin!"
```

### Funkcje

Deklaracja funkcji odbywa się za pomocą słowa kluczowego `fun`. Funkcje mogą być globalne albo zdefiniowane wewnątrz klas i innych struktur. Kotlin wspiera funkcje zwracające wartości oraz funkcje, które nie zwracają wartości (funkcje procedur).

```kotlin
fun add(a: Int, b: Int): Int {
    return a + b
}
```
### Instrukcje warunkowe i pętle

Kotlin wspiera standardowe instrukcje warunkowe (`if`, `else if`, `else`) oraz pętle (`for`, `while`, `do while`).

```kotlin
val x = 10
if (x > 5) {
    println("x jest większe niż 5")
} else {
    println("x nie jest większe niż 5")
}

for (i in 1..5) {
    println(i)
}
```

### Klasy i obiekty

* Kotlin umożliwia definiowanie klas za pomocą słowa kluczowego `class`. Domyślnie klasy są `final`, ale można je oznaczyć jako `open`, aby były dziedziczone.

* Obiekty mogą być tworzone bez potrzeby definiowania klasy za pomocą słowa kluczowego `object`.

Na przykład :
```kotlin
class Car(val brand: String, val model: String) {
    fun displayInfo() {
        println("Brand: $brand, Model: $model")
    }
}

val myCar = Car("Toyota", "Corolla")
myCar.displayInfo()
```
1. Definicja klasy `Car`:
   * `class Car(val brand: String, val model: String)` definiuje klasę Car z dwoma właściwościami: `brand` (marka) i `model` (model), obie zadeklarowane jako parametry konstruktora (w Kotlinie `val` oznacza, że są to właściwości tylko do odczytu).
2. Metoda `displayInfo()`:
   * Jest to metoda wewnętrzna klasy `Car`, która drukuje na konsolę informacje o marce i modelu samochodu za pomocą interpolacji ciągów Kotlin (`"Brand: $brand, Model: $model"`).
3. Tworzenie obiektu `myCar`:
   * `val myCar = Car("Toyota", "Corolla")` tworzy nowy obiekt typu `Car` o marce "Toyota" i modelu "Corolla".
4. Wywołanie metody `displayInfo()`:
   * `myCar.displayInfo()` wywołuje metodę `displayInfo()` na obiekcie `myCar`, co powoduje wydrukowanie na konsolę tekstu "Brand: Toyota, Model: Corolla".

#### Zastosowanie
Ten kod demonstruje podstawy tworzenia klas i obiektów w Kotlinie oraz sposób definiowania konstruktorów i metod w tej języku. Jest to podstawowy przykład programowania obiektowego w Kotlinie, gdzie `Car` jest klasą reprezentującą samochód, a `displayInfo()` jest metodą do wyświetlania informacji o danym samochodzie.

### Null Safety

Kotlin promuje bezpieczeństwo nulli poprzez wprowadzenie systemu typów, które wymuszają świadome zarządzanie możliwością wystąpienia nulli (`Nullable` types).
```kotlin
var nullableString: String? = null
```
