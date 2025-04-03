# _NixOS Cloud VPS Deployment_ Berbasis Web dengan Proxmox dan _Shell Scripting_

> Disusun oleh : M. Rizqi R 

## PENDAHULUAN

### Latar Belakang
Dalam beberapa tahun ini, sistem operasi berbasis GNU/Linux, yaitu NixOS mulai
naik daun. Sistem operasi ini dikenal dengan fiturnya yaitu pendeklarasian
sistem operasi dalam konfigurasi yang absolut. Sistem konfigurasi NixOS
membuatnya dapat di deploy secara berulang dan dipastikan hasilnya satu banding
satu dengan yang lain. Ini sangat cocok digunakan apabila kita ingin melakukan
deployment yang sama secara berulang dan membuatnya cocok dijadikan sebagai
sistem operasi untuk server. 

Namun sangat disayangkan bahwa hanya sedikit penyedia layanan cloud Virtual
Private Server (VPS) yang memberikan opsi NixOS sebagai bagian dari layanan
mereka. Tentu hal ini bisa diatasi dengan nixos-anywhere yang dapat mengubah
distribusi GNU/Linux apapun menjadi NixOS dengan media kexec untuk memulai
NixOS installer. Cara kedua adalah dengan mengunggah _custom image_ berisikan
NixOS, namun tidak semua penyedia layanan berbasis _cloud_ mendukung cara ini.





