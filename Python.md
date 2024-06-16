---
layout: default
---
[Strona Główna](index.md) | [Kotlin](Kotlin.md) | [C++](C++.md)

## Podstawy Pythona

Python to wysokopoziomowy język programowania, który cechuje się czytelnością składni oraz prostotą nauki. Został stworzony przez Guido van Rossuma i jest rozwijany jako projekt open-source. Python jest wszechstronny i używany do tworzenia różnorodnych aplikacji, od prostych skryptów po zaawansowane aplikacje internetowe i sztuczną inteligencję.\

### Wypisywanie tekstu

Do wypisywania tekstu na ekranie używa się funkcji `print()`:

```python
print("Hello, world!")
```
### Zmienne i typy danych

Python automatycznie rozpoznaje typy zmiennych na podstawie przypisanych wartości. Przykłady:

```python
my_number = 10  # Liczba całkowita
my_float = 3.14  # Liczba zmiennoprzecinkowa
my_string = "Hello"  # Łańcuch znaków (string)
my_bool = True  # Wartość logiczna True/False
```
### Operatory

Python oferuje standardowe operatory arytmetyczne, porównania i logiczne:

#### Aritmetyczne

```python
result = 10 + 5  # Dodawanie
result = 10 - 5  # Odejmowanie
result = 10 * 5  # Mnożenie
result = 10 / 5  # Dzielenie
result = 10 % 3  # Reszta z dzielenia
```
#### Porównania
```python
is_equal = (10 == 5)  # Równe
is_not_equal = (10 != 5)  # Różne
is_greater = (10 > 5)  # Większe
is_less = (10 < 5)  # Mniejsze
is_greater_equal = (10 >= 5)  # Większe lub równe
is_less_equal = (10 <= 5)  # Mniejsze lub równe
```
#### Logiczne
```python
logical_and = (True and False)  # AND logiczne
logical_or = (True or False)  # OR logiczne
logical_not = not True  # NOT logiczne
```
### Instrukcje warunkowe

Instrukcje warunkowe pozwalają na wykonanie różnych fragmentów kodu w zależności od warunku:

```python
a = 10
if a > 5:
    print("A jest większe niż 5")
else:
    print("A nie jest większe niż 5")
```
### Pętle

Python oferuje pętle `for` i `while` do iteracji:

```python
# Pętla for
for i in range(5):
    print(i)

# Pętla while
i = 0
while i < 5:
    print(i)
    i += 1
```
### Funkcje

Definiowanie i wywoływanie funkcji w Pythonie:

```python
def greet(name):
    print("Hello, " + name + "!")
    
greet("Alice")
``` 
