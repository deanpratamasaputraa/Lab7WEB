### Mata Kuliah: Pemograman Web 2
### Nama: Dean Pratama Saputra
### Nim: 312210114
### Kelas: I241B
### Dosen Pengampu: Agung Nugroho, S.Kom., M.Kom., S.Kom., M. Kom
---
## Langkah - Langkah Praktikum

### Praktikum 1: PHP Framework (Codeigniter)
### mengaktifkan ekstentsi XAMPP Control Panel
Untuk mengaktifkan ekstentsi tersebut, melalu XAMPP Control Panel, pada bagian Apache
klik Config -> PHP.ini

<img width="1078" height="882" alt="image" src="https://github.com/user-attachments/assets/78a12de1-201b-4c91-b0bc-6a24239cee20" />

### Ekstensi PHP

<img width="365" height="422" alt="image" src="https://github.com/user-attachments/assets/511225de-572d-4a6a-be70-0233a56c4247" />

### Instalasi Codeigniter 4
Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual
dan menggunakan composer. Pada praktikum ini kita menggunakan cara manual.
• Unduh Codeigniter dari website https://codeigniter.com/download
• Extrak file zip Codeigniter ke direktori htdocs/lab11_ci.
• Ubah nama direktory framework-4.x.xx menjadi ci4.
• Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/

<img width="1228" height="747" alt="image" src="https://github.com/user-attachments/assets/0fa9a062-681d-49a9-aeca-223c01a3beb2" />

### Menjalankan CLI (Command Line Interface)
Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses
CLI buka terminal/command prompt.

<img width="985" height="244" alt="image" src="https://github.com/user-attachments/assets/944e3a86-7605-41c4-ad20-a08810f9bb94" />

### Tampilan Command Prompt
Arahkan lokasi direktori sesuai dengan direktori kerja project dibuat
(xampp/htdocs/lab11_ci/ci4/)
Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah:
php spark

<img width="1154" height="731" alt="image" src="https://github.com/user-attachments/assets/50d9416f-9525-4f58-9282-6c2b7fcaf638" />

### Mengaktifkan Mode Debugging
Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis errornya,
maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment
variable CI_ENVIRINMENT menjadi development.

<img width="923" height="141" alt="image" src="https://github.com/user-attachments/assets/43a4935f-c41b-4017-b332-1ac054a96330" />

Untuk mencoba error tersebut, ubah kode pada file app/Controller/Home.php hilangkan titik koma pada akhir kode

<img width="1852" height="810" alt="image" src="https://github.com/user-attachments/assets/77d1e415-2443-4da3-b967-bfa538d6916c" />

### Routing dan Controller
tambahkan route baru pada file app/config/Routes.php

<img width="791" height="435" alt="image" src="https://github.com/user-attachments/assets/14117bc4-e2a7-4781-99b5-c8ba8a013ef9" />

Untuk mengetahui route yang ditambahkan sudah benar, buka CLI dan jalankan perintah php spark routes.

<img width="1329" height="544" alt="image" src="https://github.com/user-attachments/assets/527cd562-406a-44a0-ae7a-a71b3e0866aa" />

Selanjutnya adalah membuat Controller Page. Buat file baru dengan nama page.php pada
direktori Controller kemudian isi kodenya seperti berikut

<img width="683" height="595" alt="image" src="https://github.com/user-attachments/assets/b9aa9f81-602a-458c-8059-59f9692b5689" />

kemudian buka browser untuk membuka hasilnya

<img width="579" height="124" alt="image" src="https://github.com/user-attachments/assets/44cb356e-1cca-4245-b8cd-90ed17890950" />

### Membuat View
Selanjutnya adalam membuat view untuk tampilan web agar lebih menarik. Buat file baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi kodenya seperti berikut.

<img width="543" height="395" alt="image" src="https://github.com/user-attachments/assets/6640f5b0-42b4-4f1b-a3bc-aa2cba835610" />

Ubah method about pada class Controller Page menjadi seperti berikut:

