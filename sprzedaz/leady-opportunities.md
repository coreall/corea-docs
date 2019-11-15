# Leady

### Pola wspólne

* id \| varchar \(36\)
* name \| nvarchar \(50\) 
* date\_entered \| datetime \(NULL\) 
* date\_modified \| datetime \(NULL\) 
* modified\_user\_id \| varchar \(36\) 
* created\_by \| varchar \(36\) 
* description \| nvarchar \(-1\) 
* deleted \| bit \(NULL\) 
* assigned\_user\_id \| varchar \(36\) 
* currency\_id \| varchar \(36\) 
* id\_c \| varchar \(36\) 

### opportunity\_type \| nvarchar \(255\) 

Pole niewidoczne w SuiteCRM

{% hint style="info" %}
Lista rozwijalna. Może przyjąć wartości _\[Wartość zapisywana w DB\]_

* Wynika z istniejący umów _\[Existing Business\]_
* Nowo wypracowana _\[Nowo wypracowana\]_
{% endhint %}

### campaign\_id \| varchar \(36\) 

{% hint style="warning" %}
Klucz obcy tabeli campaigns
{% endhint %}

### lead\_source \| nvarchar \(100\) 

{% hint style="info" %}
Lista rozwijalna. 

* -czysto- \[-czysto-\] 
* Cold Call \[Cold Calling\] 
* Dealer \[Dealer\] 
* Self Generated \[Inicjatywa Własna Handlowca\] 
* Employee \[Z polecenia pracownika Allcomp\] 
* Partner \[Partner\] 
* Public Relations \[Public Relations\] 
* Web Site \[Formularz www\] 
* Word of mouth 
* \[Z polecenia klienta\] 
* Email \[Z emaila\] 
* Targi \[Targi\] 
* Phone \[Telefon\] 
* Press \[Prasa\] 
* Databases \[Z baz\] 
* Socialmedia \[Z social media\] 
* Internet \[Z internetu\] 
* Networking \[Networking\] 
* Ankieta \[Badanie Satysfakcji Klienta\]
{% endhint %}

### amount \| float \(NULL\) 

Pole określające wartość Leada netto.

{% hint style="success" %}
Na późniejszych etapach procesu sprzedaży wartość ta jest aktualizowana za pomocą 

1. Workflows w SuiteCRm
2. Cleanerów uruchamianych cyklicznie w aplikacji CoreA.
{% endhint %}

### amount\_usdollar \| float \(NULL\) 

Pole nieużywane 

### date\_closed \| datetime \(NULL\) 

Data zakończenia danego etapu 

> Pole widoczne w module Leady. Nie było nigdy jednak zwracane w żadnym z raportów.

### next\_step \| nvarchar \(100\) 

> Pole nieużywane

### sales\_stage \| nvarchar \(255\) 

Etap Leada

{% hint style="info" %}
Lista rozwijalna

* LeadNKrp \[LN\] 
* LNU \[LN - Anulowany\] 
* LeadKW \[LK Wycena\] 
* LeadKWof \[LK Oferta Wysłana\] 
* Closed Won \[LK Zakończony sukcesem\] 
* Closed Lost \[LK Zakończony porażką\] 
* LeadUn \[LK Unieważniony\] 
* Kontrakt\_Podpisany \[LK Zaliczka wpłynęła\]
{% endhint %}

### probability \| float \(NULL\) 

Prawdopodobieństwo. Za wyjątkiem gdy etap Leada jest równy LN prawdopodobieńtwo jest aktualizowane przez aplikację CoreA raz dziennie na podstawie zależności. /\*

```text
 * LN - 2%
 * LK Wycena - 10%
 * LK Oferta wysłana
 *      Oferta 20% - Lead 20%
 *      Oferta 40% - Lead 30%
 *      Oferta 60% - Lead 50%
 *      Oferta 80% - Lead 70%
 *      Oferta 100% - Lead 80%
 * LK Podpisany kontrakt - 90%
 * LK Zaliczka wpłtynęła - 100%
 */
```

### account\_id \| varchar \(36\) 

{% hint style="warning" %}
Klucz obcy tabeli accounts

