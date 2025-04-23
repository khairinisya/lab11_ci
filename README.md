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



