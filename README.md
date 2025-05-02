|Nama|NIM|Kelas|Matkul|
|----|---|-----|------|
|Khairinisya Ani Atmaja|312310365|TI.23.A4|Pemograman Web 2|

Download code igniter

1. cek code igniter dengan "php spark"
![image](https://github.com/user-attachments/assets/9339edec-4571-42dd-bd36-075b8b720274)

2. nyalakan code igniter dengan "php spark server"
![image](https://github.com/user-attachments/assets/f11bae5d-8e8d-4473-ad8f-03b64a6d21c3)

cek di localhost808
![image](https://github.com/user-attachments/assets/2aff510b-7383-45a1-836e-d794fb5e7190)

3. buka vscode dan buka folder app/controller/home.php di folder igniter yang suda di install
![image](https://github.com/user-attachments/assets/e3aa9f89-c7d7-4124-9f04-35d89c1b6184)
hapus tanda (;) di akhir tambahkan welcome message

4. tambahkan rute di app/config/Routes.php
![image](https://github.com/user-attachments/assets/e0f1241c-2a9c-4fde-8cb2-c594d6733f59)

6. tambahkan rute baru di routes.php dengan
![image](https://github.com/user-attachments/assets/15887e3b-3e83-4ecb-871a-f6241cda7a6c)

7. di shell ketik php spark routes untuk mengetahui routesnya
![image](https://github.com/user-attachments/assets/58482fa2-914c-4244-9eba-b7d598588969)

8. ketik di localhost http://localhost:8080/about
![image](https://github.com/user-attachments/assets/e091ce81-b415-4902-9388-ff509a08a11d)
kalau sudah ada output 404 berarti udah terhubung

9. buat controller dengan page.php
![image](https://github.com/user-attachments/assets/281397a0-8722-4e83-b683-8e86337d8a98)

resresh pagenya akan muncul seperti ini :
![image](https://github.com/user-attachments/assets/7da8d199-136d-4c48-ae27-3a9c60a003f6)

10. MEmbuat view di app/Views/about.php
![image](https://github.com/user-attachments/assets/0f09d155-b9c0-4a66-bfa0-c98f7c7e4b89)

11. ubah method aboud pada class cpntroller page
![image](https://github.com/user-attachments/assets/925ddb4d-1d26-4fd1-8c0b-738853080155)

12. buat style.css yang telah dibuat sebelumnya
![image](https://github.com/user-attachments/assets/7853be92-f77e-4cf7-b58e-d980b2e53cea)

13. buat folder template di folder app/view, di dalam folder template dan buat table baru, header dan footer
![image](https://github.com/user-attachments/assets/685f4c88-f20d-446c-aba6-484c3790434d)
header

footer 
![image](https://github.com/user-attachments/assets/c72ff4ab-51bc-40f3-93ca-f15154995ba9)

14. kemudian ubah file app/view/about.php dengan menambahkan include header an footer
![image](https://github.com/user-attachments/assets/0613be61-7a2e-435c-aad8-7519d1b28762)

setelah itu refresh http://localhost:8080/about. maka akan menjadi
![image](https://github.com/user-attachments/assets/1c9aeb7f-9eda-4ad5-b621-eec89792e5c4)

Tugas :
lengkapi kode program untuk menu lainnya yang ada pada controller page, sehingga semua dapat ditampilkan dengan layout yang sama
about
![image](https://github.com/user-attachments/assets/6f217b37-6977-4bd7-aad2-f3ae7cb52d64)

kontak
![image](https://github.com/user-attachments/assets/8475cb0b-0b9b-4174-a8bb-781310fa8ff5)

Tugas 2
1. buat database bernama lab_ci4 dan buat tabel bernama artikel didalamnya, dalam artikel ada id,judul,isi,gambar,status, slug
![image](https://github.com/user-attachments/assets/e7a1dee2-b8ef-425a-93e4-1bfe3729d479)

2. koneksikan database
   buat file bernama .env dan temukan tulisan database
   ![image](https://github.com/user-attachments/assets/9b8b536a-a294-452a-9f5f-59d2571e3d2b)
didalam tulisan "database.default.database" isi dengan nama database yang sudah dibuat

3. buat file baru di dalam app/Models yang bernama ArtikelModel.php
![image](https://github.com/user-attachments/assets/0afa06a9-dc58-44f9-88b4-218c89f95352)

4. buat controller dengan nama artikel.php pada app/Controllers
![image](https://github.com/user-attachments/assets/c078873a-eced-498d-a7bd-9971cc3f1d3c)

5. buat folder dengan nama artikelpada direktori app/views kemuadian buat file baru bernama index.php
![image](https://github.com/user-attachments/assets/bdc6a9b7-c1cd-42f5-b735-a62a612dfd64)

lalu buka web http://localhost:8080/artikel, dan lohat perubahannya

6. di mysql, insert kalimat dalam table artikel yang tehubung di database

7. refresh web artikel dan cek
![image](https://github.com/user-attachments/assets/c2f3644f-043e-4161-838a-70d2dfa28068)

8. buat tampilan detail artikel menambah fungsi baru pada app/controllers/artikel.php dengan nama view()
![image](https://github.com/user-attachments/assets/0f0ffc0b-8d92-41f7-b83e-88cc8edfa594)

buat view baru di halaman detail artikel pada direktori app/views/artikel namanya detail.php
![image](https://github.com/user-attachments/assets/3fda6f94-57d3-408c-911e-50370de3db82)

buat route untuk artikel detail
![image](https://github.com/user-attachments/assets/95ee8658-a8c4-4c07-8b55-d95b30075ea4)
![image](https://github.com/user-attachments/assets/f044a069-f282-4734-9d4c-70be6603e186)


fungsi videw() dan detail.php berfungsi ketika di klik maka memunculkan artikel tersebut , contohj :
![image](https://github.com/user-attachments/assets/ddf2042e-0205-483a-9a39-27de23529f47)

9. buat panel admin di direktori app/controllers/artikel.php dengan admin_index()
![image](https://github.com/user-attachments/assets/2cf092da-58e3-43eb-9599-b381aec45326)

buat tampilan adminnya di app/views/artikel namanya admin_index.php
![image](https://github.com/user-attachments/assets/90161da9-a00b-4d24-b3f1-eb632b8d09f7)
![image](https://github.com/user-attachments/assets/fb4f73a0-9a63-41c8-8f0b-2fa73343649f)
![image](https://github.com/user-attachments/assets/08dbeaed-9fcd-4236-9646-8b47fa992122)
![image](https://github.com/user-attachments/assets/0d84fc44-0833-44ea-819e-5aa25690f594)

tambahkan route baru untuk menu admin app/config/routes.php
![image](https://github.com/user-attachments/assets/41685e87-39ab-4f27-8f9f-d08a0e233759)

lalu akses dengan url http://localhost:8080/admin/artikel/
![image](https://github.com/user-attachments/assets/57b35129-e8a5-4255-9264-7010b646a7cb)

10. menambah data artikel, di app/controllers/artikel.php dengan nama add()
![image](https://github.com/user-attachments/assets/7bcfa85d-1798-46a2-9048-7650928e7cec)

kemudian vuat view baru untuk menambah artikel direktori app/views/artikel dengan nama form_add.php
![image](https://github.com/user-attachments/assets/1545674b-012f-47d8-93b4-98613a05d95f)

11. membuat fungsi untuk mengubah data artikel app/controllers/artikel.php dengan nama edit()
![image](https://github.com/user-attachments/assets/1fb8dbe7-4358-444c-b92f-065673631aca)

buat view tampilan editnya di direktori app/views/artikel dengan nama form_edit.php
![image](https://github.com/user-attachments/assets/c6c62251-d205-4a58-9def-c4babb93096d)

tampilannya :
![image](https://github.com/user-attachments/assets/b23760fb-837a-455a-b1cf-ac0598f1ff27)

12. membuat fungsi delete di tempat app/Controllers/artikel.php dengan nama delete()
![image](https://github.com/user-attachments/assets/316d918d-0463-4977-adeb-d7bcd9ab1bd8)


Tugas 3

1. buat layout di dalam app/views dan buat file dengan nama main.php di dalam folder layout dengan kode berikut
![image](https://github.com/user-attachments/assets/317ebd2a-87c4-4b28-af29-143bb0e3d66a)
![image](https://github.com/user-attachments/assets/79a67892-04fe-48e9-bd1e-f64a3810a9b5)

2. buat file pada direktori app/views dengan nama home.php
![image](https://github.com/user-attachments/assets/c377d0fd-d111-46b6-b080-4f0801953bc2)

3. buat class view, folder baru di app/ dengan nama cells, buat file artikelterkini.php dalam app/cells
![image](https://github.com/user-attachments/assets/3be8eb28-5360-4c30-962e-92a2d780e3bd)

4. buat folder components dalam app/views dan buat file artikel_terkini.php dalam direktori app/views/components
![image](https://github.com/user-attachments/assets/def4d5d7-6830-48c8-820d-fea24cdb7961)

Tugas dan pertanyaan
1. apa manfaat utama dari view layout dalam pengembangan aplikasi?
2. jelaskan perbedaan antara cell dan view biasa
3. ubah view cell agar hanya menampilkan kategori tertntu saja

jawab
1. View layout membantu mengatur dan mengelola tampilan antar komponen UI secara konsisten, responsif, dan terstruktur, terutama ketika tampilan perlu menyesuaikan berbagai ukuran layar atau orientasi.
2. - cell : Dipakai untuk menampilkan item-item dalam daftar dinamis.
   - view biasa : 	Digunakan untuk membangun tampilan statis maupun dinamis.
3. -