<img width="1098" height="329" alt="image" src="https://github.com/user-attachments/assets/7573670d-5fdc-43cb-839b-e8307b1caa69" />

Buka browser untuk melihat hasilnya.

<img width="742" height="695" alt="image" src="https://github.com/user-attachments/assets/6aaf80b3-2ecd-41bd-87d5-b9b95a01f9d8" />

### Membuat Layout Web
Buat file app/view/template/header.php

<img width="878" height="608" alt="image" src="https://github.com/user-attachments/assets/b09e643f-f6e5-4490-a6a4-c4357f2e63de" />

Kemudian buat file app/view/template/footer.php

<img width="1390" height="709" alt="image" src="https://github.com/user-attachments/assets/83c545d2-68dc-4e88-8629-cacb06893d91" />

Kemudian buka browser untuk melihat hasilnya.

<img width="1914" height="941" alt="image" src="https://github.com/user-attachments/assets/af11ffcf-0412-43dd-bf8d-5e8646055080" />

---

### Praktikum 2:

### Membuat Database dan Tabel
Langkah pertama adalah membuat database dengan nama lab_ci4 dan tabel artikel melalui phpMyAdmin.

<img width="1226" height="477" alt="image" src="https://github.com/user-attachments/assets/059ff1ae-f9d4-470d-969d-36432428c244" />

### Konfigurasi Database
Selanjutnya melakukan konfigurasi database untuk menghubungkan ke database server. Konfigurasi dilakukan pada file .env, konfigurasi juga bisa dilakukan pada file app/config/database.php.

<img width="795" height="281" alt="image" src="https://github.com/user-attachments/assets/58d52f28-d92b-484a-a58f-9af960cca2e7" />

### Membuat Model
Selanjutnya membuat model untuk memproses data artikel. Buat file baru dengan nama ArtikelModel.php pada direktory app/Models.

<img width="1226" height="507" alt="image" src="https://github.com/user-attachments/assets/74783128-6d78-451c-b76e-f1dc349da8ad" />

### Membuat Controller
Selanjutnya buat Controller baru dengan nama Artikel.php pada direktory app/Controllers.

<img width="1177" height="624" alt="image" src="https://github.com/user-attachments/assets/5b6953f0-5ae6-413a-8b4a-2b6ee601cc1d" />

### Membuat View
Selanjutnya buat direktory baru dengan nama artikel pada direktory app/view, lalu buat file baru dengan nama index.php.

<img width="1231" height="508" alt="image" src="https://github.com/user-attachments/assets/bc959273-2434-4b41-8627-8c7f8c982d7d" />

Kemudian menambahkan beberapa data pada database.

<img width="1256" height="194" alt="image" src="https://github.com/user-attachments/assets/89e54f9e-1700-40fd-9350-c99a5ab39c44" />

Lalu ubah jalur route pada routes.php menjadi $routes->get('/artikel', 'Artikel::index');.

<img width="1228" height="446" alt="image" src="https://github.com/user-attachments/assets/e85e856d-4fe4-4b51-aa7d-af631000d78e" />

Kemudian buka browser dan lihat hasilnya.

<img width="1253" height="550" alt="image" src="https://github.com/user-attachments/assets/4cf23733-04b2-42a3-a4c8-253b22839c9f" />

### Membuat Tampilan Detail Artikel
Selanjutnya, agar saat judul artikel di klik maka akan diarahkan ke halaman yang berbeda. Untuk membuatnya tambahkan fungsi baru pada file Controller/Artikel.php.

<img width="1191" height="738" alt="image" src="https://github.com/user-attachments/assets/2657ed0c-2657-4a87-aa91-5b41518a88b0" />

Kemudian buat view baru di direktory app/View/artikel dengan nama file detail.php.

<img width="1231" height="294" alt="image" src="https://github.com/user-attachments/assets/ff29f928-1846-4075-8f0d-d319a9363c00" />

Kemudian tambahkan routing baru di direktory app/Config/Routes.php

<img width="1229" height="460" alt="image" src="https://github.com/user-attachments/assets/71f9fe45-8300-485e-9d52-9eb2f987d632" />

