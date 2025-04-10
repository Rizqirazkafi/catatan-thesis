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



