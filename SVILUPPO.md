# Ambiente di Sviluppo Laravel - Configurato ✅

## Software Installato
- **PHP**: 8.3.30
- **Composer**: 2.9.3
- **Node.js**: 25.4.0
- **npm**: 11.7.0
- **Xdebug**: Configurato per debugging

## Estensioni VS Code Installate
1. **Intelephense** - PHP IntelliSense avanzato
2. **PHP Debug** - Debug con Xdebug
3. **Laravel Extra Intellisense** - Autocompletamento Laravel
4. **Laravel Blade Snippets** - Snippets per Blade
5. **Laravel Artisan** - Comandi Artisan integrati

## Come Debuggare

### 1. Avviare il Server di Sviluppo
```bash
php artisan serve
```
Il server sarà disponibile su: http://localhost:8000

### 2. Avviare il Debugging
1. Apri il file PHP che vuoi debuggare
2. Imposta un breakpoint cliccando a sinistra del numero di riga
3. Premi `F5` oppure vai su Run > Start Debugging
4. Seleziona "Listen for Xdebug"
5. Apri il browser e naviga alla pagina che vuoi debuggare
6. Il debugger si fermerà ai breakpoint impostati

### 3. Configurazioni di Debug Disponibili
- **Listen for Xdebug**: Ascolta le richieste di debug (usa questa per il web)
- **Launch currently open script**: Debug del file PHP attualmente aperto
- **Launch Built-in web server**: Avvia server PHP integrato con debug

## Comandi Utili Laravel

### Artisan
```bash
php artisan list                    # Lista tutti i comandi
php artisan migrate                 # Esegui migrazioni database
php artisan db:seed                 # Popola il database
php artisan make:controller Nome    # Crea controller
php artisan make:model Nome         # Crea model
php artisan route:list              # Lista tutte le route
php artisan tinker                  # REPL interattivo
php artisan cache:clear             # Pulisci cache
php artisan config:clear            # Pulisci config cache
php artisan view:clear              # Pulisci view cache
```

### NPM
```bash
npm run dev                         # Compila assets in modalità sviluppo
npm run build                       # Compila assets per produzione
npm run watch                       # Watch mode per sviluppo
```

## Configurazione Database
Modifica il file `.env` con le tue credenziali database:
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nome_database
DB_USERNAME=username
DB_PASSWORD=password
```

Dopo aver configurato il database:
```bash
php artisan migrate
php artisan db:seed
```

## Shortcuts VS Code Utili
- `F5` - Avvia/Continua debugging
- `F10` - Step Over (prossima riga)
- `F11` - Step Into (entra nella funzione)
- `Shift+F11` - Step Out (esci dalla funzione)
- `Shift+F5` - Stop debugging
- `Cmd+Shift+P` - Command Palette
- `Cmd+P` - Cerca file

## Test
```bash
php artisan test                    # Esegui tutti i test
./vendor/bin/pest                   # Esegui Pest tests
./vendor/bin/phpunit                # Esegui PHPUnit tests
```

## Problemi Comuni

### Se Xdebug non funziona:
```bash
php -v  # Verifica che Xdebug sia caricato
```
Dovresti vedere "with Xdebug" nell'output.

### Se il server non si avvia:
```bash
php artisan config:clear
php artisan cache:clear
composer dump-autoload
```

### Ricompilare assets:
```bash
npm run dev
```

## Note Importanti
- PHP 8.3 è stato configurato come versione predefinita
- Il path è stato aggiunto a ~/.zshrc
- Xdebug è configurato sulla porta 9003
- I permessi delle directory storage e bootstrap/cache sono stati impostati

## Prossimi Passi
1. Configura il database nel file `.env`
2. Esegui le migrazioni: `php artisan migrate`
3. Avvia il server: `php artisan serve`
4. Inizia a sviluppare! 🚀
