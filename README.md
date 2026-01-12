# 🗳️ E-Voting System

E-Voting System adalah aplikasi web berbasis Laravel yang dirancang untuk memfasilitasi proses pemilihan secara digital dengan aman, terstruktur, dan mudah digunakan. Aplikasi ini menerapkan **role-based access control**, di mana setiap pengguna memiliki hak akses sesuai perannya, yaitu **Admin** dan **Voter**.

Sistem ini memungkinkan admin untuk mengelola kandidat dan memantau hasil voting secara real-time melalui dashboard interaktif, sementara voter dapat melakukan voting secara aman dengan ketentuan **satu orang satu suara**.

Aplikasi ini dikembangkan sebagai bagian dari project pembelajaran dan portofolio, dengan fokus pada implementasi logika bisnis, keamanan akses, serta visualisasi data hasil voting.

---

## ✨ Fitur Utama

### 👤 Admin
- Halaman Login
  <img width="1920" height="827" alt="screencapture-127-0-0-1-8000-login-2026-01-12-14_17_44" src="https://github.com/user-attachments/assets/6209a78d-3af2-44b7-96de-911b750b2adb" />
---

- Dashboard statistik voting
  <img width="1920" height="941" alt="screencapture-127-0-0-1-8000-app-dashboard-2026-01-12-14_51_54" src="https://github.com/user-attachments/assets/3325a9e9-9529-42e6-99c2-c9123bf38916" />
  <img width="1920" height="941" alt="screencapture-127-0-0-1-8000-app-dashboard-2026-01-12-15_05_35" src="https://github.com/user-attachments/assets/5214e631-db54-411f-9eec-7d57fabdaaeb" />

---

- Manajemen kandidat
  <img width="1920" height="948" alt="screencapture-127-0-0-1-8000-app-candidate-2026-01-12-14_53_36" src="https://github.com/user-attachments/assets/0e48a943-822d-4c56-bfad-ab6de10cb2ac" />
---

- Manajemen voter
  <img width="1920" height="827" alt="screencapture-127-0-0-1-8000-app-voter-2026-01-12-14_54_31" src="https://github.com/user-attachments/assets/44a3f8ef-7e3f-4207-b2c9-e4b2c8a7fe5b" />
---

- Manajemen user, role, dan permission
<img width="1920" height="993" alt="screencapture-127-0-0-1-8000-app-user-2026-01-12-14_55_24" src="https://github.com/user-attachments/assets/6e4ca740-0c64-4569-8095-bd3e6670ccf5" />
<img width="1920" height="827" alt="screencapture-127-0-0-1-8000-app-role-2026-01-12-14_56_21" src="https://github.com/user-attachments/assets/dcae5abb-037c-4142-8f8d-ed36f34df955" />


### 🗳️ Voter
- Login sebagai voter
  <img width="1920" height="827" alt="screencapture-127-0-0-1-8000-login-2026-01-12-15_02_28" src="https://github.com/user-attachments/assets/335c91ac-f921-4dc7-8cfe-8be00dab69ef" />
---

- Melihat daftar kandidat
  <img width="1920" height="1083" alt="screencapture-127-0-0-1-8000-app-dashboard-2026-01-12-14_58_07" src="https://github.com/user-attachments/assets/bb2e08a1-33a2-4096-86d0-98aeaf71f8dd" />
---

- Melakukan voting satu kali dan Status voting (Already Voted) juga Validasi otomatis untuk mencegah double voting
<img width="1920" height="1149" alt="screencapture-127-0-0-1-8000-app-dashboard-2026-01-12-14_58_48" src="https://github.com/user-attachments/assets/ab2e7397-03e9-43ce-9393-fec103b814f9" />

---

## 📌 Alur Penggunaan Aplikasi E-Voting

Aplikasi E-Voting ini memiliki dua peran utama, yaitu **Admin** dan **Voter**, dengan alur penggunaan yang berbeda sesuai dengan hak akses masing-masing.

---

## 👤 1. Alur Penggunaan sebagai Admin

Admin bertugas mengelola data dan memantau jalannya proses voting.

### 🔐 Login Admin
1. Admin mengakses halaman login.
2. Admin melakukan login menggunakan akun dengan role **admin**.
3. Setelah login berhasil, admin diarahkan ke **Dashboard Admin**.

### 📊 Dashboard Admin
Pada dashboard admin, sistem menampilkan:
- Total jumlah voter
- Total jumlah kandidat
- Total suara masuk
- Jumlah voter yang belum memilih
- Grafik perolehan suara tiap kandidat (Bar Chart & Pie Chart)

### 🗂️ Manajemen Data
Admin dapat melakukan:
- Pengelolaan data kandidat (tambah, edit, hapus)
- Pengelolaan data voter
- Pengelolaan user dan role
- Pengaturan permission menggunakan **role-based access control**
- admin@app.com (password)

### 📈 Monitoring Voting
- Admin dapat memantau hasil voting secara **real-time**
- Data suara akan otomatis terupdate setelah voter melakukan voting

---

## 🗳️ 2. Alur Penggunaan sebagai Voter

Voter hanya memiliki akses untuk melakukan voting **satu kali**.

### 🔐 Login Voter
1. Voter mengakses halaman login.
2. Voter melakukan login menggunakan akun dengan role **voter**.
3. Setelah login berhasil, voter diarahkan ke **Dashboard Voter**.

### 📋 Dashboard Voter
Pada dashboard voter, sistem menampilkan:
- Daftar kandidat yang tersedia
- Informasi kandidat (nama, ketua, wakil, visi, dan misi)
- Tombol **Vote** untuk memilih kandidat

### ✅ Proses Voting
1. Voter memilih satu kandidat dengan menekan tombol **Vote**.
2. Sistem memvalidasi bahwa voter **belum pernah melakukan voting**.
3. Jika valid, suara akan disimpan ke dalam sistem.
4. Voter diarahkan kembali ke dashboard dengan notifikasi berhasil.

### 🔒 Pembatasan Voting
- Setiap voter **hanya dapat melakukan voting satu kali**
- Setelah voting, tombol **Vote** akan berubah menjadi **Already Voted**
- Voter tidak dapat melakukan voting ulang

---

## 🔐 Keamanan Sistem
- Role & Permission menggunakan **Spatie Laravel Permission**
- Pembatasan akses berdasarkan peran pengguna
- Validasi satu suara untuk satu voter
- Dashboard dinamis sesuai role (Admin / Voter)

---

## 🛠️ Teknologi yang Digunakan
- **Laravel**
- **MySQL**
- **SB Admin 2**
- **Chart.js**
- **Spatie Laravel Permission**

---

## 🎯 Tujuan Pengembangan
Aplikasi ini dikembangkan untuk mensimulasikan sistem e-voting yang sederhana namun fungsional, dengan pemisahan peran yang jelas antara admin dan voter, serta menekankan pada keamanan data dan kemudahan penggunaan.

---

> 📌 **Catatan:**  
> Proyek ini ditujukan untuk keperluan pembelajaran dan portofolio, serta dapat dikembangkan lebih lanjut sesuai kebutuhan.