Lalu klik pada judul artikel maka akan di arahkan he halaman yang berbeda.

<img width="1223" height="554" alt="image" src="https://github.com/user-attachments/assets/f0984a6f-ed1d-48dd-a6e3-74e9bd8ab923" />

### Membuat Menu Admin
Selanjutnya membuat menu admin untuk melakukan proses CRUD pada artikel. Buat fungsi baru pada file Artikel.php

<img width="1221" height="754" alt="image" src="https://github.com/user-attachments/assets/75176f30-fbd4-4b3f-a4b9-76e0b6a878ea" />

Kemudian buat view baru untuk menampilkan tampilan admin dengan nama file admin_index.php pada direktory app/View/artikel

<img width="1228" height="571" alt="image" src="https://github.com/user-attachments/assets/9d3526d8-19d2-440e-a85c-0ef4eed52097" />

<img width="614" height="106" alt="image" src="https://github.com/user-attachments/assets/2b75081c-f065-44c8-9194-d11bb1af9bff" />

Kemudian buat file admin_header.php pada direktory app/View/template/.

<img width="1240" height="672" alt="image" src="https://github.com/user-attachments/assets/4de66484-ca02-40e0-9e8b-0f1ef471cc51" />

Kemudian buat file admin_footer.php pada direktory app/View/template/.

<img width="1230" height="473" alt="image" src="https://github.com/user-attachments/assets/5bae9dc4-46c7-43ae-8cf3-135278622304" />

Kemudian tambahkan routing baru pada file routes.php untuk menu admin.

<img width="1228" height="669" alt="image" src="https://github.com/user-attachments/assets/0511e4ff-e80f-4352-bf12-1b4ad56b552f" />

Kemudian buka browser untuk melihat hasilnya.

<img width="1220" height="549" alt="image" src="https://github.com/user-attachments/assets/c0824711-a819-4601-be78-cdda70e51992" />

### Menambah Data Artikel
Selanjutnya menambahkan fungsi baru pada direktory app/Controllers/Artikel.php untuk menambahkan artikel baru.

<img width="1200" height="754" alt="image" src="https://github.com/user-attachments/assets/8ad3838b-49a7-43e8-9296-07d7aadd32f6" />

Kemudian buat view baru untuk form tambah artikel dengan nama file from_add.php.

<img width="1147" height="422" alt="image" src="https://github.com/user-attachments/assets/1cad11b2-1424-4887-898b-66406ab93be5" />

Kemudian buka browser untuk melihat hasilnya.

<img width="1231" height="549" alt="image" src="https://github.com/user-attachments/assets/56c29e0a-b68d-4852-bd73-c4e49304c7e7" />

### Mengubah Data
Selanjutnya menambahkan fungsi baru pada direktory app/Controllers/Artikel dengan nama edit().

<img width="1149" height="744" alt="image" src="https://github.com/user-attachments/assets/affc0d77-e003-4984-a9ca-f8aa6739e1cc" />

Kemudian buat view baru untuk form edit artikel dengan nama file from_edit.php

<img width="1229" height="340" alt="image" src="https://github.com/user-attachments/assets/8fab8fc9-707c-4623-b2cf-a1e1728dfe49" />

Kemudian buka browser untuk melihat hasilnya.

<img width="1207" height="542" alt="image" src="https://github.com/user-attachments/assets/4a91e65d-2f1f-4c1a-b3bf-1a9325462789" />

### Menghapus Data
Selanjutnya menambahkan fungsi baru untuk menghapus data pada direktory app/Controllers/Artikel.php dengan nama fungsi delet().

<img width="766" height="377" alt="image" src="https://github.com/user-attachments/assets/b85cca15-186c-4bbf-a98c-3771b07eb1ce" />

Kemudian buka browser untuk melakukan hapus artikel.

- Before


<img width="1212" height="558" alt="image" src="https://github.com/user-attachments/assets/b3c41145-cdde-4112-8598-df438acc5f9f" />

- After


<img width="1221" height="552" alt="image" src="https://github.com/user-attachments/assets/a8fd1d1f-5890-4f6d-8e33-4f6628d000d9" />

