## Nama : Khairinisya Ani .A.
## NIM  : 312310365
## kelas :TI 23 A.4

1. Untuk mengaktifkan ekstentsi tersebut, melalu XAMPP Control Panel, pada bagian Apache klik Config -> PHP.ini
![foto1](https://github.com/user-attachments/assets/1e07a78e-4080-4e57-a60a-50408b6259b7)

2. Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan diaktifkan. Kemudian simpan kembali filenya dan restart Apache web server.
![foto2](https://github.com/user-attachments/assets/b0915c52-97a1-4dab-b56e-d88e2488dd40)

3. Instalasi Codeigniter 4 Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual dan menggunakan composer.
![foto3](https://github.com/user-attachments/assets/4c996e3e-7693-4459-b0a7-f06aaf475a30)

4.Menjalankan CLI (Command Line Interface) Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses CLI buka terminal/command prompt.
![foto4](https://github.com/user-attachments/assets/e5fb44b4-663b-47a4-b9fd-27c88a29a75f)
Arahkan lokasi direktori sesuai dengan direktori kerja project dibuat (xampp/htdocs/lab11_ci/ci4/)

5. Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah: PHP SPARK
![foto5](https://github.com/user-attachments/assets/ab2ed5dc-a91f-4583-9ee2-a0bfbd192390)

6. Mengaktifkan Mode Debugging Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program. Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan pesan kesalahan seperti berikut
![foto6](https://github.com/user-attachments/assets/21ffd5f3-ff56-41a6-b4d2-b0b484455376)

7. Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment variable CI_ENVIRINMENT menjadi development.
![foto7](https://github.com/user-attachments/assets/67278ef5-865f-4c9c-a188-2494c9a8bc4c)

Ubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable CI_ENVIRINMENT menjadi development.
![foto7(1)](https://github.com/user-attachments/assets/4a07fab5-1adf-4700-8ed2-eb1cae0ecbb9)

Contoh error yang terjadi. Untuk mencoba error tersebut, ubah kode pada file app/Controller/Home.php hilangkan titik koma pada akhir kode.
![425317938-ed11d490-dc4f-431f-8d8e-ce1fd94dce35](https://github.com/user-attachments/assets/832a8ffb-da17-484c-8d1f-977b51ea1da2)

8. Pada Codeigniter, request yang diterima oleh file index.php akan diarahkan ke Router untuk meudian oleh router tesebut diarahkan ke Controller. Router terletak pada file app/config/Routes.php
![425318337-d4492232-bce8-43f8-a232-fce17fdce80f](https://github.com/user-attachments/assets/47c1d99e-29cb-4582-9e60-fa3c447622aa)

9. Membuat Route Baru. Tambahkan kode berikut di dalam Routes.php
$routes->get('/about', 'Page::about'); $routes->get('/contact', 'Page::contact'); $routes->get('/faqs', 'Page::faqs');
![425318952-e0df964a-7992-4fa7-964f-61993655aab0](https://github.com/user-attachments/assets/95597010-e899-4e1f-b67c-c70f41bbc496)

Untuk mengetahui route yang ditambahkan sudah benar, buka CLI dan jalankan perintah berikut.
![433188767-5c07fc9e-65dc-46af-8891-10742ae7581d](https://github.com/user-attachments/assets/f30fb009-55e0-4cdc-9b30-c7b7b52b23e0)

Selanjutnya coba akses route yang telah dibuat dengan mengakses alamat url http://localhost:8080/about
![425320294-2f3edd4f-6569-43a8-9800-b6273c99b5bc](https://github.com/user-attachments/assets/418d0604-2e26-4367-9085-8b07c2668f7c)

Ketika diakses akan mucul tampilan error 404 file not found, itu artinya file/page tersebut tidak ada. Untuk dapat mengakses halaman tersebut, harus dibuat terlebih dahulu Contoller yang sesuai dengan routing yang dibuat yaitu Contoller Page.

10. Membuat Controller Selanjutnya adalah membuat Controller Page. Buat file baru dengan nama page.php pada direktori Controller kemudian isi kodenya seperti berikut.
![425321216-c299574b-ce23-460a-a56d-3db282e82ac3](https://github.com/user-attachments/assets/34499921-d0fa-4342-acee-15a2aa68d465)

Selanjutnya refresh Kembali browser, maka akan ditampilkan hasilnya yaotu halaman sudah dapat diakses.
![425323742-3f5987fd-8fe8-4cf8-8a19-e067cc3fef12](https://github.com/user-attachments/assets/2adde603-1f4d-44c4-b81b-72e17cbf8c52)

11. Auto Routing Secara default fitur autoroute pada Codeiginiter sudah aktif. Untuk mengubah status autoroute dapat mengubah nilai variabelnya. Untuk menonaktifkan ubah nilai true menjadi false.

Method ini belum ada pada routing, sehingga cara mengaksesnya dengan menggunakan alamat: http://localhost:8080/page/tos
![425324588-31cf84ba-697f-443b-87e3-dd2789cc8637](https://github.com/user-attachments/assets/a8a1475d-23fe-4b13-8719-1f6ec7927e28)

12. Membuat View Selanjutnya dalam membuat view untuk tampilan web agar lebih menarik. Buat file baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi kodenya seperti berikut.
![425325261-daff301b-6d8d-4be0-a055-325edffa0e96](https://github.com/user-attachments/assets/fcf19f26-5725-4744-a7d2-a106c81f1078)

Ubah method about pada class Controller Page menjadi seperti berikut:
<img width="627" alt="425325590-9d95d4ac-d564-4f7e-a5a0-3434f6ea8e52" src="https://github.com/user-attachments/assets/c60121d1-c981-4167-991b-410e435c61c4" />

Kemudian lakukan refresh pada halaman tersebut.
![425325830-b285993b-bf83-449c-a4d4-e283d25cb86c](https://github.com/user-attachments/assets/9094f42e-f910-4f2c-997a-c1991e14bfec)

13. Membuat Layout Web dengan CSS Pada dasarnya layout web dengan css dapat diimplamentasikan dengan mudah pada codeigniter. Yang perlu diketahui adalah, pada Codeigniter 4 file yang menyimpan asset css dan javascript terletak pada direktori public. Buat file css pada direktori public dengan nama style.css
![425326565-d4099607-3343-4ae5-b1e7-c972aed2c39b](https://github.com/user-attachments/assets/6e50fb0d-5fe0-4384-9471-689e751fc6ea)

Kemudian buat folder template pada direktori view kemudian buat file header.phph dan footer.php
![425327295-3fb3cbc9-7f2f-4e8f-bbec-7a1abcc84c65](https://github.com/user-attachments/assets/976bb4fa-d71f-43e8-b426-58f2d2cdc1b7)

File app/view/template/footer.php
![425328498-ec607eeb-4662-459a-b9cb-64b2fe96b717](https://github.com/user-attachments/assets/63fdf827-42e5-4f29-8f15-e7b6e3dd907b)

Kemudian ubah file app/view/about.php seperti berikut.
![425328889-cd5c4862-8a4b-4fab-a187-83a853bfbc5b](https://github.com/user-attachments/assets/f923c091-c8c5-47dd-ba64-d96b76d31c06)

Selanjutnya refresh tampilan pada alamat http://localhost:8080/about
![433190793-4c8eb14e-a444-4324-9883-509174cc72ee](https://github.com/user-attachments/assets/16025910-4708-422e-8882-93b2c8bae9e0)

14. Membuat database di my sql dengan nama lab_ci4
![425801788-9eb909fb-33ef-4c69-ae6c-4359e2a0e332](https://github.com/user-attachments/assets/fe651968-a4a8-4919-ad62-dffe542b6393)

setelah membuat data base, lalu membuat tablenya dengan nama artikel
![425801853-b20b1606-c8c0-420a-a778-1812ae5b2cc7](https://github.com/user-attachments/assets/6571498e-8131-4ac0-b001-0dac1edfd820)

15.Konfigurasi koneksi database Selanjutnya membuat konfigurasi untuk menghubungkan dengan database server. Konfigurasi dapat dilakukan dengan du acara, yaitu pada file app/config/database.php atau menggunakan file .env. Pada praktikum ini kita gunakan konfigurasi pada file .env.
![425801923-298f0c1b-66c5-4285-9f2e-1f6380750355](https://github.com/user-attachments/assets/f0858ef7-1a58-46af-8d01-a4c5db017043)

16. Membuat Model Selanjutnya adalah membuat Model untuk memproses data Artikel. Buat file baru pada direktori app/Models dengan nama **ArtikelModel.php
![425802073-50b97124-a21c-4b39-b0bd-a11d053fbaba](https://github.com/user-attachments/assets/7c523a21-ec19-4eea-a090-c9e28d3638ee)

17. Membuat Controller Buat Controller baru dengan nama Artikel.php pada direktori app/Controllers.
![425802214-898d6d00-d37a-4437-b348-2320f0c9e88c](https://github.com/user-attachments/assets/a9392b06-c9ae-40f7-829e-087fd8e1ad5f)

18. Membuat View Buat direktori baru dengan nama artikel pada direktori app/views, kemudian buat file baru dengan nama index.php.
![425802305-daac512a-cc9f-4006-9f8a-d8381b91b38e](https://github.com/user-attachments/assets/5f324858-5b47-481d-b45e-92acb1696611)

Selanjutnya buka browser kembali, dengan mengakses url http://localhost:8080/artikel
![425802776-2095cbd0-8697-4dce-8fa2-9ec28b9d4663](https://github.com/user-attachments/assets/cea8202e-bc89-4ed6-ada6-dd5e6d140cec)

Belum ada data yang diampilkan. Kemudian coba tambahkan beberapa data pada database agar dapat ditampilkan datanya.

INSERT INTO artikel (judul, isi, slug) VALUE ('Artikel pertama', 'Lorem Ipsum adalah contoh teks atau dummy dalam industri percetakan dan penataan huruf atau typesetting. Lorem Ipsum telah menjadi standar contoh teks sejak tahun 1500an, saat seorang tukang cetak yang tidak dikenal mengambil sebuah kumpulan teks dan mengacaknya untuk menjadi sebuah buku contoh huruf.', 'artikel-pertama'), ('Artikel kedua', 'Tidak seperti anggapan banyak orang, Lorem Ipsum bukanlah teks-teks yang diacak. Ia berakar dari sebuah naskah sastra latin klasik dari era 45 sebelum masehi, hingga bisa dipastikan usianya telah mencapai lebih dari 2000 tahun.', 'artikel-kedua');

Refresh kembali browser, sehingga akan ditampilkan hasilnya.
![433191321-2081ddc0-5f4a-481a-85da-1674e44665be](https://github.com/user-attachments/assets/706608c4-8e32-419e-a3fe-f5400c1d6b4b)

19. Membuat Tampilan Detail Artikel Tampilan pada saat judul berita di klik maka akan diarahkan ke halaman yang berbeda. Tambahkan fungsi baru pada Controller Artikel dengan nama view().
![425803084-f407fc46-c2e9-48f7-9dac-7544ffc0ffd0](https://github.com/user-attachments/assets/d8cf140d-0122-477d-b653-3ffefc87f862)

20.Membuat View Detail Buat view baru untuk halaman detail dengan nama app/views/artikel/detail.php.
![425803155-52dcb932-f354-47e4-adfc-6c3d3d4c573e](https://github.com/user-attachments/assets/5c86dddc-7ab4-45cb-a000-6c35766140a5)

21. Membuat Routing untuk artikel detail Buka Kembali file app/config/Routes.php, kemudian tambahkan routing untuk artikel detail.
![425803236-960ded60-038f-4163-917b-e92d9c3c165a](https://github.com/user-attachments/assets/06b1fd42-0ece-4a98-a321-f2aab0a4c0fb)

22. Membuat Menu Admin Menu admin adalah untuk proses CRUD data artikel. Buat method baru pada Controller Artikel dengan nama admin_index().
![425803315-e857ac11-fafe-40d2-b0ec-3d3094c0a940](https://github.com/user-attachments/assets/21790301-655e-4014-bf13-cac334b7e368)

Selanjutnya buat view untuk tampilan admin dengan nama admin_index.php
![425803678-7a5e3ccf-89eb-4699-88a3-36317d84c097](https://github.com/user-attachments/assets/3bcf4147-f600-48da-bf34-35fbecd7733d)

![425803687-1a872862-e42b-4843-a3c1-443e099ffd8d](https://github.com/user-attachments/assets/5f52059f-c898-4873-ad7b-7692bcaeb271)

![425803700-bd54a369-8ce0-4851-bdc2-5d679efaf666](https://github.com/user-attachments/assets/65868fa7-b534-409d-93a6-b35f53d72078)

![425803705-4af20293-7339-4195-8d14-06a92594ddc6](https://github.com/user-attachments/assets/b2452448-540c-426a-bf99-a7ddccd83050)

Tambahkan routing untuk menu admin seperti berikut:
![425803775-03d240eb-467b-4508-a385-7051320b167f](https://github.com/user-attachments/assets/f660c317-1111-4298-a2d2-222e9dc64b16)

Akses menu admin dengan url http://localhost:8080/admin/artikel
![425803797-a29dda68-4955-46d5-952d-79e928701737](https://github.com/user-attachments/assets/e504c335-59ae-40fa-ac60-87ce32abb9ab)

23. Menambah Data Artikel Tambahkan fungsi/method baru pada Controller Artikel dengan nama add().
![425803871-021a3384-b68b-4b3a-b8ac-4c670e476005](https://github.com/user-attachments/assets/c6d30de0-6d75-41cd-ad61-31de2ed958a8)

Kemudian buat view untuk form tambah dengan nama form_add.php
![425803975-60aa76cb-c0f2-4b26-a3b3-2728e6ca4a77](https://github.com/user-attachments/assets/e806ca5f-7de6-4086-b8aa-f818c8faab07)

![425803968-c4523463-46d7-4213-af73-b958cd279108](https://github.com/user-attachments/assets/c7f87f96-c33c-4952-87d9-00a4e2b2a09f)

24. Mengubah Data Tambahkan fungsi/method baru pada Controller Artikel dengan nama edit().
![425804020-d8684394-4097-4550-be78-cdb8857ad6bb](https://github.com/user-attachments/assets/399298f8-605d-4551-aea3-d0b316b1d354)

Kemudian buat view untuk form tambah dengan nama form_edit.php
![425804051-e576d3f0-5785-4f69-9129-1945e790ad72](https://github.com/user-attachments/assets/c572c0f7-1bea-488e-940e-857fe3fe511b)

![425804098-300bb226-325c-4de1-9481-aa998e38b4c7](https://github.com/user-attachments/assets/81a9831f-acc1-4988-bfa0-b385297b9afb)

25. Menghapus Data Tambahkan fungsi/method baru pada Controller Artikel dengan nama delete().
![425804152-276a3ee5-2b3a-4470-8a1d-a662d94fcb91](https://github.com/user-attachments/assets/886d1398-fa22-4f02-8b44-511ff1d33704)

26. Membuat Layout Utama Buat folder layout di dalam app/Views/ Buat file main.php di dalam folder layout dengan kode berikut:
![425804292-c3ea7d25-7e97-4c06-a53a-26b3a2acaa03](https://github.com/user-attachments/assets/03856612-4a54-4081-8066-af96443cc9b4)

![425804303-0051ef7e-24f6-4740-97c2-96f3ec10341f](https://github.com/user-attachments/assets/e29d76cc-f235-4aed-9680-8b7af925d5b9)

27. Modifikasi File View Ubah app/Views/home.php agar sesuai dengan layout baru:
![425804365-e5a2fbb3-064e-470c-98b0-aafe29a15e31](https://github.com/user-attachments/assets/5e9d6adf-4efd-4af4-83fd-60a00f3fb81b)

28.Membuat Class View Cell Buat folder Cells di dalam app/ Buat file ArtikelTerkini.php di dalam app/Cells/ dengan kode berikut:
![425804444-6be0740b-4e46-430b-bab6-20207e85e7d5](https://github.com/user-attachments/assets/c81227c4-a662-4c7c-a5c7-54d44077a2f9)

29. Membuat View untuk View Cell Buat folder components di dalam app/Views/ Buat file artikel_terkini.php di dalam app/Views/components/ dengan kode berikut:
![425804468-d250d040-7b4e-4ad9-9d63-c59293f2ce9c](https://github.com/user-attachments/assets/40303522-27e5-46d7-abee-293028bfa3d4)

30. Menambahkan tanggal tujuanya agar mendapatkan data aertikel yang baru di ubah
![425804637-313b69f7-f993-4487-82ce-22c9817fb689](https://github.com/user-attachments/assets/aa9d311d-ac38-4c93-a909-61c86c412bb9)

contohnya seperti ini :
![425804726-88d73672-4819-47fa-8d32-1c22c1b740a7](https://github.com/user-attachments/assets/d2bc0a0f-986f-4d13-b257-56b3367ad859)

Apa manfaat utama dari penggunaan View Layout dalam pengembangan aplikasi? jawab :

1. Struktur yang Terorganisir
Memudahkan pengaturan elemen UI dengan tata letak yang rapi dan terstruktur.

2. Responsivitas yang Lebih Baik
Memastikan tampilan UI menyesuaikan dengan berbagai ukuran layar dan orientasi perangkat.

3. Pemeliharaan Kode yang Lebih Mudah
Dengan pemisahan tata letak dan logika bisnis, perubahan UI lebih mudah dilakukan tanpa mengganggu fungsionalitas aplikasi.

4. Penggunaan Ulang Komponen
Layout dapat digunakan kembali di berbagai bagian aplikasi, mengurangi redundansi kode.

5. Kinerja yang Lebih Optimal
Beberapa jenis layout dioptimalkan untuk performa yang lebih baik, seperti ConstraintLayout di Android yang mengurangi jumlah view hierarchy.

Jelaskan perbedaan antara View Cell dan View biasa. jawab :
![425804924-3f08a236-4d3c-4d34-ab79-991e4f154339](https://github.com/user-attachments/assets/927e0c0f-c809-49a4-9c5d-a74d72df07c4)
