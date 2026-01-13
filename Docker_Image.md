## Docker Image

Menampilkan bantuan mengenai command-command yang dapat di gunakan untuk mengoperasikan docker `image` :

```bash
docker image --help
```

### List Image

Menampilkan list image yang sudah ada di local :

```bash
docker images
```

### Pull Image

mendownload image dari container registry :

```bash
docker pull [IMAGE]
```

Note :

1. `[IMAGE]` diisi dengan nama image yang tersedia di container registry.

### Image Tag

Membuat TAG baru untuk image yang sudah ada :

```bash
docker tag [IMAGE] [NAMA]
```

### Remove Image

Menghapus docker image yang ada di local :

```bash
docker rmi [IMAGE]
```

### Image Push

Mengupload image ke repository di container registry :

```bash
docker push [IMAGE]
```