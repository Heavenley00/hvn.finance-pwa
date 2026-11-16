HEAVENLY FINANCE — PWA VERSION

Isi folder:
- index.html: aplikasi asli yang sudah ditambahkan dukungan PWA
- manifest.json: nama, ikon, warna, dan pengaturan instalasi
- service-worker.js: cache dasar agar aplikasi dapat dibuka kembali saat offline setelah aset pernah dimuat
- icons/: ikon aplikasi 192px dan 512px

CARA MENCOBA DI ANDROID
1. Upload seluruh isi folder ini ke hosting HTTPS (misalnya GitHub Pages atau Netlify). Jangan hanya upload index.html; semua file harus tetap dalam susunan foldernya.
2. Buka alamat website hasil hosting menggunakan Chrome di Android.
3. Tunggu halaman selesai dimuat saat internet aktif.
4. Buka menu Chrome (titik tiga), lalu pilih “Install app” atau “Tambahkan ke layar utama” jika tersedia.
5. Buka aplikasi dari ikon yang muncul di layar utama.
6. Untuk uji offline, buka aplikasi sekali saat online, lalu aktifkan mode pesawat dan coba buka lagi.

CATATAN PENTING
- PWA perlu dijalankan dari HTTPS (atau localhost untuk pengujian), bukan dengan membuka file HTML langsung dari File Manager.
- Aplikasi masih memakai React, Tailwind, HTM, dan Google Fonts dari CDN. Setelah pertama kali dimuat saat online, browser/service worker akan mencoba menyimpan aset GET yang berhasil ke cache. Jadi, kemampuan offline penuh belum dijamin pada pemakaian pertama.
- Data transaksi tetap disimpan di localStorage browser/perangkat. Data tidak otomatis tersinkron antarperangkat atau antarbrowser. Hapus data situs/browser dapat menghapus data aplikasi; buat backup secara berkala.
- Versi ini tidak mengubah fitur dan struktur data keuangan yang sudah ada.
