# Test Case – HelpCenter

Skenario di bawah ini disusun dari fitur utama HelpCenter. Kolom **Actual Result** dan **Status** diisi dari hasil pengujian yang benar-benar dijalankan.

**Keterangan status:** `PASS` | `FAIL` | `BLOCKED` | `NOT TESTED`

---

## A. Autentikasi

### TC-001 – Login dengan data yang benar
- **Precondition:** User sudah memiliki akun.
- **Test Data:** Email dan password valid.
- **Steps:**
  1. Buka halaman login.
  2. Masukkan email terdaftar.
  3. Masukkan password yang benar.
  4. Klik tombol Login.
- **Expected Result:** User berhasil masuk dan diarahkan ke dashboard.
- **Actual Result:** [isi]
- **Status:** [PASS / FAIL]

### TC-002 – Login dengan password salah
- **Test Data:** Email valid, password salah.
- **Steps:**
  1. Buka halaman login.
  2. Masukkan email terdaftar dan password yang salah.
  3. Klik tombol Login.
- **Expected Result:** Login ditolak dan muncul pesan kesalahan yang jelas.
- **Actual Result:** [isi]
- **Status:** [PASS / FAIL]

### TC-003 – Login dengan field kosong
- **Steps:**
  1. Buka halaman login.
  2. Kosongkan email dan password.
  3. Klik tombol Login.
- **Expected Result:** Muncul pesan validasi bahwa field wajib diisi.
- **Actual Result:** [isi]
- **Status:** [PASS / FAIL]

---

## B. Tiket Laporan

### TC-004 – Membuat tiket dengan data lengkap
- **Precondition:** User sudah login.
- **Steps:**
  1. Buka menu pembuatan tiket.
  2. Isi judul, kategori, dan deskripsi.
  3. Kirim tiket.
- **Expected Result:** Tiket berhasil dibuat dan muncul di daftar tiket dengan status awal yang benar.
- **Actual Result:** [isi]
- **Status:** [PASS / FAIL]

### TC-005 – Membuat tiket dengan deskripsi kosong
- **Steps:**
  1. Buka menu pembuatan tiket.
  2. Isi judul dan kategori, kosongkan deskripsi.
  3. Kirim tiket.
- **Expected Result:** Tiket tidak tersimpan dan muncul pesan bahwa deskripsi wajib diisi.
- **Actual Result:** [isi]
- **Status:** [PASS / FAIL]

### TC-006 – Melihat detail tiket
- **Steps:**
  1. Buka daftar tiket.
  2. Klik salah satu tiket.
- **Expected Result:** Detail tiket tampil sesuai data yang diinput.
- **Actual Result:** [isi]
- **Status:** [PASS / FAIL]

---

## C. Penanganan Tiket

### TC-007 – Penugasan vendor pada tiket
- **Precondition:** Ada tiket berstatus baru, login sebagai peran yang berhak.
- **Steps:**
  1. Buka detail tiket.
  2. Pilih vendor dan simpan penugasan.
- **Expected Result:** Vendor tercatat pada tiket dan perubahan terlihat di detail tiket.
- **Actual Result:** [isi]
- **Status:** [PASS / FAIL]

### TC-008 – Mengubah status tiket hingga selesai
- **Steps:**
  1. Buka detail tiket.
  2. Ubah status secara berurutan sampai selesai.
- **Expected Result:** Status berubah sesuai alur dan tersimpan setelah halaman dimuat ulang.
- **Actual Result:** [isi]
- **Status:** [PASS / FAIL]

---

## D. API dan Database

### TC-009 – GET daftar tiket lewat Postman
- **Steps:**
  1. Kirim request GET ke endpoint daftar tiket dengan token yang valid.
- **Expected Result:** Status 200 dan data tiket sesuai format.
- **Actual Result:** [isi]
- **Status:** [PASS / FAIL]

### TC-010 – Request API tanpa token
- **Steps:**
  1. Kirim request ke endpoint yang sama tanpa token.
- **Expected Result:** Status 401 (unauthorized) dan tidak ada data yang dikembalikan.
- **Actual Result:** [isi]
- **Status:** [PASS / FAIL]

### TC-011 – Validasi data tiket di database
- **Steps:**
  1. Buat tiket lewat aplikasi.
  2. Jalankan `SELECT` pada tabel tiket di MySQL.
- **Expected Result:** Data di database sama dengan data yang diinput di aplikasi.
- **Actual Result:** [isi]
- **Status:** [PASS / FAIL]
