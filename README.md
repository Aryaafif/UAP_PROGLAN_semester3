# Penjelasan Class dalam Aplikasi Pemesanan Villa

## 1. `LoginBooking`

### Fungsi Utama:
- Berfungsi sebagai halaman login aplikasi.
- Melakukan validasi username dan password sebelum mengizinkan pengguna mengakses aplikasi.

### Detail Fungsi:
- **Validasi Login:**
  - Memeriksa apakah username dan password sesuai dengan data yang telah ditentukan:
    - Username: `villa arya`
    - Password: `murahbanget`.
  - Jika validasi berhasil, pengguna diarahkan ke halaman **HomeBooking**.
  - Jika gagal, akan menampilkan pesan kesalahan.
- **Komponen Antarmuka:**
  - **JTextField** untuk input username.
  - **JPasswordField** untuk input password.
  - **JButton (Submit):** Memicu proses login.

### Alur Kerja:
1. Pengguna memasukkan username dan password.
2. Sistem memvalidasi input dengan data yang ada.
3. Jika validasi berhasil, sistem mengarahkan ke halaman utama.
4. Jika gagal, pesan kesalahan akan ditampilkan.

---

## 2. `FormBooking`

### Fungsi Utama:
- Halaman utama untuk memasukkan detail pemesanan villa.
- Menampilkan informasi tamu dan menyediakan tabel untuk memasukkan detail pemesanan.

### Detail Fungsi:
- **Input Data Pemesanan:**
  - **JTable:** Untuk memasukkan informasi seperti jenis villa, tanggal check-in, jumlah hari, harga per malam, dan subtotal.
  - **TxtTotal:** Menampilkan total biaya pemesanan.
- **Menampilkan Informasi Tamu:**
  - Method `setData()` digunakan untuk menampilkan nama dan nomor telepon tamu yang dimasukkan sebelumnya.
  - Informasi tamu ditampilkan menggunakan **JLabel**.

### Alur Kerja:
1. Pengguna memasukkan informasi tamu (nama, telepon).
2. Pengguna menambahkan detail pemesanan ke tabel.
3. Sistem menghitung total biaya dan menampilkannya.

---

## 3. Halaman Booking (Ringkasan Pemesanan)

### Fungsi Utama:
- Menampilkan ringkasan dari data pemesanan sebelum proses pembayaran dilakukan.
- Memastikan semua data sudah benar sebelum konfirmasi.

### Detail Fungsi:
- **Ringkasan Pemesanan:**
  - Menampilkan informasi seperti nama tamu, jenis villa, tanggal check-in, durasi menginap, harga per malam, subtotal, dan total biaya.
  - Informasi ditampilkan dalam format tabel dan label untuk memudahkan pengguna melakukan pengecekan.
- **Konfirmasi:**
  - Halaman ini menyediakan tombol konfirmasi untuk melanjutkan ke proses pembayaran.

### Alur Kerja:
1. Data dari `FormBooking` diambil dan ditampilkan.
2. Pengguna memverifikasi data yang ditampilkan.
3. Pengguna mengklik tombol konfirmasi untuk melanjutkan.

---

## 4. `HomeBooking`

### Fungsi Utama:
- Berfungsi sebagai halaman utama setelah login.
- Menyediakan navigasi ke fitur utama aplikasi seperti pemesanan atau logout.

### Detail Fungsi:
- **Navigasi ke FormBooking:**
  - Mengarahkan pengguna ke halaman **FormBooking** untuk memulai proses pemesanan baru.
- **Logout:**
  - Mengembalikan pengguna ke halaman **LoginBooking** untuk keluar dari sistem.

### Alur Kerja:
1. Setelah login, pengguna diarahkan ke halaman ini.
2. Pengguna dapat memilih untuk:
   - Membuat pemesanan baru (FormBooking).
   - Logout untuk keluar dari aplikasi.

---

## Alur Utama Aplikasi:
1. **LoginBooking:** Verifikasi username dan password.
2. **HomeBooking:** Halaman beranda utama setelah login.
3. **FormBooking:** Halaman untuk memasukkan detail pemesanan.
4. **Halaman Booking:** Ringkasan pemesanan sebelum pembayaran.

Setiap class memiliki perannya masing-masing untuk memastikan aplikasi berjalan dengan baik dan alur kerja dapat diikuti oleh pengguna dengan mudah.

