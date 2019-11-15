# Produkty

## Pola wspólne

* id \| varchar\(36\) 
* name \| nvarchar\(255\) 
* date\_entered \| datetime\(NULL\) 
* date\_modified \| datetime\(NULL\) 
* modified\_user\_id \| varchar\(36\) 
* created\_by \| varchar\(36\) 
* description \| nvarchar\(-1\) 
* deleted \| bit\(NULL\) 
* assigned\_user\_id \| varchar\(36\) 
* currency\_id \| varchar\(36\) 

### maincode \| nvarchar\(100\) 

Kod produktu. W SuiteCRM przyjmuje postać listy rozwijalnej, za pomocą której nie ma sposobu wprowadzić żądane wartości. Raz na 5 minut wartość ta jest porównywana z polem kod\_c i w razie, gdy są różne jest nadpisywana wartością z ww pola.

### part\_number \| nvarchar\(100\) 

Kod produktu, z którym połączony jest dany produkt

### category \| nvarchar\(100\) 

Nieużywane

### type \| nvarchar\(100\) 

Nieużywane

### cost \| decimal\(NULL\) 

Nieużywane

### cost\_usdollar \| decimal\(NULL\) 

Nieużywane

### price \| decimal\(NULL\) 

Cena produktu

### price\_usdollar \| decimal\(NULL\)

Nieużywane

### url \| nvarchar\(255\) 

Link do strony produktu

### contact\_id \| varchar\(36\) 

Identyfikator opiekuna produktu

### product\_image \| nvarchar\(255\) 



### aos\_product\_category\_id \| varchar\(36\) 

### id\_c \| varchar\(36\) 

Identyfikator tabeli \_cstm

### kod\_c \| nvarchar\(100\) 

Kod produktu. W to pole jest wprowadzana wartość, która później jest przepisywana do pola maincode

### szerokosc\_c \| nvarchar\(50\) 

Szerokość

### bussiness\_unit\_c \| nvarchar\(100\) 

Bussiness Unit \(zgodnie z hierarchią produktów\)

### product\_group\_c \| nvarchar\(100\) 

Product group \(zgodnie z hierarchią produktów\)

### product\_subgroup\_c \| nvarchar\(100\) 

Product subgroup \(zgodnie z hierarchią produktów\)

### product\_brand\_c \| nvarchar\(100\) 

Product brand \(zgodnie z hierarchią produktów\)

### product\_manufacturer\_c \| nvarchar\(100\) 

Product manufacturer \(zgodnie z hierarchią produktów\)

### product\_type\_c \| nvarchar\(100\) 

Product type \(zgodnie z hierarchią produktów\)

### product\_model\_c \| nvarchar\(100\) 

Product model \(zgodnie z hierarchią produktów\)

### manufacturer\_code\_c \| nvarchar\(255\) 

Manufacturer code \(zgodnie z hierarchią produktów\)

### purchase\_price\_c \| decimal\(NULL\) 

Pole dodane na prośbę Pana Prezesa

### technical\_production\_cost\_c \| decimal\(NULL\) 

Pole dodane na prośbę Pana Prezesa

### net\_profit\_c \| decimal\(NULL\) 

Pole dodane na prośbę Pana Prezesa

### end\_user\_price\_pln\_c \| decimal\(NULL\)

Pole dodane na prośbę Pana Prezesa

### additional\_cost\_c \| decimal\(NULL\)

Dodatkowy koszt

