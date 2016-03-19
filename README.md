# Komputerowe wspomaganie nauczania przedmiotów cisych i przyrodniczych

##Zadania ze zjazdu 18-20.03.2016

Zadanie 3 
```
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
Zadanie 3 z pierwszej listy zadan
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
