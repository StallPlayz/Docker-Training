## Docker Network

Menampilkan list Network yang sudah ada di local :

```bash
docker network ls
```

Note :

1. Ada beberapa jenis network :
```markdown
    - Bridge : Default network driver.
    - Host : Menghapus isolasi antara container dan host.
    - None : Mengisolasi penuh antara container lain dengan host.
    - Overlay : Menghubungkan antar docker host.
    - IPVLAN : Menyediakan control penuh terhadap IPv4 & IPv6.
    -MACVLAN : Memberikan MAC address pada container.
```

Menampilkan bantuan mengenai command-command yang dapat dioperasikan dengan docker `network` :

```bash
docker network --help
```

### Docker Network Create

Menampilkan bantuan mengenai command-command yang dapat dioperasikan dengan docker `network create` :

```bash
docker network create --help
```

Membuat network baru di dalam docker :

```bash
docker network create [NAMA_JARINGAN]
```

bisa juga di spesifikasikan subnet nya :

```bash
docker network create [NAMA_JARINGAN] --subnet 10.1.0.0/20
```

Note :

1. `[NAMA_JARINGAN]` diisi dengan nama yang ingin di gunakan untuk menamai jaringan yang akan di tambahkan.

### Docker Network Connect

Menghubungkan network yang sudah di buat dengan sebuah container :

```bash
docker network connect [NAMA_JARINGAN] [NAMA_CONTAINER] / [ID]
```

Adapun kita dapat menspesifikasikan network di awal pembuatan container :

```bash
docker run -d --name [NAMA_CONTAINER] --network [NAMA_JARINGAN] [IMAGE]
```

Note :

1. ini membuat container akan langsung tehubung ke network yang telah di berikan, tanpa ter koneksi ke network type biasa.

### Port Mapping

Melakukan port mapping pada container yang baru di buat :

```bash
docker run -d --name [NAMA_CONTAINER] -p [PORT]:80 [IMAGE]
```

Note :

1. `-p` untuk melakukan publish.
2. `[PORT]` diisi dengan port yang ingin di gunakan, contoh nya 8081:80.