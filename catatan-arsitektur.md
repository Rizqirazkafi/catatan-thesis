1. Saat testing, konfigurasi dilakukan seperti biasa dengan ada interface yang menghadap ke API Server aplikasi yang tidak boleh di interupt accessnya
1. Ketika konfigurasi menggunakan DHCP pada PC A & B, maka peserta wajib mencantumkan alamat IP dan harus mengaktifkan DHCP reservation
1. Membuat bash script untuk menguji rute dari PC A ke PC B
1. Pengujian pertama dilakukan dengan path Router B ke Router D
1. Path Router B ke Router D akan diputus dengan menonaktifkan status port Router B yang menuju Router D
1. API menunggu beberapa detik kemudian menguji kembali rute  dari PC A ke PC B
1. Port Router B ke Router D akan diaktifkan kembali dan diuji kembali
1. API Server aplikasi akan meminta konfigurasi semua router kemudian di analisis menggunakan metode API Checking