---

### PRAKTIKUM 3: VIEW LAYOUT & VIEW CELL
### Update Database
Update database terlebih dahulu di phpMyAdmin pada database lab_ci4.

<img width="944" height="230" alt="image" src="https://github.com/user-attachments/assets/297719f8-afe2-45d1-8453-fdcdae97440e" />

Kemudian buat direktory Models pada direktory app/ lalu buat file baru dengan nama ArtikelModel.php di dalam direktory app/Models/.

<img width="1219" height="502" alt="image" src="https://github.com/user-attachments/assets/be9db95e-d8ba-48f6-863b-fe85dfad937f" />

### Buat Layout Utama
Buat folder baru dengan nama layout pada direktory app/Views/ kemudian buat file baru dengan nama main.php pada direktory app/Views/layout/.

<img width="1234" height="431" alt="image" src="https://github.com/user-attachments/assets/a8cb577a-4951-482e-8c71-db9c4e200cd6" />

<img width="1227" height="422" alt="image" src="https://github.com/user-attachments/assets/6ebb53f9-a379-449f-a9d4-0e69c4810490" />

### Buat Sidebar (View Cell)
Buat folder Cells pada direktory app/ kemudian buat file ArtikelTerkini.php pada direktory app/Cells/.

<img width="1229" height="469" alt="image" src="https://github.com/user-attachments/assets/58efaa60-0bf9-4006-a53c-c8eb5e6f8569" />

Kemudian buat folder baru Components pada direktory app/Views lalu buat file dengan nama artikel_terkini.php.

<img width="1164" height="484" alt="image" src="https://github.com/user-attachments/assets/075f2e8d-c073-47ba-b74e-6511014c3dae" />

### Membuat Halaman Daftar Artikel
Buat file baru pada direktory app/Views/artikel dengan nama file index.php.

<img width="1228" height="687" alt="image" src="https://github.com/user-attachments/assets/3031355e-adc8-47f6-8b48-591a2aa44318" />

Kemudian lakukan update pada file home.php, artikel.php, about.php, dan contact.php.

<img width="685" height="420" alt="image" src="https://github.com/user-attachments/assets/c4b9323d-5aec-410e-8059-93a72d52ba08" />

<img width="648" height="433" alt="image" src="https://github.com/user-attachments/assets/8936813c-cab1-4c98-9227-9e6a9c812a1e" />

<img width="673" height="430" alt="image" src="https://github.com/user-attachments/assets/cc8fd3ff-447d-431e-8e9b-e84e3d10c51b" />

<img width="629" height="407" alt="image" src="https://github.com/user-attachments/assets/e2880ce9-6564-45cb-b3d3-773555ebda68" />

Kemudian buka browser untuk melihat hasilnya.

- Halaman Home

<img width="1046" height="538" alt="image" src="https://github.com/user-attachments/assets/ff43d8da-f6fc-4d93-a2b4-b66423294fbc" />

- Halaman Artikel

<img width="1022" height="546" alt="image" src="https://github.com/user-attachments/assets/5f36ae07-edc4-4c7f-9314-e7b113043bfb" />

- Halaman About

<img width="1013" height="559" alt="image" src="https://github.com/user-attachments/assets/c74d07f3-1e72-4e35-abba-04ea600920c6" />

- Halaman Kontak

<img width="955" height="549" alt="image" src="https://github.com/user-attachments/assets/db491173-df13-4a56-a386-4855ad2e4cd9" />

### Jawaban Pertanyaan Tugas
Manfaat utama dari penggunaan View Layout

- Efisiensi Kode (Reusability): Kita tidak perlu menulis ulang struktur HTML (Header, Navigasi, Footer) di setiap file View.
- Kemudahan Maintenance: Jika ada perubahan pada tampilan menu atau footer, kita cukup mengubah satu file saja (layout/main.php), maka seluruh halaman akan otomatis terupdate.
- Konsistensi Tampilan: Memastikan seluruh halaman website memiliki desain dan struktur yang seragam.

