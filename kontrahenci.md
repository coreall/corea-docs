# Kontrahenci

### Pola wspólne

* id \| varchar \(36\)
* name \| nvarchar \(150\)
* date\_entered \| datetime \(NULL\)
* date\_modified \| datetime \(NULL\)
* modified\_user\_id \| varchar \(36\)
* created\_by \| varchar \(36\)
* description \| nvarchar \(-1\)
* deleted \| bit \(NULL\)
* assigned\_user\_id \| varchar \(36\)

### account\_type \| nvarchar \(100\)

Typ kontrahenta

{% hint style="info" %}
Lista rozwijalna. Przyjmuje jedną z wartości:

* Dealer 
* Dousu 
* Competitor 
* Prospekt 
* Customer 
* Partner\_Handlowy 
* Konkurencja\_Producent 
* Partner\_Handlowy\_Autoryzowany 
* Other
{% endhint %}

### industry \| nvarchar \(100\)

Branża przedsiębiorcy 

{% hint style="info" %}
Lista wielokrotnego wyboru przyjmuje wartości:

* ^Automotive^
* ^Biuro\_konstrukcyjne^
* ^Government^
* ^Homedecor^
* ^Homedecor^,^Obuwie^
* ^Kompozyty^
* ^Machinery^
* ^Meblarska^
* ^Meblarska^,^Obuwie^
* ^Not For Profit^
* ^Odziez^
* ^Pozostali^
* ^Technologies^
* ^Utilities^
* ^Zabawki^
{% endhint %}

### phone\_fax \| nvarchar \(100\)

Numer fax

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

### rating \| nvarchar \(100\)

W tym polu jest zapisywany numer NIP

### phone\_office \| nvarchar \(100\)

Telefon do biura

### phone\_alternate \| nvarchar \(100\)

Dodatkowy numer telefonu

### website \| nvarchar \(255\)

Strona internetowa

### ownership \| nvarchar \(100\)

Pole nieużywane

### employees \| nvarchar \(10\)

Pole nieużywane

### ticker\_symbol \| nvarchar \(10\)

Pole nieużywane

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

### parent\_id \| varchar \(36\)

{% hint style="info" %}
Klucz obcy tabeli accounts
{% endhint %}

### sic\_code \| nvarchar \(10\)

Pole nieużywane.

### campaign\_id \| varchar \(36\)

{% hint style="info" %}
Identyfikator powiązanej kampanii
{% endhint %}

### billing\_address\_region \| nvarchar \(255\)

Pole nieużywane

### shipping\_address\_region \| nvarchar \(255\)

Pole nieużywane

### id\_c \| varchar \(36\)

{% hint style="info" %}
Klucz obcy tabeli accounts
{% endhint %}

### jjwg\_maps\_lng\_c \| real \(NULL\)

Pole nieużywane

### jjwg\_maps\_lat\_c \| real \(NULL\)

Pole nieużywane

### jjwg\_maps\_geocode\_status\_c \| nvarchar \(255\)

Pole nieużywane

### jjwg\_maps\_address\_c \| nvarchar \(255\)

Pole nieużywane.

### forma\_po\_fin\_c \| nvarchar \(255\)

Pole nieużywane

### skala\_dzialani\_c \| nvarchar \(255\)

Pole nieużywane

### inf\_nat\_zatru\_c \| nvarchar \(255\)

Pole nieużywane

### rekrutacje\_c \| nvarchar \(255\)

Pole nieużywane

### aktualna\_sytuacja\_c \| nvarchar \(255\)

Pole nieużywane

### obecna\_technologia\_c \| nvarchar \(255\)

Pole nieużywane

### przebieg\_produkcji\_c \| nvarchar \(-1\)

Pole nieużywane

### plany\_c \| nvarchar \(-1\)

Pole nieużywane

### przyczyny\_inwestycji\_c \| nvarchar \(-1\)

Pole nieużywane

### wspolne\_ustalenia\_c \| nvarchar \(-1\)

Pole nieużywane

### wiedza\_c \| nvarchar \(-1\)

Pole nieużywane

### segmentacja\_c \| nvarchar \(100\)

{% hint style="info" %}
Pole przyjmuje postać listy rozwijalnej z wartościami

* -czysto- \[-czysto-\]
* Low \[Niska \| Bez potencjału\]
* Average \[Średnia\]
* High \[Wysoka\]
* PartnerT \[Partner Technologiczny\]
* CheckRequired \[Wymaga sprawdzenia\]
* WithPotential \[Z potencjałem\]
{% endhint %}

### pozyskanie\_c \| nvarchar \(100\)

{% hint style="info" %}
Pole przyjmuje postać listy rozwijalnej
{% endhint %}

### formaw\_c \| nvarchar \(255\)

Pole nieużywane

### ukladw\_c \| nvarchar \(255\)



### test\_c \| nvarchar \(-1\)

{% hint style="info" %}
Pole wyboru, specyfikacja branży:

