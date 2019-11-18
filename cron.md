# CRON

### Kernel

Automatyczne akcje zapisane są w klasie  **app\Console\Kernel.php** w metodzie schedule\(\). Każda z linii wywołujących komendę odpowiada wpisowi do CRONA. Komentarz przy każdej komendzie wskazuje na klasę, która zostaje uruchomiona w danej akcji.

```php
/**
 * CLEANERS
 */
# app\Console\Commands\CleanerForEveryFiveMinutes.php
$schedule->command('cleaners')->everyFiveMinutes();

# app\Console\Commands\CleanerForEveryHour.php
$schedule->command('cleaners:hourly')->hourly();

# app\Console\Commands\CleanerForEveryDay.php
$schedule->command('cleaners:daily')->dailyAt('03:03');

# app\Console\Commands\CleanerForEveryWeek.php
$schedule->command('cleaners:weekly')->weeklyOn(1, '03:10');

/**
 * UPDATERS
 */
# app\Console\Commands\RefreshActivitiesCommand.php
$schedule->command('refresh:activities weekly')->weekly()->mondays()->at('04:02');

# app\Console\Commands\RefreshActivitiesCommand.php
$schedule->command('refresh:activities monthly')->monthlyOn(1, '04:06');

# app\Console\Commands\SnapshotDataQualityModulesCommand.php
$schedule->command('snapshot:data-quality')->hourlyAt(59);

# app\Console\Commands\CalculateClosedWonProbablitiesCommand.php
$schedule->command('refresh:probabilities')->dailyAt('04:22');

# app\Console\Commands\HR\CompareCoreaUsersWithRedmineCommand.php
$schedule->command('users:compare-with-redmine')->dailyAt('04:18');

# app\Console\Commands\RefreshUoReportCommand.php
$schedule->command('report:refresh-uo')->dailyAt('04:16');

/**
 * SENDERS
 */
# app\Console\Commands\SendDailyNotifications.php
$schedule->command('send:daily')->dailyAt('04:01');

# app\Console\Commands\Mails\SendReportAboutExpiredQuotesToCeoCommand.php
$schedule->command('send:opportunities-expiration')->weeklyOn(1, '04:13');

# app\Console\Commands\SendQuotesToApproveCommand.php
$schedule->command('send:quotes-to-approve')->dailyAt('18:00');

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

Każdy wpis zawiera również informację na temat tego, w jakich interwałach jest uruchamiana dana akcja. Określone jest to za pomocą metod, wywołanych po metodzie command\(\).

### 



