## Menjalankan Docker

Membuat dan menjalankan sebuah container :

```bash
docker run [OPTIONS] [IMAGE] [COMMAND] [ARG...]
```

Note :
1. `[OPTIONS]` diisi dengan opsi tambahan seperti nama, konfigurasi, network, volume, dll.
2. `[IMAGE]` diisi dengan nama image yang akan digunakan, contoh : `nginx`.
3. `[COMMAND]` dan `[ARG...]` diisi dengan perintah atau argumen tambahan yang bersifat opsional.

Untuk menjalankan container di belakang layar :

```bash
docker run -d --name [NAMA_CONTAINER] [IMAGE]
```

Note :
1. `-d (detach)` memungkinkan container berjalan di belakang layar (agar tidak memenuhi CLI dan bisa menggunakan CLI setelah running Image).
2. `--name` digunakan untuk memberi nama pada container yang dijalankan.
3. gunakan `docker run --help` untuk mencari tahu opsi-opsi lainnya yang dapat digunakan dalam command line ini.