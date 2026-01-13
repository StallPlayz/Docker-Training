## Docker Volume

Menampilkan bantuan mengenai command-command yang dapat dioperasikan dengan docker `volume` :

```bash
docker volume --help
```

### Menggunakan Volume

Membuat volume baru :

```bash
docker volume create [NAMA_CONTAINER]
```

Menyambungkan volume pada container yang baru di buat pertama kali :

```bash
docker run -d --name [NAMA_CONTAINER] -v [NAMA_VOLUME]:/[LOKASI] [IMAGE]
```

Note :

1. `[NAMA_VOLUME]` diisi dengan nama volume yang telah dibuat sebelumnya.
2. `[LOKASI]` diisi dengan nama lokasi / path yang ingin di tambahkan di dalam container.
3. jika lebih dari 1 container menggunakan volume yang sama, maka akan terjadi yang namanya `sharing data`.

Melakukan Pengujian pada volume yang baru saja di sambungkan ke dalam sebuah container :

```bash
docker exec [NAMA_CONTAINER] ls -l /
```

Bisa juga melakukan tes mendalam dengan command berikut :

```bash
docker exec -it [NAMA_CONTAINER] bash

cd [NAMA_VOLUME]

ls -l

touch [NAMA_FILE.JENIS_FILE]

ls -l

exit

rm -f [NAMA_CONTAINER]
```

Note :

1. Lakukan sequence di atas untuk mengetahui apakah volume benar-benar sudah terkoneksi dan apakah file benar-benar tersimpan di dalam volume setelah penghapusan container.