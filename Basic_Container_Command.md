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
docker start [NAMA_CONTAINER] / [ID]

/

docker container start [NAMA_CONTAINER] / [ID]
```

Note :
1. `[NAMA]` dan `[ID]` dapat dipilih salah satu, diisi dengan nama atau ID dari container yang telah dimatikan.

Mematikan container yang sedang berjalan :

```bash
docker stop [NAMA_CONTAINER] / [ID]
```

Note :
1. jika menyalakan container dengan mode attach (tidak dapat berjalan di belakang layar), dapat melakukan terminasi dalam CLI yang sebelumnya digunakan untuk menyalakan container.

### Inspect container

Menampilkan informasi detail dari container yang di pilih :

```bash
docker inspect [NAMA_CONTAINER] / [ID]
```

#### Log container

Menampilkan log dari container yang di pilih :

```bash
docker logs [NAMA_CONTAINER] / [ID]
```

### Exec Container

Menjalankan suatu perintah di dalam sebuah container yang dipilih :

```bash
docker exec [NAMA_CONTAINER] / [ID] [PERINTAH]
```

Contoh nya seperti :

```bash
docker exec [NAMA_CONTAINER] / [ID] hostname

/

docker exec [NAMA_CONTAINER] / [ID] env

/

docker exec [NAMA_CONTAINER] / [ID] ls -l /
```

Masuk kedalam container dengan mode interaktif seperti remote SSH pada virtual machine :

```bash
docker exec -it [NAMA_CONTAINER] / [ID] bash
```

Note :
1. `ls -l /` merupakan command linux untuk membuka root directory.