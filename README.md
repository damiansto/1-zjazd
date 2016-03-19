# Komputerowe wspomaganie nauczania przedmiotów scisych i przyrodniczych

##Zadania ze zjazdu 4-6.03.2016
*Ćwiczenie 1*

Zadanie 1 
###Napisz skrypt który wykonuje nastpujaca operacje 

Zadanie 2
###Napisz skrypt który wykonuje nastpujaca operacje 



##Zadania ze zjazdu 18-20.03.2016

Zadanie 3 
###Napisz skrypt który wykonuje nastpujaca operacje 
(a) definiuje zmienna n rowna np. 30
(b) oblicza sume liczb naturalnych od 1 do n i wyswietla wynik za pomoca polecenia print
(c) oblicza sume liczb parzystych od 2 do 2n i wyswietla wynik za pomoca polecenia print
(d) oblicza iloczyn kolejnych ulamkow od 1/2 do 1/n i wyswietla wynik za pomoca polecenia print
(e) oblicza sume kolejnych ulamkow od 1/n^2 do 1/2^2 i wyswietla wynik za pomoca polecenia print
(f) buduje 2n-elementowa liste x, zawierajaca na przemian liczby generowane przez rand i randint
(g) buduje liste y, zawierajaca elementy listy x ustawione w odwrotnej kolejnosci
(h) tworzy wykres, zawierajcy punkty wyznaczone przez odpowiednie elementy listy x i y (niebieskie kropki polaczone czarna linia)
```python
import numpy as np
import matplotlib.pyplot as plt
import numpy.random as npr

n=30
x=[]
for i in range (30):
    x.append(npr.randint(10))
    x.append(npr.rand())
    
print(len(x))
print(x)

print('odwarcamy')

y=x[::-1]
print(y)

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

