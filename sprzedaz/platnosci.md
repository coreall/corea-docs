# Płatności

### id \(UUID\)

Niepowtarzalny identyfikator dla każdej płatności.

### opportunity\_id \(UUID\)

{% hint style="warning" %}
Klucz obcy łączący z tabelą opportunities.
{% endhint %}

identyfikator Leada, z którym jest połączona dana płatność. Również w formacie UUID

### contract\_id \(UUID\)

Identyfikator Zamówienia, z którym jest powiązana dana płatność. W formacie UUID.

### type 

Lista wybieralna z rodzajami płatności 

* Spodziewana \[expected\]
* Dokonana \[actual\]

### name 

Lista wybieralna z nazwą płatności. Przyjmuje jedną z trzech wartości.

* Zaliczka START
* Zaliczka PRZED DOSTAWĄ
* Inna wpłata

### payment\_date 

Data płatności. Wartość w tym polu jest zależna od wartości wpisanej w pole _date\_calculation\_method._ Jeżeli _date\_calculation\_method_ jest równe:

* **strict -** wartość payment\_date jest wpisywana z ręki i nie podlega modyfikacjom;
* **after\_signing** - wartość payment\_date jest obliczana w relacji do daty podpisania kontraktu \(gdy nie ma jeszcze podpisanego kontraktu tę wartość antycypuje nam data zamknięcia leada 
* **before\_installation** - wartość payment\_date jest obliczana w stosunku do daty\_instalacji. Jeżeli nie mamy podanej daty instalacji nie można wprowadzić tej wartości.
* **after\_installation** - wartość payment\_date jest obliczana w stosunku do daty\_instalacji. Jeżeli nie mamy podanej daty instalacji nie można wprowadzić tej wartości.

### payment\_amount\_netto 

Kwota płatności netto, Wartość w tym polu jest zależna od wartości zapisanej w polu _amount\_calculation\_method_. Jeżeli amount\_calculation\_method jest równe:

* strict - wartość jest wpisywana z ręki i nie jest modyfikowana żadnymi obliczeniami
* percent - wartość przeliczana jako procent wartości całego Leada.

### payment\_amount\_brutto 

Kwota płatności netto powiększona o % podatku wskazany na poziomie Zamówienia, Oferty, czy Leada. Uwaga: Dla Leadów zagranicznych oraz Leadów Niekwalifikowanych wartość ta może wynosić 0%.

### checksum 

Wartość kontrolna dla płatności. Niezależnie od waluty, w której została zapisana płatnosć oraz czy została zapisana pierwotnie jako kwota netto czy brutto, **wartość checksum zawsze jest przeliczana do wartości netto wyrażonej w walucie EUR.**

### is\_advance 

Wartość logiczna \(prawda / fałsz\) określająca czy dana płatność powinna być traktowana jako zaliczka. Na poziomie interfejsu użytkownika jest założony skrypt, który sprawia, że już na etapie wprowadzania danych wartość is\_advance jest określona jako true dla płatności, gdzie name równa się "Zaliczka START" lub "Zaliczka PRZED DOSTAWĄ" oraz jest określana jako false dla płatności gdzie name = "Inna wpłata".

### invoice 

Numer faktury w systemie Optima.

### deleted 

Pole ukryte. Określa czy dana płatność nie została usunięta.

### currency\_id 

Identyfikator waluty danej płatności. 

* \[-99\] - wartość domyślna - EUR
* d757c114-e5f9-ddd0-c410-5927c9c07a0b - PLN
* 6fb20afe-7671-489c-7529-5927c9822530 - USD

#### conversion\_rate 

Przelicznik w stosunku do EURO dla danej waluty. Dla płatności jest pobierana z banku NBP z dnia poprzedającego dzień wpłaty.

### conversion\_date 

Data przewalutowania. Zasadniczo jest to dzień poprzedzajacy dzień wpłaty, a w przypadku, gdy w danym dniu NBP nie publikowało kursów walut, będzie to data poprzedzająca dany dzień.

### date\_calculation\_value 

### date\_calculation\_method 

Sposób obliczania daty płatności. Może przyjąć następujące wartości.

* strict
* after\_signing
* before\_installation
* after\_installation

### amount\_calculation\_method 

Sposob naliczania kwoty płatności. Może przyjąć następujące wartości

* strict
* percent

### percent 

Procent kwoty oznaczonej jako kwota kontraktu.

### note 

Miejsce na notatkę dotyczącą płatności. Max 255 znaków.

### created\_by \(UUID\)

Identyfikator użytkownika, który utworzył rekord

### modified\_by \(UUID\)

Identyfikator użytkownika, który dokonał ostatniej aktualizacji na danym rekordzie.

### frozen\_by 

Identyfikator użytkownika, który zablokował rekord do dalszej edycji.

### frozen\_at 

Data \(timestamp\) zablokowania rekordu do dalszej edycji.

### created\_at 

Data \(timestamp\) utworzenia rekordu.

### updated\_at

Data \(timestamp\) ostatniej aktualizacji rekordu.

### checksum\_brutto

Wartość kontrolna dla płatności. Niezależnie od waluty, w której została zapisana płatnosć oraz czy została zapisana pierwotnie jako kwota netto czy brutto, **wartość checksum zawsze jest przeliczana do wartości BRUTTO wyrażonej w walucie EUR.**



