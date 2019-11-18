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



```php
# app\Console\Commands\SendInfoAboutNextTrainings.php
$schedule->command('send:training-notification')->monthlyOn('1', '04:10');

# app\Console\Commands\SendDailyTrainingNotification.php
$schedule->command('send:training-reminder')->dailyAt('04:11');

# app\Console\Commands\SendInfoAboutNextTrainings.php
$schedule->command('send:training-notification')->monthlyOn('16', '04:10');

# app\Console\Commands\SendWeeklyBirthdaysReport.php
$schedule->command('send:birthdays-weekly')->weekly()->fridays()->at('04:08');

# app\Jobs\SendWeeklyActivitiesReportJob.php
$schedule->command('send:weekly-activities-report')->weekly()->mondays()->at('04:09');

# app\Console\Commands\SendQuestionnaireNotificationsCommand.php
$schedule->command('send:questionnaire-notifications')->dailyAt('04:14'); #needs 2 minutes

# app\Console\Commands\SendNotificationAboutMultipleRelatedEmailsCommand.php
$schedule->command('send:multiple-related-emails')->weekdays()->twiceDaily(7, 13);

# app\Console\Commands\SendDataQualityReportCommand.php
$schedule->command('send:data-quality-report')->weeklyOn(5, '18:00');

# app\Console\Commands\SendDailyBirthdaysReport.php
$schedule->command('send:birthdays-daily')->dailyAt('04:05');

# app\Console\Commands\SendDailyActivitiesReportCommand.php
$schedule->command('send:daily-activities')->dailyAt('19:00');
```



