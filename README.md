# CRON

### Kernel

Automatyczne akcje zapisane są w klasie  **app\Console\Kernel.php** w metodzie schedule\(\). Każda z linii wywołujących komendę odpowiada wpisowi do CRONA. Komentarz przy każdej komendzie wskazuje na klasę, która zostaje uruchomiona w danej akcji.

```php
# app\Console\Commands\CleanerForEveryFiveMinutes.php
$schedule->command('cleaners')->everyFiveMinutes();
```

Każdy wpis zawiera również informację na temat tego, w jakich interwałach jest uruchamiana dana akcja.

### Commands

C:\Users\piotr.skrobol\Projects\corea\app\Console\Commands\SendQuotesToApproveCommand.php



