# Matrizen und Listen von Listen

Empfohlene Skills: [Datentypen und Operatoren](01_datentypen_operationen.md), [Kontrollstrukturen](02_kontrollstrukturen.md), [Listen](04_listen.md) und 
Grundkenntnisse in [List Comprehension](06_list_comprehension.md)

---

Zweidimensionale Listen, auch bekannt als Listen von Listen, sind eine Möglichkeit, Daten in einer tabellarischen Form zu 
organisieren. Sie können verwendet werden, um Matrizen, Tabellen oder ähnliche Datenstrukturen darzustellen. Prinzipiell
sind natürlich beliebig dimensionale Listen denkbar, aber wir fokussieren uns hier auf den Fall der zweidimensionalen Liste.


## Erstellung von zweidimensionalen Listen

Eine zweidimensionale Liste wird erstellt, indem mehrere Listen als Elemente innerhalb einer äußeren Liste definiert werden.

### Beispiel:

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

In diesem Beispiel besteht `matrix` aus 3 Zeilen und 3 Spalten, wobei jede innere Liste eine Zeile darstellt.


## Zugriff auf Elemente in zweidimensionalen Listen

Der Zugriff auf die Elemente erfolgt über den Zeilen- und Spaltenindex. Der erste Index bezeichnet die Zeile, der zweite Index die Spalte.

### Beispiel:

```python
print(matrix[0][1])  # Zugriff auf die erste Zeile, zweite Spalte 
print(matrix[2][2])  # Zugriff auf die dritte Zeile, dritte Spalte 
```

Sie können auch negative Indizes verwenden, um von hinten auf die Listen zuzugreifen.

```python
print(matrix[-1][-1])  # Zugriff auf das letzte Element 
print(matrix[-2][-3])  # Zugriff auf das Element in der zweiten letzten Zeile und dritten letzten Spalte
```


## Iteration über zweidimensionale Listen

Es ist möglich, mit verschachtelten `for`-Schleifen über zweidimensionale Listen iterieren, um jedes Element zu erreichen.

### Beispiel:

```python
for row in matrix:
    for element in row:
        print(element, end=' ')
    print()
```

**Ausgabe:**

```
1 2 3 
4 5 6 
7 8 9 
```


## Modifizieren von Elementen in einer zweidimensionalen Liste

Sie können die Elemente einer zweidimensionalen Liste ändern, indem Sie sie über ihren Index ansprechen.

### Beispiel:

```python
matrix[1][1] = 10  # Ändere das Element in der zweiten Zeile und zweiten Spalte
print(matrix)  
```


## Slicing in zweidimensionalen Listen

Analog zu eindimensionalen Listen können Sie auch Slicing in zweidimensionalen Listen verwenden, um Teile der Liste zu extrahieren.

### Beispiel:

```python
# Zugriff auf die ersten beiden Zeilen
part_matrix = matrix[:2]
print(part_matrix)  

# Zugriff auf die ersten beiden Spalten jeder Zeile
column_part = [row[:2] for row in matrix]  # siehe List Comprehension
print(column_part)  
```

---

[vorherige Seite](04_listen.md)  
[Zurück zum Inhaltsverzeichnis](00_inhaltsverzeichnis.md)  
[nächste Seite](06_list_comprehension.md)