# Chatbot Akademik untuk Mahasiswa

## Elevator Pitch
Sebuah chatbot akademik sederhana yang dapat menjawab pertanyaan seputar jadwal kuliah mahasiswa, seperti mata kuliah, SKS, dosen, ruangan, dan hari. Sistem ini membantu mahasiswa mendapatkan informasi dengan cepat (<5 detik) dan akurat (≥80%), dibandingkan cara manual melalui grup WhatsApp atau bertanya langsung ke teman.

## Problem Statement
Mahasiswa sering kesulitan mencari informasi terkait jadwal kuliah, seperti mata kuliah apa yang diambil, jumlah SKS, siapa dosennya, di ruangan mana, dan pada hari apa. Saat ini, sebagian besar mahasiswa masih mengandalkan grup WhatsApp atau bertanya langsung ke teman, yang memakan waktu lama, tidak praktis, dan rawan miskomunikasi.  
**Nilai bagi pengguna**: akses informasi akademik lebih cepat, akurat, dan efisien.  
**Nilai bagi institusi**: mengurangi beban administrasi manual dan meningkatkan kepuasan mahasiswa.

## Scope
**In-Scope:**
- Pertanyaan tentang jadwal kuliah per prodi.  
- Informasi mata kuliah, dosen, SKS, ruangan, dan hari.  
- Implementasi prototipe chatbot sederhana berbasis dataset statis.  

**Out-of-Scope:**
- Perubahan jadwal mendadak (belum real-time).  
- Informasi administrasi non-jadwal (misalnya keuangan kampus/UKT).  
- Data pribadi mahasiswa.  

## Metrik
- **Baseline:** mahasiswa mendapat jawaban via WA/teman, ±5–10 menit.  
- **Target:** chatbot menjawab otomatis <5 detik dengan akurasi ≥80%.  
- **Evaluasi:**  
  - Accuracy ≥ 0.8 (80%)  
  - Latensi p95 ≤ 5 detik  

## Data
- Dataset dummy dibuat berdasarkan struktur jadwal perkuliahan resmi yang dikeluarkan oleh pihak akademik.  
- Data mencakup: hari, jam, semester, group, ruang, mata kuliah, SKS, dosen, dan prodi.  
- **Lisensi & privasi:** hanya menggunakan data publik (jadwal perkuliahan), tidak ada data pribadi mahasiswa.  
- Data asli bersifat internal, sehingga versi dummy digunakan untuk eksplorasi awal.  

## Arsitektur
Alur sistem chatbot:  
Input pertanyaan mahasiswa
↓
Preprocessing (ekstraksi kata kunci)
↓
Query dataset jadwal
↓
Output jawaban terstruktur


## Struktur Repository
- `README.md` → dokumentasi utama proyek.  
- `notebooks/` → berisi notebook eksplorasi dataset dummy.  
- `src/` → kode chatbot.  
- `issues board` → manajemen To Do / In Progress / Done (≥5 issue).  

## Link GitHub
[Repository GitHub](https://github.com/Syzafid/chatbot-jadwal-akademik)  

## Roadmap
- M1: Definisi masalah, setup, dummy notebook.  
- M2: Buat dataset jadwal dummy.  
- M3: Implementasi query sederhana.  
- M4: Integrasi chatbot CLI.  
- M5: Evaluasi response time & accuracy.  
- M6: Dokumentasi & laporan akhir.  

## Etika & Privasi
Risiko: chatbot bisa memberikan jawaban salah atau jadwal tidak ter-update, sehingga mahasiswa berpotensi salah masuk kelas. Risiko lain adalah kebocoran data internal kampus.  
Mitigasi: chatbot selalu menyertakan sumber data resmi prodi, dilakukan update berkala, dan hanya menggunakan dataset publik (tanpa data pribadi mahasiswa). Dengan demikian, risiko kesalahan dan privasi dapat diminimalkan.  


