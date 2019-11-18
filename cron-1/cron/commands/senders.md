# Senders

## SendDailyNotifications

```php
# app\Console\Commands\SendDailyNotifications.php
$schedule->command('send:daily')->dailyAt('04:01');
```

{% hint style="info" %}
Uruchamia się codziennie o godzinie 04:01 AM
{% endhint %}

### SendReminderAboutUpcomingPayments

Przypomnienie o nadchodzących planowanych płatnościach

### ReminderAboutBillingRequestJob

Przypomnienie o zleceniu fakturowania

## SendReportAboutExpiredQuotesToCeoCommand

```php
# app\Console\Commands\Mails\SendReportAboutExpiredQuotesToCeoCommand.php
$schedule->command('send:opportunities-expiration')->weeklyOn(1, '04:13');
```

{% hint style="info" %}
Uruchamia się raz w tygodniu o godz. 04:13 AM
{% endhint %}

Wysyła informację na temat kończących się oraz przeterminowanych ofert do Pana Prezesa oraz przypisanych handlowców

## SendQuotesToApproveCommand

```php
# app\Console\Commands\SendQuotesToApproveCommand.php
$schedule->command('send:quotes-to-approve')->dailyAt('18:00');
```

{% hint style="info" %}
Uruchamia się raz dziennie o godz 6:00 PM
{% endhint %}

Wysyła do Prezesa informację na temat tego czy są jakieś oferty oczekują na akceptację.

## NotifyAboutEmployeesCommand

```php
# app\Console\Commands\NotifyAboutEmployeesCommand.php
$schedule->command('users:notify-about-employees')->dailyAt('04:21');
```

{% hint style="info" %}
Uruchamiane się raz dziennie o godz 04:21 AM
{% endhint %}

Na podstawie wpisów w rejestrze \[Pracownicy\] - tworzy lub dezaktywuje konta użytkowników w CoreA oraz powiadamia o tym, czy dani pracownicy mają założone konta w Redmine.

```php
# app\Console\Commands\NotifyAboutEmployeesCommand.php
$schedule->command('users:notify-about-employees')->dailyAt('04:21');

# app\Console\Commands\SendNotificationAboutUnsentRodoCommand.php
$schedule->command('send:unsent-rodo')->weeklyOn(1, '04:21');

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



