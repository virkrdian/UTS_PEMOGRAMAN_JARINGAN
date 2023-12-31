UTS-Pemograman-Jaringan
Ini adalah Tugas Pemograman Jaringan dari kelompok yang ber anggotakan Virki Fardian (362201022) , Raden Hasan (362201019), Muhammad Rahmadika (362201024).
 dua program ini dibuat: 


-Program Server :Virki Fardian Nur Rohman (362201022) 


-Program Client :Raden Hasan RR (362201019) 


-Membuat kata-kata presentasi maupun yang ada di Github : Muhammad Rahmadika (362201024) dan Virki F N R (362201022)

Tentu, berikut adalah langkah-langkah umum untuk membuka program dari GitHub:

Unduh dan Instal Git:

Pastikan Git telah diinstal di komputer\Laptop Anda. Anda dapat mengunduhnya dari situs resmi Git dan mengikuti instruksi instalasinya.
Dapatkan URL Repositori GitHub:

Kunjungi halaman repositori GitHub yang berisi program yang ingin Anda unduh.
Klik tombol "Code" atau "Clone" dan salin URL repositori.
Buka Terminal atau Command Prompt:

Buka terminal atau command prompt di komputer Anda.
Pilih Lokasi Penyimpanan:

Pindah ke direktori atau lokasi di mana Anda ingin menyimpan program GitHub tersebut dengan menggunakan perintah cd.

cd path/to/directory
Klon Repositori:

Gunakan perintah git clone untuk mengunduh repositori ke komputer Anda.

git clone <URL Repositori GitHub>
Gantilah <URL Repositori GitHub> dengan URL yang telah Anda salin sebelumnya.

Buka Proyek:

Setelah proses pengunduhan selesai, pindah ke direktori repositori yang baru dibuat.

cd nama-repositori
Buka dengan IDE atau Editor Kode:

Buka proyek menggunakan Integrated Development Environment (IDE) atau editor kode seperti IntelliJ IDEA, Eclipse, atau Visual Studio Code.
Jalankan atau Modifikasi Program:

Jika proyek memiliki instruksi khusus untuk konfigurasi atau instalasi dependensi, ikuti petunjuk tersebut.
Buka dan jalankan program sesuai dengan instruksi proyek.
Dengan mengikuti langkah-langkah ini, Anda seharusnya dapat mengunduh, membuka, dan menjalankan program yang ada di GitHub.




Program transfer file enkripsi ini adalah aplikasi sederhana yang menggunakan socket untuk mengirim file dari klien (client) ke server. Namun, sebelum file dikirim, program melakukan proses enkripsi terlebih dahulu menggunakan algoritma enkripsi AES (Advanced Encryption Standard).

Langkah-langkah yang terjadi dalam program transfer file enkripsi ini adalah sebagai berikut:

1. **Inisialisasi Koneksi:**
   - Klien membuat socket untuk terhubung ke server yang berjalan pada localhost dan port tertentu (dalam contoh ini, port 12312).

2. **Pengiriman File:**
   - Klien membaca file yang akan dikirim (dalam contoh ini, `file_to_send.txt`) ke dalam buffer dan mengirimnya melalui koneksi socket ke server menggunakan OutputStream.
  
3. **Enkripsi File:**
   - Setelah file berhasil dikirim, klien memanggil fungsi `encryptFile()` untuk melakukan proses enkripsi pada file yang sama (`file_to_send.txt`).
   - Proses enkripsi dilakukan dengan menggunakan kunci AES yang telah ditetapkan (di sini disimpan dalam bentuk string biasa, namun dalam implementasi yang lebih aman, kunci akan diperoleh dengan cara yang lebih aman).

4. **Proses Enkripsi:**
   - File yang akan dienkripsi dibaca ke dalam byte array.
   - Objek Cipher diinisialisasi dengan algoritma enkripsi AES menggunakan kunci yang telah disediakan.
   - Isi file dienkripsi menggunakan metode `doFinal()` dari objek Cipher.
   - Hasil enkripsi disimpan ke dalam file baru (`file_to_send_encrypted.txt`).

5. **Penutup Koneksi:**
   - Setelah pengiriman file yang belum dienkripsi dan file yang telah dienkripsi selesai, koneksi socket ditutup.

Namun, penting untuk dicatat bahwa keamanan program ini dapat ditingkatkan. Penyimpanan kunci dalam bentuk string biasa dalam kode sumber adalah praktik yang tidak aman. Dalam lingkungan produksi, penggunaan kunci enkripsi yang lebih aman dan pengelolaan kunci yang tepat akan menjadi prioritas utama untuk menjaga keamanan transfer file terenkripsi.
