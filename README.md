# Monitoring Mesin CPCM MOI
PWA dashboard read-only untuk tab `Form Responses 1`.

## Deploy
1. Ekstrak ZIP dan upload isi folder ke repository GitHub.
2. Import repository di Vercel. Framework: Other; tanpa build command.
3. Deploy, lalu buka URL Vercel melalui Chrome Android.
4. Pilih menu browser **Install app** / **Add to Home screen**.

## Akses Google Sheet
Atur Share → General access → Anyone with the link → Viewer. Dashboard hanya membaca data (GET), tidak memiliki fungsi mengubah/menghapus sheet.

## Kolom yang dikenali
Tanggal: Timestamp/Tanggal/Date/Waktu. Teknisi: NAMA TEKNISI/Teknisi/Technician. Mesin: NAMA MESIN/Mesin/Machine. Sesuaikan fungsi `col()` di index.html jika judul kolom berbeda.

Jumlah mesin dihitung berdasarkan nama mesin unik, bukan jumlah baris laporan. Bulan berjalan menggunakan tanggal 1 sampai hari terakhir bulan menurut waktu perangkat. Pembacaan spreadsheet memerlukan internet; shell PWA dapat terbuka dari cache saat offline.