**UWAGA!** Pole dodane zewnętrznie do tabeli opportunities, aby zoptymalizować raportowanie i wiązanie z tabelą. Natywnie w SuiteCRM tabele opportunities oraz accounts są powiazane relacją wiele-do-wielu zapośrednioczoną przez tabelę accounts\_opportunities. 

_Aktualizacja tego pola dokonuje się za pośrednictwem aplikacji CoreA_
{% endhint %}

### quote\_id \| varchar \(36\) 

{% hint style="warning" %}
Klucz obcy tabeli łączący z jedną ofertą \(Ofertą Estymowaną\).

**UWAGA!** Pole dodane zewnętrznie do tabeli opportunities, aby zoptymalizować raportowanie i wiązanie z tabelą quotes. Natywnie w SuiteCRM tabele opportunities oraz quotes są powiazane relacją jeden-do-wielu \(jeden lead ma wiele ofert\). 

_Aktualizacja tego pola dokonuje się za pośrednictwem aplikacji CoreA_
{% endhint %}

### contract\_id \| varchar \(36\) 

{% hint style="warning" %}
Klucz obcy tabeli łączący z tabelą contracts

**UWAGA!** Pole dodane zewnętrznie do tabeli opportunities, aby zoptymalizować raportowanie i wiązanie z tabelą contracts. Natywnie w SuiteCRM tabele opportunities oraz quotes są powiazane relacją jeden-do-wielu \(jeden lead ma wiele ofert\). Dzięki temu uzupełnieniu symulujemy relację jeden-do-jednego.

_Aktualizacja tego pola dokonuje się za pośrednictwem aplikacji CoreA._
{% endhint %}

### tax \| float \(NULL\) 

> Podatek VAT \(w procentach\).

{% hint style="warning" %}
Pole nie znajduje się natywnie w SuiteCRM. Aktualiazacja tego pola dokonuje się na podstawie wartości zapisanej w ofercie estymowanej.
{% endhint %}

### jjwg\_maps\_lng\_c \| real \(NULL\) 

> Pole nieużywane. Dedykowane do zapisywania współrzędnych geograficznych. W przypadku podania adresu \[jjwg\_maps\_address\_c\] pole może zostać zmapowane za pomocą Google API

### jjwg\_maps\_lat\_c \| real \(NULL\) 

> Pole nieużywane. Dedykowane do zapisywania współrzędnych geograficznych. W przypadku podania adresu \[jjwg\_maps\_address\_c\] pole może zostać zmapowane za pomocą Google API

### jjwg\_maps\_geocode\_status\_c \| nvarchar \(255\) 

> Pole nieużywane.Dedykowane dla zapisywania informacji czy powiodło się geotaggowanie

### jjwg\_maps\_address\_c \| nvarchar \(255\) 

> Pole nieużywane

### data\_zamkniecia\_c \| datetime \(NULL\) 

> Pole zawierające informację odnośnie planowanej daty zamknięcia Leada. Aktualizowane na podstawie Daty zamknięcia w Ofercie oraz daty podpisania w Zamówienie.

### wymagania\_konwersja\_c \| nvarchar \(-1\)

> ABY PRZEJŚĆ do następnego etapu: - uzupełnij matrycę potrzeb i jeżeli to konieczne matrycę obiekcji - dodaj ofertę pod lead-em na etapie wstępnej wyceny, dodając wstępną datę zamknięcia.

> ABY PRZEJŚĆ do następnego etapu: - wśród osób kontaktowych przypisanych do kontrahenta oznacz DECYDENTA - skoryguj ofertę na gotową, dodaj pod ofertę osobę kontaktową \(decydent\)oraz zmień etap oferty na oferta wysłana jeżeli będzie konieczne, zaktualizuj szacowaną datę zamknięcia.

> Kontynuuj pracę z obiekcjami oraz potrzebami lead-u. - wśród kontaktów lead-u postaraj się znaleźć DECYDENTA - wszelkie obiekcje lead-u muszą zostać zapisane w matrycy obiekcji - W karcie handlowej musi zostać opisana obecna technologia oraz przebieg produkcji ABY przejść do następnego etapu skoryguj ofertę na gotową oraz zmień etap oferty na oferta wysłana jeżeli będzie konieczne zaktualizuj szacowaną datę zamknięcia.

