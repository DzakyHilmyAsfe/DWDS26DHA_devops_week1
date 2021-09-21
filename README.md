## Flow DevOps
DevOps merupakan gabungan dari *Development* dan *Operational*. Sebagai seorang *DevOps Engineer* kita berada diantara tim *developer* dan tim *operational*, sehingga kita harus memiliki skill komunikasi yang baik, agar dapat mencapai tujuan dari *project* perusahaan tempat kita bekerja secara efektik dan efesien. Alur kerja DevOps itu terdiri dari :
  * *Plan*
  * *Code*
  * *Build*
  * *Test*
  * *Release*
  * *Deploy*
  * *Operate*
  * *Monitor*
  
 <p align="center">
  <img src="https://user-images.githubusercontent.com/90166624/133842970-d587632e-97b8-4573-aeba-c523437b4c1d.jpg?raw=true" alt="Sublime's custom image"/>
</p>


Berikut penjelasan dari alur DevOps :

1. **Plan** 

Fase ini melibatkan perencanaan untuk seluruh alur kerja yang dibutuhkan sebelum tim pengembang mulai menulis kode. Dalam tahap ini, manajer produk dan manajer proyek akan memainkan peran penting. Mereka akan bekerjasama untuk mengumpulkan requirements dan feedback dari klien ataupun stakeholders. Informasi tersebut kemudian akan dikumpulkan untuk membangun roadmap produk untuk memandu proses pengembangan yang akan dilakukan. 

2. **Code** 

Setelah rencana dibuat, tim developer dapat mulai menulis kode yang dibutuhkan untuk mengembangkan produk. Tim developer biasanya akan menggunakan seperangkat plugin standar yang dipasang di lingkungan pengembangan mereka untuk membantu proses pengembangan, membantu menerapkan gaya kode yang konsisten, serta menghindari kelemahan keamanan umum dan anti-pattern.

3. **Build** 

Setelah tim developer selesai menulis kode yang dibutuhkan, mereka akan memasukan kode tersebut ke dalam shared code repository. Developer akan mengirimkan pull request, setelah developer yang lain akan mereview perubahan yang telah dilakukan. Jika kode tidak memiliki masalah, maka developer tersebut akan menyetujui pull request yang telah dikirim sebelumnya.

4. **Test** 

Langkah selanjutnya adalah melakukan pengujian.  Jika ada masalah yang ditemukan pada fase ini, maka masalah tersebut akan dikirim kembali ke tim developer untuk diselesaikan.

5. **Release** 

Fase release menjadi tonggak penting dalam DevOps pipeline. Pada tahap ini, setiap perubahan kode telah melewati serangkaian pengujian dan tim IT operations telah memastikan bahwa masalah yang merusak dan regresi sudah teratasi dengan baik.

6. **Deploy** 

Tahap selanjutnya adalah deployment. Setelah production environment dibuat dan dikonfigurasi maka versi terakhir dari pengembangan yang telah dilakukan akan diterapkan.

7. **Operate**

Pada tahap ini produk akan di operasikan atau dijalankan.

8. **Monitor** 

Pada tahap terakhir ini, tim IT operations akan terus bekerja keras untuk memantau infrastruktur, sistem, dan aplikasi. Hal ini dilakukan untuk memastikan bahwa produk atau aplikasi yang dikembangkan dapat berjalan dengan lancar. Mereka juga mengumpulkan data-data penting dari log, analitik, sistem monitoring, serta melihat feedback dari pengguna untuk mengetahui jika ada masalah pada kinerja aplikasi.  

Alur tersebut terus dilakukan berulang-ulang, hingga produk dapat di rilis ke publik.

## Tools DevOps
Tools DevOps merupakan alat-alat yang digunakan oleh seorang DevOps engineer dalam melakukan pekerjaannya. Berikut merupakan tools yang diugunakan :

* **Planning**

Salah satu tools yang dapat kita gunakan untuk planning adalah asana, asana merupakan layanan yang dirancang untuk meningkatkan kolaborasi tim dan manajemen kerja. Ini membantu tim mengelola proyek dan tugas dalam satu alat. Tim dapat membuat proyek, menugaskan pekerjaan ke rekan satu tim, menentukan tenggat waktu, dan berkomunikasi tentang tugas secara langsung di Asana. Ini juga mencakup alat pelaporan, lampiran file, kalender, dan banyak lagi.

