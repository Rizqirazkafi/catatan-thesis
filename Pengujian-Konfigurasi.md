# Sistem Pengujian Konfigurasi RouterOS Berbasis Virtualisasi untuk Sertifikasi MTCNA

## Abstrak
Pengujian untuk sertifikasi Miktorik Certified Network Associate (MTCNA) 
kebanyakan dilaksanakan secara _offline_ agar proktor dapat mengawasi
serta menguji pemahaman terkait teori dan praktik penggunaan RouterOS.
Namun ini dapat memakan biaya seperti gedung, konsumsi dan transport baik
bagi peserta dan panitia. Oleh karena itu dibutuhkan sebuah sistem dimana
pengujian dapat dilakukan secara _online_ untuk efisiensi biaya.
Maka dari itu, proposal ini bertujuan untuk menawarkan sistem tersebut 
dengan harapan Mikrotik mampu mempermudah proses baik sertifikasi maupun 
pelatihan.

# BAB I PENDAHULUAN

## Latar Belakang

Sertifikasi Mikrotik Certified Network Associate (MTCNA) diperlukan bagi 
yang ingin mempermudah dirinya untuk bekerja atau terjun ke bidang jaringan
komputer. Sertifikasi ini diselenggarakan oleh Mikrotik bekerja sama dengan 
pihak ketiga yang biasanya satu paket dengan pelatihan. Pelaksanaannya 
dilakukan secara _offline_ dengan menyewa tempat atau gedung selama beberapa
hari untuk melatih dan menguji peserta yang mengikuti pelatihan.

Mikrotik menyediakan pengujian secara _online_ dengan pengawasan proktor _via_
Zoom atau Google Meet dan pengujian tersebut diakses melalui situs resmi
Mikrotik. Dalam ujian ini, peserta harus membagikan layar komputer dan diawasi
oleh proktor selama ujian berlangsung. Sayangnya dalam pengujian berbasis
_online_ ini hanya diujikan tentang teori tanpa adanya praktik Konfigurasi
untuk RouterOS yang dimana seharusnya menjadi target utama pengujian.

Oleh karena itu dibutuhkan media pengujian _online_ yang lebih komprehensif
sehingga mampu meliputi baik dalam teori maupun praktik konfigurasi. Proposal 
ini dibuat dengan tujuan agar pengujian MTCNA dapat meliputi pengujian 
konfigurasi yang dilaksanakan secara _online_ .

Sistem dirancang menggunakan GNS3 untuk membuat topologi studi kasus pengujian 
sebagai _backend_ dimana terdapat _Virtual Machine_ berisi RouterOS dan PC
yang terhubung satu sama lain. Antarmuka yang digunakan oleh peserta dalam 
bentuk web untuk mengakses CLI RouterOS dan PC yang tersedia.

Peserta melakukan konfigurasi pada perangkat jaringan yang tersedia, kemudian
sistem akan memeriksa apakah konfigurasi yang telah dilakukan sudah memenuhi
kriteria studi kasus. Dari hasil konfigurasi tersebut baru diputuskan apakah 
peserta berhasil mengkonfigurasi dan lolos atau tidak.

## Rumusan Masalah

Adapun rumusan masalah berdasarkan latar belakang diatas yaitu:
1. Bagaimana membuat CLI RouterOS dapat diakses melalui web?
1. Bagaimana cara mengintegrasikan GNS3 server dengan web?
1. Bagaimana cara mendapatkan konfigurasi setelah peserta selesai mengerjakan?
1. Bagaimana menilai hasil konfigurasi RouterOS peserta?

## Tujuan 
Adapun tujuan dalam penelitian ini adalah:
1. Membuat sistem pengujian konfigurasi RouterOS berbasis web.
1. Membuat sistem penilaian konfigurasi RouterOS.

<!-- use blackbox testing? -->

## Manfaat
Manfaat yang dapat dihasilkan dari penelitian ini antara lain:
1. Mendapatkan sebuah sistem pengujian konfigurasi RouterOS berbasis web.
2. Mempermudah pihak Mikrotik dan pihak ketiga penyelenggara sertifikasi 
dalam melaksanakan pengujian sertifikasi.
3. Mendapatkan sistem yang bisa diadaptasi bukan hanya untuk Mikrotik namun 
juga pihak lain yang membutuhkan sistem serupa.

## Batasan Masalah 
Adapun batasan masalah yang digunakan untuk menghindari penyimpangan dari 
judul dan tujuan adalah sebagai berikut ini:
1. Antarmuka yang digunakan peserta untuk mengkonfigurasi RouterOS adalah CLI 
_via_ web.
1. Penilaian diambil berdasarkan kecocokan konfigurasi dengan poin studi kasus 
yang diujikan.
1. Sistem yang digunakan untuk menjalankan RouterOS berbasis Virtualisasi yang
dijalankan dengan QEMU dalam topologi GNS3.
1. Data konfigurasi RouterOS dikirim menggunakan API yang disediakan oleh 
RouterOS
1. Dukungan untuk banyak pengguna, keamanan pengguna, serta keamanan sistem 
dari serangan luar tidak akan dibahas dalam penelitian ini.
1. Konfigurasi yang diujikan meliputi pengalamatan IP, dasar daftar alamat IP, _interface bridging_,
_interface comments_, _static routing_, _firewall filtering_ , dan NAT.

# BAB II - KAJIAN PUSTAKA

## Penelitian Terdahulu

Sebelumnya sudah ada penelitian terkait pelatihan teknisi untuk mengkonfigurasi 
router berbasis web yang ditulis oleh Novalino Reynaldi Anas berjudul "
 PERANCANGAN SISTEM INFORMASI UNTUK KONFIGURASI PERANGKAT JARINGAN BERBASIS WEB
: Studi Kasus PT. Indonesia Comnets Plus". Metode yang digunakan dalam 
pengujian adalah _blackbox testing_ dimana hanya menguji keberhasilan 
konfigurasi apakah berjalan sesuai ekspektasi. Tentu dalam penelitian tersebut 
sudah cukup untuk pengujian. Namun dalam pengujian tersebut digunakan router 
Mikrotik fisik yang tentu akan menjadi halangan ketika harus dilakukan 
pengujian seperti routing karena butuh beberapa router fisik sekaligus.
(A. Novalino Reynaldi, 2020).

Penelitian mengenai integrasi CLI router dengan GNS3 sebagai virtualisasi 
topologi jaringan pernah dilakukan oleh Elin Sylvania, Suroso, dan Irwan Hadi
dalam artikel yang berjudul "Pengujian Konfigurasi Otomatis Penambahan Gateway
Pada Virtual Router Menggunakan Aplikasi Otomatisasi Jaringan Berbasis Web" 
dimana konfigurasi dilakukan dengan memasukkan baris konfigurasi melalui 
_text input_ via web yang dibuat sendiri. Hasilnya konfigurasi penambahan 
gateway otomatis dapat dilakukan.


# BAB III - METODE PENELITIAN

Terdapat tahapan-tahapan yang masuk dalam metodologi penelitian sebagai 
pedoman agar tujuan utama dari penelitian ini tercapai dan tidak menyimpang
dari tujuan awal.

## Metode Penelitian
Metode penelitian yang digunakan adalah _waterfall_

