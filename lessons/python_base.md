# Presentazione su Python

## Descrizione generale del linguaggio

Python è un linguaggio di programmazione ad alto livello, interpretato e orientato agli oggetti. È stato creato da Guido van Rossum nel 1991 e da allora è diventato uno dei linguaggi di programmazione più popolari al mondo.

## Storia

Python è stato sviluppato da Guido van Rossum nel tardo 1980 come successore di un linguaggio di programmazione chiamato ABC. Il nome "Python" è stato ispirato dalla passione di van Rossum per il gruppo comico britannico Monty Python.

## Sintassi

La sintassi di Python è molto chiara e leggibile. Viene utilizzata l'indentazione per delimitare i blocchi di codice e non ci sono parentesi graffe. Ad esempio, un semplice programma "Hello World" in Python sarebbe scritto così:

```python
print("Hello, World!")
```

## Variabili

Le variabili in Python sono create automaticamente quando assegniamo loro un valore. Il tipo di dato viene determinato automaticamente in base al valore assegnato. Ad esempio:

```python
x = 42
y = "Hello"
```

## Commenti

I commenti in Python iniziano con il simbolo "#" e vengono ignorati dal compilatore. I commenti sono utilizzati per spiegare il codice e rendere più facile la sua comprensione.

```python
# Questo è un commento in Python
```

## Data Types

Python supporta diversi tipi di dati, tra cui numeri, stringhe, booleani e oggetti. Alcuni esempi:

### String

Le stringhe sono sequenze di caratteri racchiuse tra virgolette singole o doppie.

```python
x = "Hello, World!"
```

### Operatori di confronto

Gli operatori di confronto sono utilizzati per confrontare due valori. Esempi di operatori di confronto includono "==" (uguale a), "!=" (diverso da), "<" (minore di), ">" (maggiore di), "<=" (minore o uguale a) e ">=" (maggiore o uguale a).

```python
x = 42
y = 23
print(x > y)  # Output: True
```

## Loop

I loop in Python vengono utilizzati per ripetere un blocco di codice un certo numero di volte. I loop più comuni in Python sono "for" e "while".

### For loop

Il ciclo "for" viene utilizzato per iterare su una sequenza di elementi.

```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
```

### While loop

Il ciclo "while" viene utilizzato per ripetere un blocco di codice fintanto che una condizione è vera.

```python
i = 1
while i < 6:
  print(i)
  i += 1
```

## Array

In Python, gli array sono chiamati "liste". Le liste sono una collezione ordinata e modificabile di elementi.

```python
fruits = ["apple", "banana", "cherry"]
```

## Tuple

Le tuple sono una collezione ordinata e immutabile di elementi.

```python
fruits = ("apple", "banana", "cherry")
```

## Set

I set in Python sono collezioni non ordinate e non indicizzate di elementi unici.

```python
fruits = {"apple", "banana", "cherry"}
```

## Dizionari

I dizionari in Python sono collezioni di coppie chiave-valore.

```python
person = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
```

### Funzioni

Le funzioni in Python sono blocchi di codice riutilizzabili che vengono utilizzati per eseguire determinate azioni.

```python
def my_function(name):
  print("Hello, " + name)

my_function("John")  # Output: Hello, John
```

## Scope

Lo scope in Python definisce la visibilità delle variabili. Le variabili dichiarate all'interno di una funzione hanno uno scope locale, mentre le variabili dichiarate all'esterno di una funzione hanno uno scope globale.

```python
x = 42

def my_function():
  x = 23
  print(x)

my_function()  # Output: 23
print(x)  # Output: 42
```

## Classi

Le classi in Python vengono utilizzate per creare oggetti. Un oggetto è un'istanza di una classe.

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

p1 = Person("John", 36)
print(p1.name)  # Output: John
print(p1.age)  # Output: 36
```

## Visibilità all'interno di una classe

La visibilità all'interno di una classe in Python è definita dai prefissi "public", "private" e "protected". I membri di una classe sono pubblici per impostazione predefinita.

```python
class Person:
  def __init__(self, name, age):
    self.name = name  # public
    self._age = age  # protected
    self.__id = 12345  # private

p1 = Person("John", 36)
print(p1.name)  # Output: John
print(p1._age)  # Output: 36
print(p1.__id)  # Errore: AttributeError: 'Person' object has no attribute '__id'
```

## Ereditarietà tra classi

L'ereditarietà in Python consente a una classe di ereditare le proprietà e i metodi di un'altra classe.

```python
class Animal:
  def __init__(self, name):
    self.name = name

  def speak(self):
    raise NotImplementedError("Subclass must implement abstract method")

class Dog(Animal):
  def speak(self):
    return "Woof!"

class Cat(Animal):
  def speak(self):
    return "Meow!"

d = Dog("Rufus")
print(d.name)  # Output: Rufus
print(d.speak())  # Output: Woof!

c = Cat("Whiskers")
print(c.name)  # Output: Whiskers
print(c.speak())  # Output: Meow!
```

## Associazione tra classi

L'associazione in Python è quando un'istanza di una classe viene utilizzata come attributo di un'altra classe.

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

class Car:
  def __init__(self, make, model, owner):
    self.make = make
    self.model = model
    self.owner = owner

p = Person("John", 36)
c = Car("Toyota", "Corolla", p)
print(c.owner.name)  # Output: John
print(c.owner.age)  # Output: 36
```

## Aggregazione tra classi

L'aggregazione in Python è quando un'istanza di una classe contiene un riferimento a un'altra istanza di una classe, ma non controlla il ciclo di vita dell'altra istanza.

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

class Team:
  def __init__(self, name, captain):
    self.name = name
    self.captain = captain

p = Person("John", 36)
t = Team("Reds", p)
print(t.captain.name)  # Output: John
print(t.captain.age)  # Output: 36
```

## Composizione tra classi

La composizione in Python è quando un'istanza di una classe contiene un riferimento a un'altra istanza di una classe e controlla il ciclo di vita dell'altra istanza.

```python
class Engine:
  def start(self):
    print("Engine started")

class Car:
  def __init__(self):
    self.engine = Engine()

c = Car()
c.engine.start()  # Output: Engine started
```

## Eccezioni

Le eccezioni in Python sono degli oggetti che rappresentano un errore durante l'esecuzione del programma.

```python
try:
  x = 10 / 0
except ZeroDivisionError:
  print("Division by zero is not allowed")
```

## Gestione dei file

Python fornisce una serie di funzioni per la gestione dei file, come ad esempio open() per aprire un file e close() per chiuderlo.

```python
f = open("myfile.txt", "r")
print(f.read())
f.close()
```
