# DWDS26DHA_devops_week1

## Flow DevOps
DevOps merupakan gabungan dari *Development* dan *Operational*. Sebagai seorang *DevOps Engineer* kita berada diantara tim *developer* dan tim *operational*, sehingga kita harus memiliki skill komunikasi yang baik, agar dapat mencapai tujuan dari *project* perusahaan tempat kita bekerja. Alur kerja DevOps itu terdiri dari :
  * *Plan*
  * *Code*
  * *Build*
  * *Test*
  * *Release*
  * *Deploy*
  * *Operate*
  * *Monitor*
  
<p align="center">
  
![flow](https://user-images.githubusercontent.com/90166624/133670456-b60ebe84-b02b-445a-9af0-61a59a4d2ad8.jpg)
</p>

Berikut penjelasan dari alur DevOps :
1. **Plan** merupakan perencanaan bagaimana proses pengembangan produk yang akan dilakukan.

2. **Code** merupakan proses penulisan kode yang dibutuhkan produk.

3. **Build** merupakan proses ketika kode selesai dibuat, para developer akan bekerjasama untuk mereview kode yang sudah dibuat, jika tidak ada masalah akan berlanjut ke proses test.

4. **Test** merupakan pengujian dari kode yang telah selesai dibuat.

5. **Release** merupakan  proses pada tim IT Operasional, yang telah memastikan bahwa tidak ada masalah pada kode.

6. **Deploy** merupakan proses setelah kode di release dimana versi terbaru dari produk yang telah dikembangkan, akan diterapkan.

7. **Monitor** merupakan proses pemantauan produk ketika dijalankan, pada proses ini akan diambil data seperti data log dan data analisa. 

Alur tersebut terus dilakukan berulang-ulang, hingga produk dapat di rilis ke publik.

## Tools DevOps
Tools DevOps merupakan alat-alat yang digunakan oleh seorang DevOps engineer dalam melakukan pekerjaannya. Berikut merupakan tools yang diugunakan :

* **Source Code Management** <br>
Git merupakan salah satu contoh tools dari Source Code Management. Dengan menggunakan git para developer bisa merubah dan memeriksa kode mereka, serta mereka bisa melakukan VCS (Version Control System) untuk menambahkan versi baru, serta kembali ke versi sebelumnya.

* **Build Server** <br>
Build server merupakan alat automation yang melakukan compile kode pada SCR agar kode tersebut dapat di eksekusi. Contoh tools nya adalah Jenkins, dan Sonarqube.

* **Configuration Management** <br>
Configuration Management berguna untuk melakukan manajemen konfigurasi pada server. Tools nya seperti puppet dan chef.

* **Virtual Infrastructure** <br>
Contoh tools dari virtual infrastructure adalah Amazon Web Services dan Microsoft Azure. Tools tersebut dijual oleh vendor Cloud dalam bentuk Platform as a Service (PaaS),  yang memungkinkan kita membuat mesin baru yang terprogram dengan alat manajemen konfigurasi.
Tools ini dikombinasikan dengan tools automation sehingga jika ingin menguji kode, cukup mengirimkan kode ke infrastruktur cloud, kemudian tes dijalankan secara otomatis.

* **Test Automation** <br>
Test automation merupakan pengujian otomatis melalui pipeline build untuk memastikan  bahwa build deployable sudah dilakukan. Tool nya seperti Selenium dan Air.
