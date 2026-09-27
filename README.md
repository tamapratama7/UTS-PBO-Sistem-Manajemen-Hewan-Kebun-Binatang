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
- `controller` : berisi kelas `PengelolaHewan` (logika CRUD) dan `Validator` (validasi input)
- `view` : berisi kelas `Main` (antarmuka console/menu program)

## Alur Program  

### Cara Kerja Sistem

Saat program dijalankan, pengguna akan ditampilkan dengan menu utama berupa daftar pilihan (1–5). Program akan terus menampilkan menu ini secara berulang (looping) sampai pengguna memilih opsi **Keluar**.  

**1. Tambah Data Hewan**
- Pengguna memasukkan ID, nama, jenis, umur, dan habitat hewan
- Program memvalidasi apakah ID sudah dipakai sebelumnya
- Pengguna memilih kategori hewan (Darat/Air), lalu mengisi atribut khusus sesuai kategori
- Pengguna mengisi data perawatan (ID perawatan, jenis, tanggal)
- Program memvalidasi format tanggal dan keunikan ID perawatan sebelum data disimpan

**2. Lihat Data Hewan**
Program menampilkan seluruh data hewan yang tersimpan, lengkap dengan info tambahan sesuai kategorinya (kecepatan lari untuk hewan darat, kedalaman renang untuk hewan air)  

**3. Ubah Data Hewan**
- Pengguna memasukkan ID hewan yang ingin diubah
- Program mencari data berdasarkan ID, lalu meminta input data baru (nama, jenis, umur, habitat, atribut khusus, dan data perawatan baru)
- Data akan diperbarui jika seluruh validasi terpenuhi

**4. Hapus Data Hewan**
- Pengguna memasukkan ID hewan yang ingin dihapus
- Program mencari dan menghapus data jika ID ditemukan

**5. Keluar**
- Program berhenti berjalan (loop menu berhenti)

Semua input angka (ID, umur, nilai desimal) divalidasi melalui kelas `Validator` agar program tidak crash saat menerima input yang tidak sesuai format.  

## Demo Program 
### 1. Tampilan Menu Utama 
<p align="center">
  <img width="447" height="241" alt="image" src="https://github.com/user-attachments/assets/5eee379c-1f35-455c-a1ad-1a92a852a006" />
</p>

Menampilkan daftar pilihan menu (1. Tambah, 2. Lihat, 3. Ubah, 4. Hapus, 5. Keluar) saat program pertama kali dijalankan.

### 2. Tambah Data Hewan  
<p align="center">
  <img width="491" height="652" alt="image" src="https://github.com/user-attachments/assets/a972a3a7-7dfc-439c-ae96-eb4f1bb903b3" />
</p>

Menampilkan proses input data hewan baru beserta data perawatannya, termasuk validasi ID yang sudah dipakai.  

### 3. Lihat Data Hewan  
<p align="center">  
  <img width="601" height="980" alt="image" src="https://github.com/user-attachments/assets/387cd8c1-5423-44f8-8b16-81bfd26533ea" />
</p>

Menampilkan seluruh data hewan yang tersimpan, termasuk info tambahan sesuai kategori (darat/air).

### 4. Ubah Data Hewan  
<p align="center">   
  <img width="498" height="478" alt="image" src="https://github.com/user-attachments/assets/155dfa03-a960-401f-97ee-4f7ef6494bac" />
</p>

Menampilkan proses pencarian data berdasarkan ID dan pembaruan data hewan.

### 5. Hapus Data Hewan  
<p align="center">   
  <img width="357" height="300" alt="image" src="https://github.com/user-attachments/assets/9ff566e4-72bb-4b0a-86ec-4afd1845d000" />
</p>  

Menampilkan proses penghapusan data hewan berdasarkan ID.  

### 5. Keluar
<p align="center"> 
  <img width="591" height="282" alt="image" src="https://github.com/user-attachments/assets/648f52e2-53ae-44ef-a92c-dcf639bfaf65" />
</p>  

Program selesai.
