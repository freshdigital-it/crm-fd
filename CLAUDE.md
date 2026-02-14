# Fresh Digital CRM (crm-fd) - Claude Context

## Project Overview
- **Type:** CRM & Project Management System (Based on Worksuite v5.5.24)
- **Framework:** Laravel (PHP)
- **Auth/ACL:** `spatie/laravel-permission`

## Architecture & Important Paths
- **Controllers:** `app/Http/Controllers` (Logic utama)
- **Services:** `app/Services` (Logic Hierarki & Export wajib di sini)
- **Views:** `resources/views`

## Coding Standards & Guidelines
### 1. Permission & Security (CRITICAL)
- **Strict Export Control:** Wajib permission terpisah (misal: `export_leads`). Jangan gunakan `view` permission untuk export.
- **Syntax:** Gunakan `$user->can('permission_name')` atau `@can`.

### 2. General Laravel Rules
- **Thin Controllers:** Pindahkan logic kompleks ke Service classes.
- **Validation:** Gunakan FormRequest terpisah, jangan di controller.

## Common Tasks (Memory Hooks)
- Jika mengerjakan fitur **Export**, cek permission di Controller DAN sembunyikan tombol di Blade.
- Jika membuat tabel baru, ikuti standar naming convention Laravel.
