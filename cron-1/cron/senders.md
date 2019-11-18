# Senders

## SendDailyNotifications

{% hint style="info" %}
Uruchamia się codziennie o godz 04:01 AM
{% endhint %}

```php
# app\Console\Commands\SendDailyNotifications.php
$schedule->command('send:daily')->dailyAt('04:01');
```

### SendReminderAboutUpcomingPayments

Przypomnienie o nadchodzących planowanych płatnościach

### ReminderAboutBillingRequestJob

Przypomnienie o zleceniu fakturowania

## SendReportAboutExpiredQuotesToCeoCommand

{% hint style="info" %}
Uruchamia się raz w tygodniu o godz. 04:13 AM
{% endhint %}

```php
# app\Console\Commands\Mails\SendReportAboutExpiredQuotesToCeoCommand.php
$schedule->command('send:opportunities-expiration')->weeklyOn(1, '04:13');
```

Wysyła informację na temat kończących się oraz przeterminowanych ofert do Pana Prezesa oraz przypisanych handlowców

## SendQuotesToApproveCommand

{% hint style="info" %}
Uruchamia się raz dziennie o godz 6:00 PM
{% endhint %}

```php
# app\Console\Commands\SendQuotesToApproveCommand.php
$schedule->command('send:quotes-to-approve')->dailyAt('18:00');
```

Wysyła do Prezesa informację na temat tego czy są jakieś oferty oczekują na akceptację.

## NotifyAboutEmployeesCommand

{% hint style="info" %}
Uruchamiane się raz dziennie o godz 04:21 AM
{% endhint %}

```php
# app\Console\Commands\NotifyAboutEmployeesCommand.php
$schedule->command('users:notify-about-employees')->dailyAt('04:21');
```

Na podstawie wpisów w rejestrze \[Pracownicy\] - tworzy lub dezaktywuje konta użytkowników w CoreA oraz powiadamia o tym, czy dani pracownicy mają założone konta w Redmine.

## SendNotificationAboutUnsentRodoCommand

{% hint style="info" %}
Uruchamia się raz w tygodniu w poniedziałki o 04:21 AM
{% endhint %}

```php
# app\Console\Commands\SendNotificationAboutUnsentRodoCommand.php
$schedule->command('send:unsent-rodo')->weeklyOn(1, '04:21');
```

Wysyła informację do odnośnie adresów email, wobec których nie została zrealizowany obowiązek informacyjny UODO.

## SendInfoAboutNextTrainings

{% hint style="info" %}
Uruchamiane pierwszego dnia każdego miesiąca o godz. 04:10 AM
{% endhint %}

```php
# app\Console\Commands\SendInfoAboutNextTrainings.php
$schedule->command('send:training-notification')->monthlyOn('1', '04:10');
```

Przypomnienie o szkoleniach BHP

## SendDailyTrainingNotification

{% hint style="info" %}
Uruchamiane codziennie o godz. 04:11 AM
{% endhint %}

Przypomnienie o szkoleniach BHP

```php
# app\Console\Commands\SendDailyTrainingNotification.php
$schedule->command('send:training-reminder')->dailyAt('04:11');
```

## SendInfoAboutNextTrainings

{% hint style="info" %}
Uruchamiane każdego 16 dnia miesiąca o godz 4:10 AM
{% endhint %}

```php
# app\Console\Commands\SendInfoAboutNextTrainings.php
$schedule->command('send:training-notification')->monthlyOn('16', '04:10');
```

Przypomnienie o szkoleniach BHP

## SendWeeklyBirthdaysReport

{% hint style="info" %}
Wysyłane raz w tygodniu w piątek o godz. 04:08 AM
{% endhint %}

```php
# app\Console\Commands\SendWeeklyBirthdaysReport.php
$schedule->command('send:birthdays-weekly')->weekly()->fridays()->at('04:08');
```

Przypomnienie o urodzinach w kolejnym tygodniu

## SendWeeklyActivitiesReportJob

{% hint style="info" %}
Wysyłane raz w tygodniu w poniedziałki o 04:09 AM
{% endhint %}

```php
# app\Jobs\SendWeeklyActivitiesReportJob.php
$schedule->command('send:weekly-activities-report')->weekly()->mondays()->at('04:09');
```

Informacja na temat aktywności handlowców  w poprzednim tygodniu

## SendQuestionnaireNotificationsCommand

{% hint style="info" %}
Wysyłane raz dziennie o 04:14 AM
{% endhint %}

```php
# app\Console\Commands\SendQuestionnaireNotificationsCommand.php
$schedule->command('send:questionnaire-notifications')->dailyAt('04:14'); 
```

Informacja na temat ankiet dotyczących badania satysfakcji klienta.

## SendNotificationAboutMultipleRelatedEmailsCommand

{% hint style="info" %}
Wysyłane każdego roboczego dnia o 07:00 AM oraz 01:00 PM.
{% endhint %}

```php
# app\Console\Commands\SendNotificationAboutMultipleRelatedEmailsCommand.php
$schedule->command('send:multiple-related-emails')->weekdays()->twiceDaily(7, 13);
```

Informacja na temat wielokrotnie przypisanych adresów email

## SendDataQualityReportCommand

{% hint style="info" %}
Wysyłane  w piątki o godz 6:00 PM
{% endhint %}

```php
# app\Console\Commands\SendDataQualityReportCommand.php
$schedule->command('send:data-quality-report')->weeklyOn(5, '18:00');
```

Informacja na temat jakości danych w CRM

## SendDailyBirthdaysReport

{% hint style="info" %}
Wysyłane codziennie o 04:05 AM
{% endhint %}

```php
# app\Console\Commands\SendDailyBirthdaysReport.php
$schedule->command('send:birthdays-daily')->dailyAt('04:05');
```

Informacja na temat dzisiejszych urodzin

## SendDailyActivitiesReportCommand

{% hint style="info" %}
Wysyłane codziennie o godz 19:00
{% endhint %}

```php
# app\Console\Commands\SendDailyActivitiesReportCommand.php
$schedule->command('send:daily-activities')->dailyAt('19:00');
```

Informacja na temat aktywności handlowców z Rumunii.