* -czysto- \[-czysto-\]
* Meblarska\_SK \[Meblarska-Skórzane\]
* Meblarska\_DR \[Meblarska-Drewniane\]
* Meblarska\_m \[Meblarska-Materace\]
* Meblarska\_T \[Meblarska-Tapicerka\]
* Odziez\_B \[Odzież-Bielizna\]
* Odziez\_D \[Odzież-Dzianina\]
* Odziez\_G \[Odzież-Garnitury\]
* Odziez\_Dam \[Odzież-Damska/Ciężka\]
* Odziez\_FK \[Odzież-Futra/Kożuchy\]
* Odziez\_M \[Odzież-Medyczna\]
* Odziez\_K \[Odzież-Koszule\]
* Odziez\_ML \[Odzież-Męska/Lekka\]
* Odziez\_MUN \[Odzież-Mundurowa\]
* Odziez\_SK \[Odzież-Skórzana\]
* Odziez\_DC \[Odzież-Damska/Ciążowa\]
* Odziez\_DL \[Odzież-Damska/Lekka\]
* Odziez\_DZ \[Odzież-Dziecięca\]
* Odziez\_KU \[Odzież-Kurtki\]
* Odziez\_MC \[Odzież-Męska/Ciężka\]
* Odziez\_MLO \[Odzież-Młodzieżowa\]
* Odziez\_BHP \[Odzież-BHP\]
* Odziez\_SP \[Odzież-Sportowa\]
* Odziez\_SKAP \[Odzież-Stroje Kąpielowe\]
* Odziez\_PPR \[Odzież-Projektańci/Projektowanie\]
* Odziez\_SS \[Odzież-Suknie Ślubne\]
* Pozostali\_CZ \[Pozostali-Czapki\]
* Pozostali\_G \[Pozostali-Gąbki\]
* Pozostali\_MO \[Pozostali-Mopy\]
* Pozostali\_PM \[Pozostali-Płótna Malarskie\]
* Pozostali\_SP \[Pozostali-Spadochrony\]
* Pozostali\_WD \[Pozostali-Wózki Dziecięce\]
* Pozostali\_BA \[Pozostali-Balony\]
* Pozostali\_DY \[Pozostali-Dywany\]
* Pozostali\_KAP \[Pozostali-Kapelusze\]
* Pozostali\_PO \[Pozostali-Pościel\]
* Pozostali\_TE \[Pozostali-Techniczne\]
* Pozostali\_TO \[Pozostali-Torby\]
* Pozostali\_ZAG \[Pozostali-Żagle\]
* Homedecor\_Akcesoria \[Homedecor-Akcersoria\]
* Utilities\_KR \[Krojownia usługowa\]
{% endhint %}

### payment\_c \| nvarchar \(255\)

Pole nieużywane

### region\_c \| nvarchar \(255\)

Pole nie

### nip\_zagraniczny\_c \| nvarchar \(255\)

Pole, w którym jest zapisywany NIP zagraniczny

### telefon\_do\_biura\_2\_c \| nvarchar \(255\)

Telefon do biura

### liczba\_pracownikow\_c \| nvarchar \(100\)

{% hint style="info" %}
Lista rozwijalna przyjmująca jedną z wartości:

* -czysto- \[-czysto-\]
* between\_1\_9 \[Od 1 do 9 osób\]
* between\_10\_19 \[Od 10 do 19 osób\]
* between\_20\_49 \[Od 20 do 49 osób\]
* between\_50\_149 \[Od 50 do 149 osób\]
* between\_150\_249 \[Od 150 do 249 osób\]
* more\_than\_250 \[Więcej niż 250 osób\]
* ko\_c \| nvarchar \(-1\)
* liczba\_pracownikow\_konk\_c \| nvarchar \(100\)
* forma\_dzialanosci\_c \| nvarchar \(-1\)
* mocne\_strony\_c \| nvarchar \(-1\)
* slabe\_strony\_c \| nvarchar \(-1\)
* produkty\_c \| nvarchar \(-1\)
* payment\_capability\_c \| nvarchar \(100\)
* has\_products\_c \| nvarchar \(-1\)
* features\_old\_c \| nvarchar \(-1\)
* categories\_old\_c \| nvarchar \(-1\)
* cutter\_room\_c \| bit \(NULL\)
* ownership\_form\_list\_c \| nvarchar \(100\)
* gain\_c \| decimal \(NULL\)
{% endhint %}

### cutting\_room\_c \| nvarchar \(100\)

Informacja czy kontrahent posiada krojownię.

### notes\_itcube\_c \| nvarchar \(-1\)

Stare notatki z ITCUBE

### reccomendation\_c \| nvarchar \(100\)

Rekomendacja

### reference\_visit\_c \| nvarchar \(100\)

Wizyta referencyjna

### reference\_c \| nvarchar \(100\)

Referencje 

### earlier\_assigned\_to\_c \| nvarchar \(255\)

Wcześniej przypisane do

{% hint style="warning" %}
Pole aktualizowane na nakładką JS
{% endhint %}

### internal\_path\_c \| nvarchar \(255\)

Ścieżka do katalogu w domenie

