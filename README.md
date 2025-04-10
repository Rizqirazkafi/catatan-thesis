# _NixOS Cloud VPS Deployment_ Berbasis Web dengan Proxmox dan Ansible

> Disusun oleh : M. Rizqi R 

## BAB I - PENDAHULUAN

### Latar Belakang

Pada pembuatan _Virtual Private Server_(VPS), penggunaan cloud init diperlukan
untuk otomasi sehingga bisa mengkonfigurasi server sesuai kebutuhan pelanggan
dengan mudah dan cepat. Namun yang jadi permasalah ada tidak semua sistem 
operasi berbasis GNU/Linux mendukung cara tersebut, terutama NixOS. Ini 
dikarenakan NixOS merupakan sistem operasi yang bersifat _atomic_ dan _immutable_
dimana perubahan sistem operasi dilakukan dengan merubah dan mengiplementasikan
konfigurasi. 
### Rumusan Masalah
Adapun rumusan masalah berdasarkan latar belakang diatas yaitu:
1. Bagaimana cara mengotomasi Proxmox VE untuk mendeploy VM NixOS?
1. Bagaimana alur otomasi Proxmox VE untuk mendeploy VM NixOS?
1. Berapa lama waktu yang dibutuhkan untuk mendeploy VM NixOS?

### Batasan Masalah 
Batasan masalah dalam penelitian ini adalah:
1. Antarmuka yang dibuat merupakan antar muka jenis web.
1. Otomasi yang dibuat hanya meliputi fungsi minimal yaitu membuat, menghapus, dan 
memonitor VM.
1. Otomasi tidak meliputi keamanan kredensial pengguna.

### Tujuan Penelitian
Adapun tujuan dalam penelitian ini adalah:
1. Membuat otmasi yang dapat berinteraksi dengan Proxmox mendeploy VM NixOS.
1. Mengukur waktu yang dibutuhkan untuk mendeploy VM NixOS.

### Manfaat Penelitian 
Manfaat yang dihasilkan penelitian ini antara lain:
1. Membantu penyedia layanan VPS untuk menambahkan NixOS sebagai opsi sistem 
operasi.
1. Membantu perluasan penggunaan NixOS dalam ranah server sebagai sistem 
sistem operasi yang murni berbasis konfigurasi.

## BAB II - Kajian Pustaka dan Landasan Teori

Pada bagian ini dipaparkan penelitian terdahulu yang berkaitan dengan 
penelitian ini. Demikian juga diberikan definisi serta beberapa contoh 
terkait sebagai dasar teori yang menjadi referensi dalam penelitian.

### Penelitian Terdahulu.

Penelitian yang pernah membahas mengenai penggunaan Ansible untuk otomasi 
_Virtual Machine_ pada Proxmox VE pernah dilaksanakan oleh Putu Hariyadi 
& Khairan Marzuki yang dimana Ansible playbook berjalan dengan baik untuk 
menyiapkan lingkungan praktikum untuk perkuliahan. Topik ini dibahas dalam 
penelitian mereka yang berjudul "_Implementation Of Configuration Management
Virtual Private Server Using Ansible_" pada tahun 2020 (Hariyadi & Marzuki,
2020).

Penelitian terhadap perbandingan Ansible dengan metode manajemen konfigurasi 
konvensional juga pernah dibahas oleh Tedi Alfiandi, T.M Diansyah, dan Risko 
Liza dalam "Analisis Perbandingan Manajemen Konfigurasi Menggunakan Ansible 
dan Shell Script Pada _Cloud Server Deployment_ AWS" pada tahun 2020.
Ansible dibandingan dengan metode shell script dalam bahasa BASH yang 
menyimpulkan bahwa penggunaan Ansible mampu memperingkas pekerjaan dalam tugas
membangun infrastruktur _web server_ (Alfiandi et al., 2020).

Dikarenakan disini menggabungkan metode manajemen konfigurasi sistem operasi 
antaranya adalah NixOS dan Ansible, maka selayaknya kita mendapatkan garis 
besar perbandingan diantara keduanya. Perbandingan ini pernah dilakukan oleh 
M. Rizqi R pada tahun 2024 dalam Skripsinya yang berjudul "Perbandingan 
Waktu Eksekusi Manajemen Konfigurasi Sistem Operasi GNU/Linux Antara Ansible 
Dengan NixOS". Hasilnya adalah Ansible memiliki performa yang lebih baik dari 
segi lamanya waktu eksekusi. Disisi lain, NixOS menang dalam segi representasi
konfigurasi yang berbanding lurus dengan sistem.

### Proxmox VE

### NixOS 

### Ansible 

### Shell Scripting

### Rest API 

### Flutter

## BAB III - Metode Penelitian 

Metodologi yang digunakan untuk penelitian ini memiliki beberapa tahapan 
sebagai pedoman agar hasil yang dicapai sesuai dan tidak menyimpang dari tujuan 
yang telah ditentukan sebelumnya.


### Metode Penelitian 
Metode yang diterapkan pada penelitian ini adalah metode _experimental design_.
Penerapan metode ....
