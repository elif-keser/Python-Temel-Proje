# Proje 

1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:

input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

output: [1,'a','cat',2,3,'dog',4,5]

2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:

input: [[1, 2], [3, 4], [5, 6, 7]]

output: [[[7, 6, 5], [4, 3], [2, 1]]

## 1


```python
def flatten(liste):
    son = []
    for e in liste:
        if isinstance(e, list):
            son.extend(flatten(e))
        else:
            son.append(e)
    return son

ilk = [[1, 'a', ['cat'], 2], [[[3]], 'dog'], 4, 5]
son = flatten(ilk)
print(sonuc)
```

    [[7, 6, 5], [4, 3], [2, 1]]


## 2


```python
def ters(liste):
    
    for a in liste:
        if isinstance(a, list): 
            a.reverse()
    
    liste.reverse()
    return liste

l = [[1, 2], [3, 4], [5, 6, 7]]
sonuc = ters(l)
print(sonuc)
```

    [[7, 6, 5], [4, 3], [2, 1]]



```python

```
