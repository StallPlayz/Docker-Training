## Basic Command CLI

Menampilkan semua bantuan mengenai command-command untuk mengakses dan menjalankan container dari docker :

```bash
docker --help
```

Mendownload image dari container registry dengan `docker pull` :

```bash
docker pull nginx:latest
```

Menampilkan list container yang sedang running (berjalan) :

```bash
docker ps
```

Menampilkan daftar image yang sudah ada di local :

```bash
docker images
```

Menampilkan daftar network yang sudah ada di local :

```bash
docker network ls
```

Menampilkan daftar volume yang sudah ada di local :

```bash
docker volume ls
```