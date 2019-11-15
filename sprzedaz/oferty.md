# Oferty

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

### approval\_issue \| nvarchar \(-1\)

Informacja do akceptacji

### billing\_account\_id \| varchar \(36\)

{% hint style="warning" %}
Klucz obcy tabeli accounts
{% endhint %}

### billing\_contact\_id \| varchar \(36\)

{% hint style="warning" %}
Klucz obcy tabeli contacts
{% endhint %}

### billing\_address\_street \| nvarchar \(150\)

Adres kontrahenta - ulica

### billing\_address\_city \| nvarchar \(100\)

Adres kontrahenta - miasto

### billing\_address\_state \| nvarchar \(100\)

Adres kontrahenta - województwo

### billing\_address\_postalcode \| nvarchar \(20\)

Adres kontrahenta - kod pocztowy

### billing\_address\_country \| nvarchar \(255\)

Adres kontrahenta - państwo

### shipping\_address\_street \| nvarchar \(150\)

Adres dostawy - ulica

### shipping\_address\_city \| nvarchar \(100\)

Adres dostawy - miasto

### shipping\_address\_state \| nvarchar \(100\)

Adres dostawy - województwo

### shipping\_address\_postalcode \| nvarchar \(20\)

Adres dostawy - kod pocztowy

### shipping\_address\_country \| nvarchar \(255\)

Adres dostawy - państwo

### expiration \| datetime \(NULL\)

Data ważności oferty

### number \| int \(NULL\)

Numer oferty

### opportunity\_id \| varchar \(36\)

{% hint style="info" %}
Klucz obcy tabeli opportunities
{% endhint %}

### template\_ddown\_c \| nvarchar \(-1\)

Pole nieuzżwane

### total\_amt \| decimal \(NULL\)

Kwota \[Razem netto\]

### total\_amt\_usdollar \| decimal \(NULL\)

Pole nieużywane

### subtotal\_amount \| decimal \(NULL\)

Kwota \[Razem netto po rabacie\]

### subtotal\_amount\_usdollar \| decimal \(NULL\)

Pole nieużywane

### discount\_amount \| decimal \(NULL\)

Wartość zniżki

### discount\_amount\_usdollar \| decimal \(NULL\)

Pole nieużywane

### tax\_amount \| decimal \(NULL\)

Wartość podatku

### tax\_amount\_usdollar \| decimal \(NULL\)

Pole nieżywane

### shipping\_amount \| decimal \(NULL\)

Koszt dostawy

### shipping\_amount\_usdollar \| decimal \(NULL\)

Pole nieużywane

### shipping\_tax \| nvarchar \(100\)

Pole nieużywane.

### shipping\_tax\_amt \| decimal \(NULL\)

Pole nieużywane.

### shipping\_tax\_amt\_usdollar \| decimal \(NULL\)

total\_amount \| decimal \(NULL\)

### total\_amount\_usdollar \| decimal \(NULL\)

Pole nieużywane

### currency\_id \| varchar \(36\)

```text
Klucz obcy tabel
```

### stage \| nvarchar \(100\)

Status oferty

### term \| nvarchar \(100\)

Pole nieużywane

### terms\_c \| nvarchar \(-1\)

Pole nieużywane

### approval\_status \| nvarchar \(100\)

Przyjmuje wartości

* Wymaga Akceptacji
* Nie wymaga 

### invoice\_status \| nvarchar \(100\)

Pole nieużywane

### subtotal\_tax\_amount \| decimal \(NULL\)

Pole nieużywane

### subtotal\_tax\_amount\_usdollar \| decimal \(NULL\)

Pole nieużywane

### billing\_address\_region \| nvarchar \(255\)

Pole nieużywane

### shipping\_address\_region \| nvarchar \(255\)

Pole nieużywane

### nr\_oferty \| nvarchar \(255\)

Numer oferty

### id\_c \| varchar \(36\)

```text
Identyfikator tabeli aos_quotes_cstm
```

### werfyfikacja\_techniczna\_c \| nvarchar \(100\)

Pole nieużywane

### warunki\_c \| nvarchar \(-1\)

Pole nieużywane

### warunkig\_c \| nvarchar \(-1\)

Pole nieużywane

### przyczyna\_porazki\_c \| nvarchar \(255\)

Pole tekstowe do opisania przyczyny wygranej

### przyczyna\_wygranej\_c \| nvarchar \(-1\)

Pole tekstowe do opisania przyczyny wygranej

### account\_id\_c \| varchar \(36\)

Połączony kontrahent

```text
Klucz obcy tabeli account
```

### typ\_maszyny\_c \| nvarchar \(255\)

Pole nieużywane

### typ\_oferty\_c \| nvarchar \(100\)

Pole typu dropdown przyjmujące wartości: 

* Estymowana, 
* Wariant

### akceptacja\_dyrekcja\_c \| bit \(NULL\)

Pole oznaczane przez dyrekcję

### akceptacja\_handlowiec\_c \| bit \(NULL\)

Pole oznaczane przez handlowca 

### akceptacja\_finansowa\_c \| bit \(NULL\)

akceptacja\_inz\_prod\_c \| bit \(NULL\)

### weryfikacja\_finansowa\_c \| nvarchar \(100\)

Pole nieużywane.

### weryfikacja\_inz\_c \| nvarchar \(100\)

Pole nieużywane.

### typ\_produktu\_c \| nvarchar \(100\)

Pole nieużywane.

### akceptacja\_techniczna\_c \| bit \(NULL\)

Pole nieużywane.

### powiadom\_dyrekcje\_c \| nvarchar \(1\)

Pole nieużywane.

### date\_sent\_quote\_c \| datetime \(NULL\)

Data wysłania oferty - aktualizowane przez proces

### installation\_date\_c \| datetime \(NULL\)

Data instalacji - aktualizowana na podstawie kontraktu

### closed\_won\_probability\_c \| nvarchar \(100\)

Prawdopodobieństwo wygranej

{% hint style="danger" %}
Pole aktualizowane za pomocą narzędzia do przedłużania ofert
{% endhint %}

