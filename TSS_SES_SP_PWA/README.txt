TSS • SYIFA E'SHOP • SYIFA PRINTING ERP — PWA WRAPPER

TUJUAN
- Memberi installable PWA sebenar pada HTTPS static hosting.
- ERP sebenar masih berjalan melalui Google Apps Script Web App di dalam iframe.
- Tidak mengubah database 23 sheet atau logic transaksi.

WAJIB SEBELUM GUNA
1. Di Apps Script > Deploy > Manage deployments > Edit Web App.
2. Execute as: Me (pemilik/deployer).
3. Who has access: Anyone (anonymous jika pilihan itu dipaparkan).
4. Deploy versi baharu.
5. Pastikan URL /exec yang digunakan sama dengan URL dalam index.html.

HOSTING PWA
Muat naik SEMUA fail dalam folder ini ke static HTTPS hosting seperti Cloudflare Pages atau GitHub Pages.
Jangan buka index.html terus dari file:// kerana service worker/PWA install memerlukan HTTPS atau localhost.

FAIL
- index.html            PWA shell + iframe ERP
- manifest.webmanifest  manifest PWA
- sw.js                 service worker shell cache
- icon-192.png          ikon
- icon-512.png          ikon
- Index.html            versi ERP yang dibersihkan daripada duplicate printDocument

NOTA
PWA shell tidak menyimpan data ERP secara offline. Database dan transaksi kekal di Google Sheets melalui Apps Script.
