1. Penjelasan Project
Pada project ini, dikembangkan sebuah aplikasi mobile berbasis Flutter yang berfungsi untuk menampilkan data resep makanan menggunakan API sebagai sumber data utama.
Aplikasi ini memungkinkan pengguna untuk melihat daftar resep, mencari resep berdasarkan nama, serta melihat detail resep secara lengkap.
Informasi yang ditampilkan dalam aplikasi meliputi gambar makanan, nama resep, dan informasi tambahan lainnya. Selain itu, pengguna juga dapat membuka halaman detail untuk melihat informasi resep secara lebih lengkap.
Pengembangan aplikasi ini berfokus pada:
• penggunaan arsitektur modular,
• pemisahan antara logic dan tampilan,
• serta pembuatan UI yang sederhana dan responsif.
________________________________________
2. Implementasi CPMK 1 – Data-Driven Architecture & Planning
2.1 Modular Folder Structure
Struktur project disusun secara modular untuk meningkatkan keterbacaan dan kemudahan pengembangan. Pembagian folder yang digunakan adalah sebagai berikut:
• core/constants/
Berisi konstanta seperti endpoint API.
• core/utils/
Berisi helper seperti cache (penyimpanan data lokal).
• models/
Berisi model data resep.
• services/
Menangani pengambilan data dari API dan caching.
• providers/
Mengatur state management menggunakan Provider.
• views/
Berisi halaman utama seperti Home dan Detail.
• widgets/
Berisi komponen UI yang dapat digunakan ulang.
Pendekatan ini membuat kode lebih terstruktur, mudah dikembangkan, dan scalable.
________________________________________
2.2 Offline Readiness (Caching)
Aplikasi dirancang untuk tetap dapat digunakan saat tidak ada koneksi internet dengan memanfaatkan caching.
Data yang sudah diambil dari API akan disimpan sementara. Ketika perangkat offline, aplikasi akan menampilkan data terakhir yang tersimpan.
Selain itu, aplikasi juga menampilkan indikator bahwa pengguna sedang dalam kondisi offline.
________________________________________
2.3 Error Handling
Aplikasi dilengkapi dengan mekanisme error handling untuk menangani kondisi seperti:
• kegagalan pengambilan data dari API,
• koneksi internet tidak tersedia,
• data tidak ditemukan.
Aplikasi menampilkan pesan yang lebih user-friendly agar pengguna tetap nyaman saat menggunakan aplikasi.
________________________________________
3. Implementasi CPMK 2 – Responsive Features & Code Consistency
3.1 Asynchronous Data Fetching
Pengambilan data dari API dilakukan secara asynchronous menggunakan async/await.
Dengan pendekatan ini, proses pengambilan data tidak menghambat tampilan UI sehingga aplikasi tetap responsif.
________________________________________
3.2 Search Feature
Aplikasi menyediakan fitur pencarian resep berdasarkan nama.
Pengguna dapat langsung mengetik pada search bar, dan data akan difilter secara real-time.
________________________________________
3.3 Reusable Widgets (Consistency & Creativity)
Untuk menjaga konsistensi UI dan efisiensi kode, aplikasi menggunakan reusable widget, antara lain:
• RecipeCard → menampilkan informasi resep
• SearchBarWidget → input pencarian
• LoadingWidget → indikator loading
• ErrorWidgetCustom / ErrorStateWidget → tampilan error
Penggunaan reusable widget membuat kode lebih modular dan mudah dikelola.
________________________________________
3.4 Loading State
Aplikasi menampilkan loading indicator saat data sedang diambil dari API.
Hal ini memberikan feedback kepada pengguna bahwa aplikasi sedang memproses data.
________________________________________
3.5 Responsive UI dan Visual Consistency
Tampilan aplikasi dibuat sederhana dan rapi dengan ciri:
• penggunaan warna yang konsisten,
• tampilan list yang terstruktur,
• serta UI yang mudah digunakan.
Aplikasi tetap nyaman digunakan pada berbagai ukuran layar.
________________________________________
4. Kesimpulan
Aplikasi Cookie App berhasil dikembangkan dengan memanfaatkan API sebagai sumber data.
Fitur utama seperti pencarian, tampilan list, dan detail resep telah diimplementasikan dengan baik.
Selain itu, aplikasi juga sudah mendukung:
• offline mode (cache),
• error handling,
• loading state,