> Po zamknięciu lead-u jako wygranego back office handlu założy PROJEKT OBSŁUGI SPRZEDAŻY \(po uzyskaniu dostępu, skontroluj poprawność danych\) Wszelkie nowe ustalenia z klientem dodawaj pod projekt. Zielona karta może zostać prowadzona za pomocą zmian w projekcie.

> Po zamknięciu lead-u jako wygranego back office handlu założy PROJEKT OBSŁUGI SPRZEDAŻY \(po uzyskaniu dostępu, skontroluj poprawność danych\) Wszelkie nowe ustalenia z klientem dodawaj pod projekt. Zielona karta może zostać prowadzona za pomocą zmian w projekcie.

> Wszelkie kontakty oraz spotkanie muszą zostać dodane do systemu Jeżeli uda się podpisać kontrakt oznacz ofertę na wygraną. - wszystkie oficjalne dokumenty muszą zostać dodane pod kontrahenta - dodaj do sytemu informację o rodzaju gwarancji Jeżeli przegramy ofertę oznaczymy ją jako zamknięta przegrana i w opisie leda-a dodajemy dokładny opis przyczyny przegranej. Jeżeli lead zostanie unieważniony \(kontrahent odstępuje od zakupu ze względu na bliżej nieokreślone przesłanki\) oznacz lead jako zamknięty unieważniony i opisz przyczyny. Pamiętaj że Lead sam wygaśnie po 45 dniach od wysłania oferty.

### okreslenieleada\_c \| nvarchar \(-1\) 

> Wstępna zawartość Leada.

{% hint style="info" %}
Lista wybieralna

* Cutter \[CUTTER WIELOWARSTWOWY\] 
* OneLayerCutter \[CUTTER JEDNOWARSTWOWY\] 
* Lagowarka \[LAGOWARKA\] 
* Stol \[STÓŁ\] 
* CAD \[PROGRAM CAD\] 
* Prime\_5 \[PRIME .5\] 
* ONE.5plus \[one .5 +\] 
* ONE.5 \[one .5\] 
* Optitex \[OPTITEX\] 
* 3C50 \[3C50\] 
* CC80 \[CC80\] 
* AERO \[aero\] 
* Caron \[Caron\] 
* Ploter \[Ploter\] 
* Digitizer \[DIGITIZER\] 
* Inne \[INNE\] 
* Dealer \[Dealer\] 
* Training \[Szkolenie Optitex\]
{% endhint %}

### przyczyna\_porazki\_c \| nvarchar \(255\) 

Pole domyślnie ukryte. Do uzupełnienia, gdy etap leada jest równy Closed Lost \[LK Zakończony porażką\] 

### przyczyna\_wygranej\_c \| nvarchar \(-1\) 

Pole domyślnie ukryte. Do uzupełnienia, gdy etap leada jest równy Closed Won \[LK Zakończony sukcesem\] 

### account\_id\_c \| varchar \(36\) 

{% hint style="warning" %}
Klucz obcy tabeli accounts.
{% endhint %}

### typ\_maszyny\_c \| nvarchar \(255\) 

> Nie używane

### nr\_lead\_c \| nvarchar \(255\) 

> Numer Leada

### nr\_kolejny\_c \| int \(NULL\) 

> Pierwszy segment z numeru leada

### cancel\_category\_c \| nvarchar \(100\) 

{% hint style="info" %}
Lista wybieralna

* -czysto- \[-czysto-\] 
* MachineIssue \[Brak urządzenia w ofercie\] 
* FinanceIssue \[Brak środków finansowych\] 
* CustomerIssue \[Klient rozmyślił się\] 
* TechnicalIssue \[Nie tniemy takiego materiału\]
{% endhint %}

### installation\_date\_c \| datetime \(NULL\)

Data instalacji

{% hint style="warning" %}
Data instalacji jest aktualizowana na podstawie Oferty Estymowanej i Zamówienia.
{% endhint %}

### 