### Perbedaan View cell dengan View biasa

- View Biasa: Digunakan untuk menampilkan konten utama satu halaman penuh (misal: halaman About atau Daftar Artikel) dan biasanya dipanggil langsung oleh Controller.
- View Cell: Digunakan untuk menampilkan komponen UI kecil yang bersifat modular (seperti widget sidebar atau menu navigasi).
- Kemandirian Data: View Cell bisa mengambil datanya sendiri (melalui class Cell) tanpa harus dikirimkan data secara manual dari Controller utama, sehingga lebih praktis digunakan berulang kali di halaman mana saja.

  ---

  ### Praktikum 4

  ### Membuat Tabel User
  Lakukan pembuatan tabel melalui phpMyAdmin pada database lab_ci4. Tabel ini berfungsi untuk mennyimpan informasi login admin.

  <img width="724" height="355" alt="image" src="https://github.com/user-attachments/assets/150fe4ee-ce20-4c8c-9ef8-98a8ef5c494e" />

  ### Membuat Model User
Model user dibuat untuk menciptakan objek yang bertugas mengelola data pada tabel users. Tanpa model, controller tidak akan bisa mengecek apakah username, email, dan password ada di database atau tidak.

Buat file baru di direktory app/Models/ dengan nama file UserModel.php.

<img width="1201" height="505" alt="image" src="https://github.com/user-attachments/assets/9af301d9-52a5-45b3-81e1-89be92cd8b9f" />

### Membuat Seeder
Seeder berfungsi untuk memasukkan data pengguna awal ke dalam tabel users secara otomatis tanpa harus mengisi manual lewat phpMyAdmin. Dengan menggunakan seeder, password admin ("admin123") akan diubah menjadi kode acak (hash) menggunakan fungsi password_hash agar tersimpan secara aman di database.

Buka terminal/CLI dan jalankan perintah php spark make:seeder UserSeeder untuk membuat seeder baru.

<img width="1135" height="242" alt="image" src="https://github.com/user-attachments/assets/53f89c9c-3c6b-4382-9c00-9723a9e1d1e3" />
Kemudian buka direktory app/Database/Seeds/UserSeeder.php lalu isi kode berikut.

<img width="1220" height="694" alt="image" src="https://github.com/user-attachments/assets/aa7978a1-14b9-4a20-9022-aac6f82a263c" />
Kemudian buka terminal dan jalankan perintah php spark db:seed UserSeeder.

<img width="1119" height="209" alt="image" src="https://github.com/user-attachments/assets/49db27e7-fa72-4de1-989a-ff641e3ed583" />
Kemudian cek kembali tabel users pada phpMyAdmin untuk melihat apakah database berhasil di eksekusi atau tidak.

<img width="1207" height="183" alt="image" src="https://github.com/user-attachments/assets/fa7597b6-3729-4ead-9872-09732e7a7135" />
Data berhasil di eksekusi dan password berhasil di has.

### Membuat Controller User
Controller ini berfungsi sebagai pengatur alur masuk dan keluar pengguna. Saat user menginput data, Controller akan meminta UserModel untuk mencari email tersebut di database. Jika ditemukan, password akan dicocokkan. Jika sesuai, data pengguna disimpan ke dalam session agar sistem mengenali bahwa user tersebut sudah login. Jika salah, user akan dikembalikan ke halaman login dengan pesan kesalahan.

Buat file baru dengan nama User.php di dalam direktory app/Controllers/.

<img width="1223" height="540" alt="image" src="https://github.com/user-attachments/assets/9bcb0d17-7f6e-4e88-805c-f9f7e105d026" />

<img width="1224" height="501" alt="image" src="https://github.com/user-attachments/assets/cb5e32f6-8c58-42e8-b6eb-74a80a47cdaa" />

### Membuat View Login
Halaman ini berfungsi sebagai antarmuka pengguna untuk melakukan proses autentikasi. Form ini menggunakan metode post untuk mengirimkan data secara aman ke Controller. Di dalamnya terdapat pengecekan session flashdata untuk memberikan feedback jika pengguna salah memasukan email atau password salah.

