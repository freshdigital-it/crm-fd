# CLAUDE.md
## Architecture
- Laravel + Spatie Permission
- Logic utama ada di `app/Http/Controllers` dan `app/Services`
- View ada di `resources/views`

## Commands
- Test: `php artisan test`
- Lint: `./vendor/bin/pint`

## Coding Rules
- Gunakan Spatie syntax untuk permission check: `$user->can('permission_name')`.
- Jangan ubah core framework file, buat Service class baru.
