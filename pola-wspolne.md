# Pola wspólne

### id \| varchar \(36\) 

Unikalny identyfikator rekordu

### name \| nvarchar \(50\) 

Nazwa rekordu

### date\_entered \| datetime 

Data i czas wprowadzenia rekordu do bazy

### date\_modified \| datetime 

Data i czas ostatniej modyfikacji rekordu w bazie danych

### modified\_user\_id \| varchar \(36\) 

> Klucz obcy łączący z tabelą users

### created\_by \| varchar \(36\) 

```text
Klucz obcy łączący z tabelą users
```

### description \| nvarchar \(-1\) 

Pole przechowujące opis rekordu. Długi tekst

### deleted \| bit  

Pole przechowujące informację o tym czy dany rekord został oznaczony jako usunięty. 

{% hint style="warning" %}
Aplikacje CoreA oraz SuiteCRM pokazuję jedynie rekordy gdzie **deleted  = 0**.
{% endhint %}

### assigned\_user\_id \| varchar \(36\) 

{% hint style="warning" %}
Klucz obcy łączący z tabelą users.
{% endhint %}

### currency\_id \| varchar \(36\) 

```text
Klucz obcy tabeli currencies
```

Lista rozwijalna generowana na postawie currency\_id

* EUR
* PLN
* USD

### id\_c \| varchar \(36\) 

