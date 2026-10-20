# TUGAS-PWEB0-LATIHAN BOOTSTRAP
5025251095_Alessandro Almaz Filemon

Link Website: https://5025251095-latihanbootstrap.netlify.app/

# Pendahuluan

Tugas ini bertujuan membangun website Kantin Pusat ITS yang menerapkan framework Bootstrap 3 untuk struktur dan komponen antarmuka, CSS kustom untuk penyesuaian tampilan, serta JavaScript untuk manipulasi DOM dan logika interaktif. Website terdiri dari dua halaman, yaitu halaman Home yang memuat slider promo (carousel), informasi jam buka, menu terfavorit minggu ini, dan daftar gerai, serta halaman Menu yang menampilkan seluruh menu kantin lengkap dengan filter kategori, kolom pencarian berdasarkan nama menu atau gerai, dan tampilan detail menu dalam bentuk modal.


# Struktur

• index.html sebagai halaman Home

• menu.html sebagai halaman Menu Kantin

• css/style.css sebagai pengatur penyesuaian tampilan di atas Bootstrap (warna, font Poppins, kartu menu, footer, dan responsivitas)

• js/main.js sebagai pengatur data menu, filter kategori, pencarian, serta tampilan detail menu

• Bootstrap 3.4.1 dan jQuery 1.12.4 dimuat melalui CDN jsDelivr



# HTML

Kedua halaman memiliki kerangka yang sama, yaitu elemen nav berisi navbar Bootstrap (navbar-default navbar-static-top) dengan tombol navbar-toggle sehingga menu menjadi collapse pada layar kecil, elemen main berisi konten utama halaman, dan elemen footer berisi deskripsi kantin, tautan halaman, lokasi, serta keterangan hak cipta.

Halaman Home berisi:

• Carousel Bootstrap berisi 3 slide promo (Paket Hemat Rp. 15.000, Es Teh Gratis, dan Dies Natalis ke-66) lengkap dengan indikator dan tombol kiri-kanan.

• Bagian pembuka dengan judul, deskripsi, tombol Lihat semua menu, dan panel Jam buka yang berisi tabel.

• Tiga kartu Menu Terfavorit Minggu Ini yang ditata dengan grid col-xs-12 col-sm-6 col-md-4.

• Panel Gerai di kantin yang memuat daftar gerai.

Halaman Menu berisi judul dan petunjuk penggunaan, empat tombol filter kategori (Semua, Makanan, Minuman, Snack), input pencarian (form-control), wadah kartu menu yang diisi otomatis oleh JavaScript, pesan Menu tidak ditemukan, serta modal Bootstrap untuk detail menu.

Cuplikan Kode HTML:

<img width="870" height="653" alt="image" src="https://github.com/user-attachments/assets/fd4060be-4fd8-4e94-9db4-9c736b9e577f" />


# JavaScript

Data menu disimpan dalam array objek bernama menuKantin di file main.js. Setiap objek memuat id, nama, kategori (makanan, minuman, atau snack), harga, gerai, dan deskripsi. Terdapat 14 menu yang terdiri dari 6 makanan, 4 minuman, dan 4 snack. Beberapa fungsi utama meliputi:

• tampilkanMenu(): Menyaring data berdasarkan kategori aktif dan kata kunci pencarian (nama menu atau gerai), lalu membangun kartu menu dan menyisipkannya ke wadah daftar-menu. Jika hasil kosong, pesan Menu tidak ditemukan ditampilkan.

• Filter Kategori: Klik pada tombol kategori mengubah kategori aktif, memindahkan kelas aktif ke tombol yang diklik, lalu memanggil tampilkanMenu().

• Pencarian: Event input pada kolom cari memfilter menu secara real-time tanpa memuat ulang halaman.

• bukaDetail(): Mengisi nama, gerai, kategori, deskripsi, dan harga ke dalam modal, lalu menampilkannya dengan fungsi modal milik Bootstrap. Tombol Lihat detail ditangani dengan event delegation pada wadah daftar menu.

• rupiah() dan namaKategori(): Fungsi bantu untuk memformat harga (misalnya Rp18.000) dan mengubah kode kategori menjadi teks.

Cuplikan Kode JavaScript:

<img width="854" height="682" alt="image" src="https://github.com/user-attachments/assets/af81be26-050e-40f3-af74-9f03ee05a834" />

# CSS

Bootstrap digunakan sebagai dasar tata letak dan komponen, sedangkan file style.css dirancang untuk menyesuaikan tampilan agar konsisten dan memiliki identitas visual sendiri:

• CSS Variables & Font: Mendefinisikan variabel warna global (--pink, --mist, --blue, --indigo, dan --soft) serta menggunakan font Poppins pada seluruh teks, termasuk tombol dan input.

• Navbar: Navbar bawaan Bootstrap disesuaikan dengan warna indigo dan penanda halaman aktif berwarna pink.

• Carousel: Slide menggunakan warna solid dan gradient halus tanpa gambar, dengan teks promo diletakkan di tengah memakai Flexbox.

• Kartu Menu: Kartu memiliki border, border-radius, dan bayangan bergeser. Header kartu memakai gradient berbeda per kategori (pink untuk makanan, biru untuk minuman, dan biru muda untuk snack).

• Tinggi Kartu Seragam: Wadah kartu memakai display: flex dengan flex-wrap sehingga seluruh kartu dalam satu baris memiliki lebar dan tinggi yang sama.

• Footer Menempel di Bawah: Body memakai Flexbox kolom dengan min-height 100%, dan konten utama diberi flex: 1 0 auto sehingga footer selalu berada di dasar halaman meskipun konten sedikit.

• Responsive: Menggunakan media query max-width: 767px untuk memperkecil judul dan tinggi carousel pada layar kecil, serta prefers-reduced-motion untuk mematikan animasi bagi pengguna yang memintanya.

Cuplikan Kode CSS:

<img width="734" height="655" alt="image" src="https://github.com/user-attachments/assets/3f0f6444-a841-411e-b154-57ad59656b16" />

# Dokumentasi Tampilan

Laptop:
<img width="1276" height="698" alt="image" src="https://github.com/user-attachments/assets/0ac3d1a0-c343-4021-9d5d-b8198d74ddc9" />
<img width="1278" height="703" alt="image" src="https://github.com/user-attachments/assets/82e61881-b573-4027-b26a-9f73b61000b9" />
<img width="1252" height="691" alt="image" src="https://github.com/user-attachments/assets/7730f0af-cf37-4016-821d-c9e4fee97adb" />

HP:
<img width="796" height="1600" alt="image" src="https://github.com/user-attachments/assets/5aad01f4-cda0-4862-827a-485ec81125c2" />
<img width="792" height="1600" alt="image" src="https://github.com/user-attachments/assets/3adef200-6e49-4dc1-8cbc-5a5805c62caa" />

# Kesimpulan

Website Kantin Pusat ITS ini berhasil dibangun dengan memanfaatkan Bootstrap. Grid, navbar, carousel, tabel, tombol, form, dan modal dari Bootstrap menyediakan struktur dan komponen yang responsif, CSS kustom memberikan identitas visual yang konsisten, dan JavaScript menghadirkan interaktivitas berupa filter kategori, pencarian real-time, serta tampilan detail menu. Data menu saat ini disimpan statis di dalam file JavaScript dan belum terhubung ke database.
