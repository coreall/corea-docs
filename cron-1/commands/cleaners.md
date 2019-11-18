# Cleaners

## CleanerForEveryFiveMinutes

{% hint style="info" %}
Uruchamiany co każde 5 minut
{% endhint %}

Wrzuca do workera następujące prace

### CheckForUnrelatedOpportunitiesJob

Łańcuch poleceń, który

* Usuwa wpisy oznaczone jako deleted z tabeli accounts\_opportunities
* Usuwa podwójne połączenia leada a kontrahentem \(pozostawia tylko najnowsze\)
* W tabeli opportunities nadpisuje wartość w polu account\_id

### CheckForUnrelatedContractsJob

W tabeli aos\_contracts w polu quote\_id wpisuje identyfikator powiązanej oferty

### LeaveOnlyOneEstimatedJob

Sprawdza czy na Leadzie istnieje więcej niż jedna oferta estymowana. Zdublowaną zmienia na Wariant. 

### EmptyProductsGroupsCleanerJob

Usuwa utworzone tymczasowo grupy, które nie zawierają żadnych produktów

### RemoveDeletedProductsQuotesJob

Usuwa produkty oznaczone jako \[deleted\].

### SynchronizeInstallationDatesJob

Ujednolica datę instalacji w modułach Leady, Oferty oraz Zamówienia

### InOpportunitiesUpdateQuoteId

W tabeli opportunities aktualizuje w polu quote\_id identyfikator powiązanej oferty estymowanej. 

### InOpportunitiesUpdateContractId

W tabeli opportunities aktualizuje w polu quote\_id identyfikator powiązanego zamówienia \(tylko jeśli zamówienie jest oparte na prawidłowo wystawionej ofercie\). 

### InOpportunitiesUpdateTax

W tabeli opportunities aktualizuje pole tax na podstawie a\) oferty, b\) zamówienia

### UpdateProductMaincodeJob

W tabeli aos\_products aktualizuje pole maincode

### DeleteRelatedDataForRemovedContract

Po usunięciu zamówienia usuwa połączone rekordy z tabel

* payments, 
* contract\_involvements
* contract\_accountings

## CleanerForEveryHour

{% hint style="info" %}
Uruchamiane raz na godzinę
{% endhint %}

Wrzuca do workera następujące zadanie:

### RecalculateAllPaymentsJob

Przelicza płatności, we wszystkich zamówieniach, które mają status inny niż \[Closed\]. 

## CleanerForEveryDay

{% hint style="info" %}
Uruchamiane raz dziennie o godz. 03:03 AM
{% endhint %}

Wrzuca do workera następujące zadania:

### SecurityGroupsCleanerMaster

Porządkuje uprawnienia na poziomie SuiteCRM wykonując następujące zadania:

**RemoveDeletedSecurityGroupsRecords** 

Z tabeli securitygroups\_record usuwa rekordy oznaczone jako \[deleted\]

#### ManageUnassignedPolishAccountsJob 

Rekordy przypisane do użytkownika \[Unassigned\] przenosi do grupy \[Unassigned\] i usuwa z innych grup. Dotyczy "polskich" rekordów.

#### ManageUnassignedRomanianAccountsJob 

Rekordy przypisane do użytkownika \[Unassigned\] przenosi do grupy \[Unassigned\] i usuwa z innych grup. Dotyczy "rumuńskich" rekordów.

#### ManageUnassignedInternationalAccountsJob 

Rekordy przypisane do użytkownika \[Unassigned\] przenosi do grupy \[Unassigned\] i usuwa z innych grup.

#### ManageAccountsAssignedToPolishSalesmakersJob 

Rekordy przypisane do "polskiego" handlowca przypisuje do grupy polskich handlowców i usuwa z grupy \[Unassigned\]

#### ManageAccountsAssignedToRomanianSalesmakersJob 

Rekordy przypisane do "rumuńskiego" handlowca przypisuje do grupy rumuńskich handlowców i usuwa z grupy \[Unassigned\]

#### ManageAccountsAssignedToInternationalSalesmakersJob 

Rekordy przypisane do "zagranicznego" handlowca przypisuje do grupy zagranicznych handlowców i usuwa z grupy \[Unassigned\]

#### ManageContactsJob 

Usuwa grupy dostępu z rekordów w module Kontatkty. Założenie jest takie, że kontaktami zarządza się na poziomie ogólnych uprawnień, a nie przez grupy. 

#### ManageActivitiesGroupsJob 

Usuwa grupy dostępu z rekordów w modułach Rozmowy, Zadania, Spotkania. Założenie jest takie, że kontaktami zarządza się na poziomie ogólnych uprawnień, a nie poprzez grupy. 

#### ManageProductsInStandardPriceListJob 

Przypisuje wybrane produkty do standardowego cennika. 

#### ManageProductsInRomanianPriceListJob 

Przypisuje wybrane produkty do rumuńskiego cennika.

#### ManageOpportunitiesAssignedToSingleSalesmakerJob 

Zarządza grupami dostępu dla leadów przypisanych do jednego, wybranego handlowca.

#### ManageOpportunitiesAssignedToCooperationGroupJob 

Zarządza grupami dostępu dla leadów przypisanych do grup kooperacji

#### ManageQuotesAssignedToSingleSalesmakerJob 

Zarządza grupami dostępu dla ofert przypisanych do jednego, wybranego handlowca.

#### ManageQuotesAssignedToCooperationGroupJob 

Zarządza grupami dostępu dla ofert przypisanych do grup kooperacji

#### ManageContractsAssignedToSingleSalesmakerJob 

Zarządza grupami dostępu dla zamówień przypisanych do jednego, wybranego handlowca.

#### ManageContractAssignedToCooperationGroupJob

Zarządza grupami dostępu dla zamówień przypisanych do grup kooperacji

### SaveMissingAccountIdInContactsJob

W tabeli contacts aktualizuje wartość w polu account\_id

### GetSnapshotOfPhoneNumbers

Wyciąga wszystkie numery telefonów z modułów Kontrahenci oraz Kontakty, oczyszcza je i tworzy z nich przeszukiwalny indeks.

### SyncCurrenciesIdInSalesProcessJob

Ujednolica wartość polu currency\_id w modułach Leady, Oferty oraz Zamówienia

### RecalculateAllContractsSummariesJob

Przelicza na nowo wszystkie dane w tabeli contract\_summaries

## CleanerForEveryWeek

### AllcompCleanerJob

Usuwa powiązane Leady, Oferty i Kontrakty z rekordu testowego Allcomp