Buat direktory baru bernama user di dalam direktory app/Views/, kemudia buat file baru dengan nama login.php pada direktory app/Views/user/.

<img width="1227" height="617" alt="image" src="https://github.com/user-attachments/assets/6eeeb25f-c681-4d95-a8f9-2c22ca37f12e" />

### Konfigurasi Routing Login dan Logout
Konfigurasi ini berfungsi untuk mendaftarkan alamat URL /user/login dan /user/logout ke dalam sistem. Tanpa konfigurasi ini, browser akan menampilkan Error 404 (Page Not Found) karena sistem tidak tahu URL tersebut harus diarahkan ke Controller User.

Buka file routes.php untuk melakukan update atau konfigurasi dan tambahkan kode berikut.

<img width="782" height="199" alt="image" src="https://github.com/user-attachments/assets/7a57831e-7218-47bc-9d70-f83dafd2fd0a" />

Kemudian buka browser untuk melihat halaman login.

<img width="1218" height="643" alt="image" src="https://github.com/user-attachments/assets/ca92a58e-7bb9-4b9f-bde2-7a500238485e" />

### Membuat Auth Filter
Auth filter berfungsi untuk menciptakan sistem keamanan (middleware). Filter ini akan memeriksa apakah pengunjung sudah login atau belum. Jika belum, filter secara otomatis akan menolak akses dan mengarahkan kembali pengunjung ke halaman login, sehingga folder admin tidak bisa diakses sembarangan.

Buat file dengan nama Auth.php pada direktory app/Fillters/ lalu isi dengan kode berikut.

<img width="1222" height="517" alt="image" src="https://github.com/user-attachments/assets/bc33d621-1500-4b12-bfa1-79d6229df455" />

### Aktivasi Filter
Aktivasi filter ini dilakukan untuk menghidupkan sistem keamanan yang telah dibuat. Dengan mendaftarkan rute admin/* ke dalam filter before, maka setiap kali ada permintaan akses ke halaman admin (seperti tambah, edit, atau hapus artikel), sistem akan otomatis menjalankan pengecekan login terlebih dahulu. Jika pengguna belum login, maka akan diarahkan kembali ke halaman login.

Buka file app/Config/Fillters.php cari public arry $aliases lalu tambahkan kode 'auth' => \App\Filters\Auth::class,.

<img width="1206" height="435" alt="image" src="https://github.com/user-attachments/assets/3a306f95-810f-4255-8f45-cb231e354c22" />

Masih di file yang sama cari bagian public $globals kemudian tambahkan kode 'auth' => ['except' => ['user/login', 'user/logout', '/']],.

<img width="1233" height="333" alt="image" src="https://github.com/user-attachments/assets/761437bd-8c56-4f97-bbc3-31840cd35854" />

### Melakukan Uji Coba (Testing)
Pengujian dilakuakn untuk mengetahui apakah sistem yang di buat sudah berjalan dengan baik atau belum. Dalam Pengujian ini dilakukan beberapa tahapan untuk pengujiannya.

- Tahap 1: Uji Coba Fillter Keamnana
Untuk melakukannya ketik manual di browser localhost:8080/admin/artikel, jika di lempar kembali ke halaman login berarti fillter keamanan berhasil diterapkan.

- Tahap 2: Uji Coba Login Gagal

Masukan email dan password asal - asalan untuk melakukan uji coba login gagal.

<img width="1220" height="724" alt="image" src="https://github.com/user-attachments/assets/2a1be709-c91f-43bb-855c-73de969d5d6e" />

- Tahap 3: Uji Coba Login Sukses
Untuk melakukan masukan email dan password dengan benar. Maka akan di arahkan ke halaman admin.

<img width="1026" height="584" alt="image" src="https://github.com/user-attachments/assets/0a678135-78af-440c-a887-ed5fb2c055a2" />

<img width="948" height="558" alt="image" src="https://github.com/user-attachments/assets/5fd2a553-9683-4b5f-826d-d264e65fda20" />















































































