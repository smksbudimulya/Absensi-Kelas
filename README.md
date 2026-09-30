# Absensi SMKS Budi Mulya — GitHub + Google Sheets

## Struktur
- `index.html` — frontend GitHub Pages
- `config.js` — URL backend Apps Script
- `code.gs` — backend/database Google Apps Script

## Instalasi backend
1. Buat Google Spreadsheet.
2. Buka **Extensions → Apps Script**.
3. Tempel `code.gs`.
4. Jalankan `setupDatabase()` sekali.
5. **Deploy → New deployment → Web app**.
6. Execute as: **Me**.
7. Who has access: **Anyone**.
8. Salin URL `/exec`.

## Instalasi frontend
Buka `config.js`, lalu ganti:
`TEMPEL_URL_WEB_APP_APPS_SCRIPT_DI_SINI`
dengan URL `/exec` hasil deployment.

Upload `index.html` dan `config.js` ke repository GitHub. Aktifkan GitHub Pages.

## Login awal
- Username: `admin`
- Password: `admin2026`

Segera ubah password admin melalui menu **User & Pengaturan**.

## Fitur
- Login berbasis role
- Dashboard statistik + grafik
- Input absensi harian
- Date picker untuk tanggal
- Rekap matriks bulanan
- Cetak A4 landscape
- Kirim ringkasan WhatsApp
- CRUD siswa
- Import Excel
- Template Excel
- CRUD user
- Role Admin / Wali / Sekretaris
- Pengaturan Kepala Sekolah
- Backup JSON
- Reset log absensi semester
- Semua perubahan utama tersimpan di Spreadsheet

## Catatan keamanan
GitHub Pages tidak menyimpan password/database. Password disimpan sebagai SHA-256 di Spreadsheet. URL Web App Apps Script adalah endpoint publik, jadi hak akses aplikasi tetap dikendalikan oleh login dan validasi backend.
