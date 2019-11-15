# Zamówienia

## Pola wspólne

* id \| varchar \(36\) 
* name \| nvarchar \(255\) 
* date\_entered \| datetime \(NULL\) 
* date\_modified \| datetime \(NULL\) 
* modified\_user\_id \| varchar \(36\) 
* created\_by \| varchar \(36\) 
* description \| nvarchar \(-1\) 
* deleted \| bit \(NULL\) 
* assigned\_user\_id \| varchar \(36\) 
* currency\_id \| varchar \(36\) 

### reference\_code \| nvarchar \(255\) 

Pole nieużywane

### start\_date \| datetime \(NULL\) 

Data rozpoczęcia kontraktu

### end\_date \| datetime \(NULL\) 

Data zakończenia kontraktu

### total\_contract\_value \| decimal \(NULL\) 

Całkowita wartość kontraktu

### total\_contract\_value\_usdollar \| decimal \(NULL\) 

Całkowita wartość kontraktu w dolarach

### currency\_id \| varchar \(36\) 

{% hint style="info" %}
Identyikator -99 odnosi się do waluty domyślnej
{% endhint %}

### status \| nvarchar \(100\) 

Lista rozwijalna - przyjmuje jedną z wartości:

* Closed
* In Progress
* Not Started
* Signed

### customer\_signed\_date \| datetime \(NULL\) 

Data podpisania zamówienia przez klienta

### company\_signed\_date \| datetime \(NULL\) 

Data podpisania zamówienia przez Allcomp

### renewal\_reminder\_date \| datetime \(NULL\) 

Pole nieużywane, ale zawierające wartości typu datetime

### contract\_type \| nvarchar \(100\) 

Lista rozwijalna \(przyjmuje listę rozwijalną\)

* Kontrakt 
* Zamowienie

### contract\_account\_id \| varchar \(36\) 

{% hint style="warning" %}
Klucz obcy tabeli accounts
{% endhint %}

### opportunity\_id \| varchar \(36\) 

{% hint style="warning" %}
Klucz obcy tabeli opportunities
{% endhint %}

### contact\_id \| varchar \(36\) 

{% hint style="warning" %}
Klucz obcy tabeli contacts
{% endhint %}

### call\_id \| varchar \(36\) 

{% hint style="warning" %}
Klucz obcy tabeli calls
{% endhint %}

### total\_amt \| decimal \(NULL\) 

Wartość zamówienia netto \(przed rabatem\)

### total\_amt\_usdollar \| decimal \(NULL\) 

Nieużywane

### subtotal\_amount \| decimal \(NULL\) 

Wartość zamówienia netto po rabacie 

### subtotal\_amount\_usdollar \| decimal \(NULL\) 

Nieużywane

### discount\_amount \| decimal \(NULL\) 

Rabat

### discount\_amount\_usdollar \| decimal \(NULL\) 

Nieużywane

### tax\_amount \| decimal \(NULL\) 

Razem VAT

### tax\_amount\_usdollar \| decimal \(NULL\) 

Nieużywane

### shipping\_amount \| decimal \(NULL\) 

Nieużywane 

### shipping\_amount\_usdollar \| decimal \(NULL\) 

Nieużywane

### shipping\_tax \| nvarchar \(100\) 

Nieużywane

### shipping\_tax\_amt \| decimal \(NULL\) 

Nieużywane

### shipping\_tax\_amt\_usdollar \| decimal \(NULL\) 

Nieużywane

### total\_amount \| decimal \(NULL\) 

Razem brutto

### total\_amount\_usdollar \| decimal \(NULL\) 

Nieużywane

### quote\_id \| varchar \(36\)

Identyfikator oferty estymowanej na leadzie powiązanej z kontraktem

{% hint style="warning" %}
Klucz obcy tabeli aos\_quotes
{% endhint %}





