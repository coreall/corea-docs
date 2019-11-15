# Kontakty

### Pola wspólne

* id \| varchar \(36\)
* date\_entered \| datetime \(NULL\)
* date\_modified \| datetime \(NULL\)
* modified\_user\_id \| varchar \(36\)
* created\_by \| varchar \(36\)
* description \| nvarchar \(-1\)
* deleted \| bit \(NULL\)
* assigned\_user\_id \| varchar \(36\)

### salutation \| nvarchar \(255\)

Pole nieużywane

### first\_name \| nvarchar \(100\)

Imię

### last\_name \| nvarchar \(100\)

Nazwisko

### title \| nvarchar \(100\)

Pole nieużywane. 

{% hint style="danger" %}
Typ pola \(nie da się tego zmienić\) to pole tekstowe. Pole to umożliwia wpisanie z ręki dowolnej wartości. W to miejscu proponowane jest używanie pola zawierajacego listę wybieralną \[stanowisko\_c\].
{% endhint %}

### photo \| nvarchar \(255\)

Pole nieużywane

### department \| nvarchar \(255\)

Pole nieużywane

### do\_not\_call \| bit \(NULL\)

Pole nieużywane

### phone\_home \| nvarchar \(100\)

Telefon domowy

### phone\_mobile \| nvarchar \(100\)

Telefon komórkowy

### phone\_work \| nvarchar \(100\)

Telefon do pracy

### phone\_other \| nvarchar \(100\)

Inny telefon

### phone\_fax \| nvarchar \(100\)

Numer faksu

### primary\_address\_street \| nvarchar \(150\)

Adres kontaktu - ulica

### primary\_address\_city \| nvarchar \(100\)

Adres kontaktu - miasto

### primary\_address\_state \| nvarchar \(100\)

Adres kontaktu - województwo

### primary\_address\_postalcode \| nvarchar \(20\)

Adres kontaktu - kod pocztowy

### primary\_address\_country \| nvarchar \(255\)

Adres kontaktu - państwo

### alt\_address\_street \| nvarchar \(150\)

Adres kontaktu - ulica

### alt\_address\_city \| nvarchar \(100\)

Pole nieużywane

### alt\_address\_state \| nvarchar \(100\)

Pole nieużywane

### alt\_address\_postalcode \| nvarchar \(20\)

Pole nieużywane

### alt\_address\_country \| nvarchar \(255\)

Pole nieużywane

### assistant \| nvarchar \(75\)

Pole nieużywane

### assistant\_phone \| nvarchar \(100\)

Pole nieużywane

### lead\_source \| nvarchar \(255\)

Pole nieużywane

### reports\_to\_id \| varchar \(36\)

Pole nieużywane

### birthdate \| datetime \(NULL\)

Pole nieużywane

### campaign\_id \| varchar \(36\)

Pole nieużywane

### joomla\_account\_id \| nvarchar \(255\)

Pole nieużywane

### portal\_account\_disabled \| bit \(NULL\)

Pole nieużywane

### portal\_user\_type \| nvarchar \(100\)

Pole nieużywane

### primary\_address\_region \| nvarchar \(255\)

Pole nieużywane

### alt\_address\_region \| nvarchar \(255\)

Pole nieużywane

### account\_id \| varchar \(36\)

{% hint style="warning" %}
Domyślnie w SuiteCRM moduły \[accounts\] oraz \[contacts\] są połączone relacją wiele-do-wielu za pośrednictwem tabeli \[accounts\_contacts\]. Pole account\_id jest nadpisywane osobnym skryptem za pośrednictwem aplikacji CoreA.
{% endhint %}

### name \| nvarchar \(201\)

{% hint style="info" %}
Pole zawierające 
{% endhint %}

### jjwg\_maps\_lng\_c \| real \(NULL\)

Pole nieużywane

### jjwg\_maps\_lat\_c \| real \(NULL\)

Pole nieużywane

### jjwg\_maps\_geocode\_status\_c \| nvarchar \(255\)

Pole nieużywane

### jjwg\_maps\_address\_c \| nvarchar \(255\)

Pole nieużywane

### rolazakupowa\_c \| nvarchar \(100\)

{% hint style="info" %}
Lista wybieralna zawierająca jedną z wartości:

* -czysto- \[-czysto-\]
* Decydent \[Decydent\]
* Poszkodowany \[Poszkodowany\]
* Doradca \[Doradca\]
* Pilot \[Pilot\]
{% endhint %}

