# Komputerowe wspomaganie nauczania przedmiotów scisych i przyrodniczych

##Zadania ze zjazdu 4-6.03.2016
*Ćwiczenie 1*

Zadanie 1 
###Napisz skrypt który wykonuje nastpujaca operacje 
a) definiuje zmienna n rowna np. 101;
b) buduje liste x, zawierajaca n rownoodleglych liczb z przedzialu (-2PI, 2PI);
c) oblicza liste s, zawierajaca sinusy liczb zawartych w liscie x;
d) oblicza liste c, zawierajaca cosinusy liczb zawartych w liscie x;
e) tworzy wykres funkcji sinus (linia ciagla zielona) i cosinus (linia czerwona przerywana), za pomoca list x, s, c;
f) oblicza liste s2, zawierajaca kwadraty elementow listy s;
g) oblicza liste c2, zawierajaca kwadraty elementow listy c;
h) oblicza wektor jt, bedacysuma list s2 i c2;
i) oblicza zmienna sr, bedaca srednia elementow listy it;
j) wyswietla wartosc zmiennej sr za pomoca polecenia print

```python
import numpy as np
import matplotlib.pyplot as plt

# a
n = 101

# b
x = np.linspace(-2*np.pi, 2*np.pi,n)

# c
s = np.sin(x)

# d
c = np.cos(x)

# e
plt.plot(x, s, '-g', x, c, '--r')
plt.show()

# f
s2 = s**2

# g
c2 = c**2

# h
jt = s2 + c2

# i
sr = np.mean(jt)

# j
print(sr)
```
Zadanie 2
###Napisz skrypt który wykonuje nastpujaca operacje 



##Zadania ze zjazdu 18-20.03.2016

Zadanie 3 
###Napisz skrypt który wykonuje nastpujaca operacje 
a) definiuje zmienna n rowna np. 30;
b) oblicza sume liczb naturalnych od 1 do n i wyswietla wynik za pomoca polecenia print;
c) oblicza sume liczb parzystych od 2 do 2n i wyswietla wynik za pomoca polecenia print;
d) oblicza iloczyn kolejnych ulamkow od 1/2 do 1/n i wyswietla wynik za pomoca polecenia print;
e) oblicza sume kolejnych ulamkow od 1/n^2 do 1/2^2 i wyswietla wynik za pomoca polecenia print;
f) buduje 2n-elementowa liste x, zawierajaca na przemian liczby generowane przez rand i randint;
g) buduje liste y, zawierajaca elementy listy x ustawione w odwrotnej kolejnosci;
h) tworzy wykres, zawierajcy punkty wyznaczone przez odpowiednie elementy listy x i y (niebieskie kropki polaczone czarna linia);

```python
import numpy as np
import matplotlib.pyplot as plt
import numpy.random as npr

#a
n=30

#b
print(sum(np.arange(1,n+1)))

#c
i=2
suma=0
while i<=2*n:
    suma=suma+i
    i=i+2
print(suma)

#d
print(np.prod(1/np.arange(2,n+1)))

#e
print(sum(1/np.arange(2,n+1)**2))

#f
x=[]
for i in range (30):
    x.append(npr.randint(10))
    x.append(npr.rand())

print(len(x))
print(x)

#g
print('odwarcamy')

y=x[::-1]
print(y)

#h
plt.plot(x,y,'.b',x,y,'-k')
```
*Ćwiczenie 2*

Zadanie 1
###Napisz skrypt który wykonuje nastpujaca operacje 
1. Buduje liste kodujaca wielomian W(x)=2x^4+4x^3+x+7
2. Wyswietla wartosc wielomianu w punkcie x=3
3. Wyswietla wykres wielomianu z zaznaczonym punktem x=3

```python
import numpy as np
import matplotlib.pyplot as plt
import numpy.random as npr

W1=[2,4,0,1,7]
a=np.polyval(W1,3)
print(a)
x=np.linspace(-4,4,101)
y=np.polyval(W1,x)
plt.plot(x,y)
plt.plot(3,a,'o')
```

