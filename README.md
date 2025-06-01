A. Deskripsi Algoritma Greedy yang Diimplementasikan

Bot kami menggunakan algoritma greedy berbasis jarak terdekat dengan kombinasi pemantauan inventory. Strategi ini membuat bot selalu mencari diamond terdekat berdasarkan jarak Manhattan dari posisinya saat ini. Jika inventory sudah mencapai kapasitas tertentu (maksimal 5), bot akan segera kembali ke base untuk menyetorkan diamond agar skor bertambah dan inventory dikosongkan.

Ciri khas dari strategi greedy kami:
•	Pemilihan target diamond berdasarkan jarak terdekat.
•	Prioritas bergerak ke arah horizontal atau vertikal yang valid (menghindari gerakan tak sah).
•	Return ke base saat inventory penuh.
•	Pemilihan langkah cadangan jika tidak ada arah valid ke target.

B. Strategi ini menghasilkan gerakan cepat, efisien, dan dapat bekerja dalam skenario kompetitif dengan bot lain tanpa perlu komunikasi antar-bot.
Requirements dan Instalasi
Bahasa dan Dependensi:
•	Python 3.8 atau lebih baru
•	pip (Python package manager)

Install dependencies:
Masuk ke folder src/, lalu jalankan:
pip install -r requirements.txt
Menjalankan Backend
1.	Pastikan sudah meng-clone dan menjalankan game engine dari repository resmi.
2.	Jalankan backend dari direktori packages/backend:
npm install
npm run start:dev

C. Menjalankan Bot
Berikut ini adalah panduan langkah demi langkah untuk menjalankan program bot dalam permainan Diamonds:
1.	Masuk ke direktori utama (root directory) dari proyek bot, kemudian jalankan perintah berikut untuk mengunduh dan memasang semua dependensi yang dibutuhkan:
pip install -r requirements.txt

2.	Menjalankan satu bot
Untuk menjalankan satu bot, buka terminal dan jalankan perintah berikut:
python main.py --logic Random --email=your_email@example.com --name=your_name --password=your_password --team=etimo

3.	Menjalankan banyak bot sekaligus
Untuk menjalankan lebih dari satu bot secara paralel:
•	Di Windows, buat file bernama run.bat dengan isi sebagai berikut:
 @echo off
start cmd /c "python main.py --logic Greedy --email=najla@email.com --name=sakura --password=123456 --team etimo"
start cmd /c "python main.py --logic Greedy --email=najlatika@email.com --name=lily --password=123456 --team etimo"
start cmd /c "python main.py --logic Greedy --email=hanifah@email.com --name=mawar --password=123456 --team etimo"
start cmd /c "python main.py --logic Greedy --email=hanifahhasanah@email.com --name=tulip --password=123456 --team etimo"

•	Di Linux/macOS (UNIX-based OS), buat file bernama run.sh:
 #!/bin/bash
python main.py --logic Random --email=test@email.com --name=stima --password=123456 --team etimo &
python main.py --logic Random --email=test1@email.com --name=stima1 --password=123456 --team etimo &
python main.py --logic Random --email=test2@email.com --name=stima2 --password=123456 --team etimo &
python main.py --logic Random --email=test3@email.com --name=stima3 --password=123456 --team etimo &

4.	Menjalankan file .bat atau .sh
•	Untuk pengguna Windows, jalankan file:
./run.bat

•	Untuk pengguna Linux/macOS, ubah izin file lalu jalankan:
chmod +x ./run.sh
./run.sh

6.	Melihat visualisasi permainan
Setelah bot dijalankan, buka browser dan akses alamat berikut:
http://localhost:8082/

D. Author (Identitas Kelompok)
Kelompok 15: yayaa
•	Najlatika — 123140078
•	Hanifah Hasanah — 123140082