### obszar\_allcomp\_c \| nvarchar \(100\)

Pole nieużywane

### stanowisko\_c \| nvarchar \(100\)

{% hint style="info" %}
Lista wybieralna, która przyjmuje jedną z wartości

* -czysto- \[-czysto-\]
* Właściciel \[Właściciel\]
* Współwłaściciel \[Współwłaściciel\]
* Prezes \[Prezes\]
* Wiceprezes \[Wiceprezes\]
* Prezes Zarządu \[Prezes Zarządu\]
* Wiceprezes Zarządu \[Wiceprezes Zarządu\]
* Dyrektor zarządu \[Dyrektor zarządu\]
* Dyrektor generalny \[Dyrektor generalny\]
* Zastępca dyrektora zarządu \[Zastępca dyrektora zarządu\]
* Członek zarządu \[Członek zarządu\]
* Przewodniczący rady nadzorczej \[Przewodniczący rady nadzorczej\]
* Członek rady nadzorczej \[Członek rady nadzorczej\]
* Prokurent \[Prokurent\]
* Sekretarka \[Sekretarka\]
* Dyrektor zakładu \[Dyrektor zakładu\]
* Dyrektor\_handlowy \[Dyrektor handlowy\]
* Dyrektor finansowy \[Dyrektor finansowy\]
* Dyrektor produkcji \[Dyrektor produkcji\]
* Dyrektor techniczny \[Dyrektor techniczny\]
* Dyrektor projektu \[Dyrektor projektu\]
* Dyrektor ds. organizacyjnych \[Dyrektor ds. organizacyjnych\]
* Zastępca szefa produkcji \[Zastępca szefa produkcji\]
* Kierownik krojowni \[Kierownik krojowni\]
* Kierownik przygotowania produkcji \[Kierownik przygotowania produkcji\]
* Kierownik biura konstrukcji \[Kierownik biura konstrukcji\]
* Kierownik wzorcowni \[Kierownik wzorcowni\]
* Kierownik działu technicznego \[Kierownik działu technicznego\]
* Kierownik utrzymania ruchu \[Kierownik utrzymania ruchu\]
* Kierownik tapicerni \[Kierownik tapicerni\]
* Kierownik szwalni \[Kierownik szwalni\]
* Kierownik działu technologicznego \[Kierownik działu technologicznego\]
* Kierownik jakości \[Kierownik jakości\]
* Kierownik optymalizacji procesów \[Kierownik optymalizacji procesów\]
* Menager ds. produkcji \[Menager ds. produkcji\]
* Menager ds. rozwoju \[Menager ds. rozwoju\]
* Główny mechanik \[Główny mechanik\]
* Główny technolog \[Główny technolog\]
* Doradca techniczny \[Doradca techniczny\]
* Specjalista ds. jakości \[Specjalista ds. jakości\]
* Specjalista ds. rozwoju \[Specjalista ds. rozwoju\]
* Specjalista ds. tekstyliów \[Specjalista ds. tekstyliów\]
* Specjalista ds. Kontroli Danych Produkcyjnych \[Specjalista ds. Kontroli Danych Produkcyjnych\]
* Specjalista ds. nowych wdrożeń \[Specjalista ds. nowych wdrożeń\]
* Specjalista ds. szablonów/wykroju \[Specjalista ds. szablonów/wykroju\]
* Specjalista ds. Utrzymania Ruchu \[Specjalista ds. Utrzymania Ruchu\]
* Konstruktor \[Konstruktor\]
* Projektant \[Projektant\]
* Technik \[Technik\]
* Tapicer \[Tapicer\]
* Krojczy \[Krojczy\]
* Obsługa maszyn \[Obsługa maszyn\]
* Kierownik zaopatrzenia \[Kierownik zaopatrzenia\]
* Specjalista ds. logistyki \[Specjalista ds. logistyki\]
* Główna księgowa \[Główna księgowa\]
* Inne \[Inne\]
* Production\_manager \[Kierownik produkcji\]
{% endhint %}

### plec\_c \| nvarchar \(100\)

Pole nieużywane

### przedzial\_wiekowy\_c \| nvarchar \(100\)

Pole nieużywane

### facebook\_c \| nvarchar \(255\)

Pole nieużywane

### linkedin\_c \| nvarchar \(255\)

Pole nieużywane

### active\_c \| nvarchar \(100\)

Informacja czy dany kontakt jest aktywny