![Asana_logo svg](https://user-images.githubusercontent.com/90166624/134054718-da1d3a8f-978d-48e5-a93f-934ad4cd5bc8.png)

* **Source Code Management** 

Melalui sumber repository, antar developer dapat memeriksa dan mengubah kode tanpa perlu saling menulis satu sama lainnya. Source control ini mungkin telah ada sejak 40 tahun yang lalu, tetapi ini merupakan komponen utama dari Continuous Integration atau CI.

Git merupakan salah satu contoh tools dari Source Code Management. Dengan menggunakan git para developer bisa merubah dan memeriksa kode mereka, serta mereka bisa melakukan VCS (Version Control System) untuk menambahkan versi baru, serta kembali ke versi sebelumnya.

![download (1)](https://user-images.githubusercontent.com/90166624/134055442-acf44cf9-6e27-4212-9168-a17c392a5f4f.png)

* **Build Server**

Build server adalah alat otomatisasi yang mengkompilasi kode dalam SCR (Source Code Repository) ke dalam basis kode yang dapat dieksekusi.

Tols yang akan kita gunakan yaitu Jenkins, Jenkins adalah server otomatisasi sumber terbuka . Jenkins membantu mengotomatisasi bagian-bagian dari pengembangan software yang terkait dengan building , testing , dan deploying , jenkisn juga akan memfasilitasi Continuous Integration dan Continuous Delivery.

![250px-Jenkins_logo_with_title svg](https://user-images.githubusercontent.com/90166624/134058028-17c93a56-a832-46a5-9c4d-3a085271cc71.png)


* **Configuration Management** 

Configuration Management berguna untuk melakukan manajemen konfigurasi pada server. Tipe jaringan yang akan kita gunakan adalah jaringan client-server, sehingga kecepatan saat melakukan CI/CD menjadi lebih cepat dan efesien. Sedangkan Jenis IP yang akan kita gunakan adalah IP statis yang cocok digunakan untuk bisnis. Untuk membuat IP statis, kita bisa edit file interfaces yang lokasinya ada di “/etc/network/interfaces“. Caranya, jalankan perintah nano untuk membuka file tersebut, lalu tambahkan onfigurasi yang kita inginkan. 

root@ubuntu:~# nano /etc/network/interfaces

Setelah file interfaces terbuka, berikan konfigurasi yang kita inginkan. Misalnya seperti dibawah ini.

#The loopback network interface <br>
auto lo <br>
iface lo inet loopback <br>
auto eth1 <br>
iface eth1 inet static <br>

        address 192.168.10.20
        netmask 255.255.255.0
        network 192.168.10.0
        broadcast 192.168.10.255
        gateway 192.168.10.10
        dns-nameservers 8.8.8.8
        
Setelah selesai memberikan konfigurasi, simpan perubahan dengan menekan tombol **Ctrl+O** (save). Lalu keluar dengan menekan tombol **Ctrl+X** (Exit).

Kemudian restart service nya agar konfigurasi tadi bisa beroperasi. Perintahnya lihat di bawah ini.

root@ubuntu:~# /etc/init.d/networking restart

 Running /etc/init.d/networking restart is deprecated because it may not enable again some interfaces
 
 Reconfiguring network interfaces...  
 
Ignoring unknown interface eth1=eth1.
                                                         [ OK ]
root@ubuntu:~#

Status OK menandakan settingan telah siap. Setelah itu kita coba cek dengan menjalankan perintah ifconfig eth1.

![CaraSettingIPAddressStaticdiUbuntuServer](https://user-images.githubusercontent.com/90166624/134222004-1908cb69-b883-43af-a6a2-c41c90c43d08.png)


Tools nya seperti ansible, ansible menyediakan open source software , manajemen konfigurasi, dan alat penerapan aplikasi yang memungkinkan infrastruktur sebagai kode. Dengan menggunakan ansible kita dapat men konfigurasi banyak server secara langsung, tanpa perlu men konfigurasi server satu persatu.

![Ansible_logo svg](https://user-images.githubusercontent.com/90166624/134065171-c7f9747a-011a-48ca-bd03-356f03d80e7d.png)


* **Virtual Infrastructure** 

Amazon Web Services  adalah tools infrastruktur virtual. Virtual Infrastructure ini disediakan oleh vendor cloud yang menjual insrastruktur atau Platform as a Service (PaaS). Infrastruktur ini memiliki API yang memungkinkan kamu membuat mesin baru yang terprogram dengan alat manajemen konfigurasi.

Ada juga private cloud di mana private infrastructure virtual memungkinkan kamu menjalankan cloud di hardware sebagai data terpusat.

Alat ini dikombinasikan dengan alat otomatisasi untuk memberdayakan organisasi yang melatih DevOps dengan kemampuan konfigurasi server tanpa jari di atas keyboard. Jika ingin menguji kode baru, cukup mengirimkan kode ke infrastruktur cloud untuk membangun lingkungan. Kemudian tes dijalankan tanpa adanya campur tangan manusia.

![amazon-web-services](https://user-images.githubusercontent.com/90166624/134065385-7d28dc11-41d7-439f-9e95-1d70077b7a14.jpg)


* **Test Automation** 

Test automation merupakan pengujian otomatis melalui pipeline build untuk memastikan  bahwa build deployable sudah dilakukan. Tool nya seperti Selenium IDE.

Selenium IDE adalah aplikasi untuk melakukan pengujian web secara otomatis.Cara kerja selenium yaitu dengan merekam aktivitas user pada web yang diuji. Aktivitas yang direkam tersebut dapat disimpan dan dapat dijalankan kembali oleh user. Jadi user tidak perlu melakukan aktivitas yang sama dua kali pada web yang sama karena user dapat menjalankan rekaman yang sudah disimpan.

<img width="913" alt="Selenium_Logo" src="https://user-images.githubusercontent.com/90166624/134066219-9cb54692-c4a4-46e0-96f2-da2b25482b78.png">


* **Monitoring**

Produk IT menjadi sangat baik karena adanya proses monitoring saat produk tersebut digunakan oleh pengguna. Tujuannya adalah untuk mengetahui bagaimana perubahan yang ada pada kode cukup berdampak pada produk dan penggunanya. Tools yang akan kita gunakan adalah elastic stack.

Elastic Stack merupakan kumpulan produk open source (Elasticsearch, Logstash, Kibana dan Beat) dari elastic.co yang memiliki kemampuan untuk mengumpulkan dan mengolah data dari berbagai sumber data, menyimpan data dalam data center yang dapat ditingkatkan seiring berkembangnya data, dan menyediakan alat untuk menganalisis serta memvisualisasi data. 

![the-elastic-stack-thumb](https://user-images.githubusercontent.com/90166624/134066816-50e95b36-5005-49ea-9bd6-229874d750be.png)
