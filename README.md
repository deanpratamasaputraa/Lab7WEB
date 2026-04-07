<img width="878" height="608" alt="image" src="https://github.com/user-attachments/assets/255338e1-cf63-41c2-88ac-b58678a701e9" /># Pratikum Pemograman Web 2
---
### Mata Kuliah: Pemograman Web 2
### Nama: Dean Pratama Saputra
### Nim: 312210114
### Kelas: I241B
### Dosen Pengampu: Agung Nugroho, S.Kom., M.Kom., S.Kom., M. Kom
---
## Langkah - Langkah Praktikum

### Praktikum 1: PHP Framework (Codeigniter)
### 1. mengaktifkan ekstentsi XAMPP Control Panel
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

















