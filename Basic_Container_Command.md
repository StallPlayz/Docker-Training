## Operasi dasar container

Menampilkan semua bantuan mengenai command-command yang dapat digunakan untuk mengoperasikan `Container` :

```bash
docker container --help
```

Menampilkan list container yang sedang running (berjalan) maupun stopped (Terhenti) :

```bash
docker ps -a
```
### Management container

Menyalakan kembali container yang telah dimatikan :

```bash
docker start [NAMA] / [ID]

/

docker container start [NAMA] / [ID]
```

Note :
1. `[NAMA]` dan `[ID]` dapat dipilih salah satu, diisi dengan nama atau ID dari container yang telah dimatikan.

Mematikan container yang sedang berjalan :

```bash
docker stop [NAMA] / [ID]
```

Note :
1. jika menyalakan container dengan mode attach (tidak dapat berjalan di belakang layar), dapat melakukan terminasi dalam CLI yang sebelumnya digunakan untuk menyalakan container.

### Inspect container

Menampilkan informasi detail dari container yang di pilih :

```bash
docker inspect [NAMA] / [ID]
```

#### Log container

Menampilkan log dari container yang di pilih :

```bash
docker logs [NAMA] / [ID]
```

### Exec Container

Menjalankan suatu perintah di dalam sebuah container yang dipilih :

```bash
docker exec [NAMA] / [ID] [PERINTAH]
```

Contoh nya seperti :

```bash
docker exec [NAMA] / [ID] hostname

/

docker exec [NAMA] / [ID] env

/

docker exec [NAMA] / [ID] ls -l /
```

Masuk kedalam container dengan mode interaktif seperti remote SSH pada virtual machine :

```bash
docker exec -it [NAMA] / [ID] bash
```

Note :
1. `ls -l /` merupakan command linux untuk membuka root directory.