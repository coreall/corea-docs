# Updaters

## RefreshActivitiesCommand

{% hint style="info" %}
Uruchamiane w poniedziałek o godz 04:02 AM
{% endhint %}

```php
# app\Console\Commands\RefreshActivitiesCommand.php
$schedule->command('refresh:activities weekly')->weekly()->mondays()->at('04:02');
```

Odświeża raport z aktywności tygodniowej handlowców

## SnapshotDataQualityModulesCommand

{% hint style="info" %}
Uruchamiane co godzinę 
{% endhint %}

```php
# app\Console\Commands\SnapshotDataQualityModulesCommand.php
$schedule->command('snapshot:data-quality')->hourlyAt(59);
```

Odświeża wyniki z modułu Data Quality 

## CalculateClosedWonProbablitiesCommand

{% hint style="info" %}
Uruchamiane codziennie o godz 04:22 AM
{% endhint %}

```php
# app\Console\Commands\CalculateClosedWonProbablitiesCommand.php
$schedule->command('refresh:probabilities')->dailyAt('04:22');
```

Przelicza prawdopodobieństwo wygranej w module Leady

## CompareCoreaUsersWithRedmineCommand

{% hint style="info" %}
Uruchamiane codziennie o godz 04:18 AM
{% endhint %}

```php
# app\Console\Commands\HR\CompareCoreaUsersWithRedmineCommand.php
$schedule->command('users:compare-with-redmine')->dailyAt('04:18');
```

Porównuje rejestr pracowników w CoreA z rejestrem pracowników w Redmine.

## RefreshUoReportCommand

{% hint style="info" %}
Uruchamiane codziennie o godz 04:16 AM
{% endhint %}

```php
# app\Console\Commands\RefreshUoReportCommand.php
$schedule->command('report:refresh-uo')->dailyAt('04:16');
```

Odświeża dane do raportu z projektu Utrzymanie Obiektu w Redmine

