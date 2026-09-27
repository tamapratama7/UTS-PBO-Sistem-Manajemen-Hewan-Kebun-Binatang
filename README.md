# UTS PBO Sistem Manajemen Hewan Kebun Binatang   
## Deskripsi Proyek  
Program ini digunakan untuk mencatat, menampilkan, mengubah, dan menghapus data hewan beserta riwayat perawatannya di kebun binatang. Setiap hewan dikategorikan menjadi dua jenis:  
- **Hewan Darat** — memiliki atribut tambahan berupa kecepatan lari (km/jam)  
- **Hewan Air** — memiliki atribut tambahan berupa kedalaman renang maksimal (meter)
  
Setiap data hewan juga dilengkapi dengan data **Perawatan Hewan** (ID perawatan, jenis perawatan, dan tanggal perawatan), sehingga riwayat kesehatan/perawatan setiap hewan dapat terekam dengan baik.

Fitur utama program:
1. **Tambah Data Hewan** : menambahkan hewan baru beserta data perawatannya
2. **Lihat Data Hewan** : menampilkan seluruh data hewan yang tersimpan
3. **Ubah Data Hewan** : memperbarui data hewan dan data perawatan berdasarkan ID
4. **Hapus Data Hewan** : menghapus data hewan berdasarkan ID
5. **Keluar** : mengakhiri program

Struktur kode dibagi ke dalam beberapa package agar rapi dan mudah dipelihara:
- `model` : berisi kelas `Hewan`, `HewanDarat`, `HewanAir`, `PerawatanHewan`
- `service` : berisi kelas `PengelolaHewan` (logika CRUD) dan `Validator` (validasi input)
- `view` : berisi kelas `Main` (antarmuka console/menu program)
