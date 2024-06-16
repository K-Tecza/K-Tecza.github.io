---
layout: default
---

[Strona Główna](index.md)

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