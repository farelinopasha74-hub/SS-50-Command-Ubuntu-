# 50 Perintah Dasar Ubuntu (Linux Terminal) beserta Contoh Penggunaannya

Berikut adalah daftar 50 perintah penting di Ubuntu/Linux lengkap dengan penjelasan fungsi, sintaks, dan contoh penggunaannya dalam format file `.md` (Markdown).

---

## 1. Menavigasi dan Mengelola File & Direktori

### 1. `pwd` (Print Working Directory)
* **Fungsi:** Menampilkan direktori (folder) aktif tempat Anda berada saat ini.
* **Sintaks:** `pwd`
* **Contoh:**
```bash
pwd
# Output: /home/user/Dokumen
```

### 2. `ls` (List)
* **Fungsi:** Menampilkan daftar file dan folder di direktori saat ini.
* **Sintaks:** `ls [opsi] [direktori]`
* **Contoh:**
```bash
ls -la
# Menampilkan semua file (termasuk file tersembunyi) dengan detail izin, ukuran, dan tanggal.
```

### 3. `cd` (Change Directory)
* **Fungsi:** Berpindah antar direktori.
* **Sintaks:** `cd [nama_direktori]`
* **Contoh:**
```bash
cd /var/www/html
# Berpindah ke direktori /var/www/html
cd ~
# Kembali ke direktori home pengguna
cd ..
# Mundur satu tingkat ke folder di atasnya
```

### 4. `mkdir` (Make Directory)
* **Fungsi:** Membuat folder baru.
* **Sintaks:** `mkdir [opsi] [nama_folder]`
* **Contoh:**
```bash
mkdir projek_baru
# Membuat folder bernama 'projek_baru'
mkdir -p a/b/c
# Membuat folder bertingkat sekaligus
```

### 5. `rmdir`
* **Fungsi:** Menghapus folder kosong.
* **Sintaks:** `rmdir [nama_folder]`
* **Contoh:**
```bash
rmdir folder_kosong
```

### 6. `touch`
* **Fungsi:** Membuat file kosong baru atau memperbarui timestamp file.
* **Sintaks:** `touch [nama_file]`
* **Contoh:**
```bash
touch catatan.txt
# Membuat file teks kosong bernama catatan.txt
```

### 7. `cp` (Copy)
* **Fungsi:** Menyalin file atau folder.
* **Sintaks:** `cp [sumber] [tujuan]`
* **Contoh:**
```bash
cp catatan.txt backup_catatan.txt
# Menyalin catatan.txt menjadi backup_catatan.txt
cp -r folder_sumber folder_tujuan
# Menyalin seluruh isi folder
```

### 8. `mv` (Move)
* **Fungsi:** Memindahkan atau mengubah nama (rename) file/folder.
* **Sintaks:** `mv [sumber] [tujuan]`
* **Contoh:**
```bash
# Rename file
mv catatan.txt tugas_so.txt

# Memindahkan file
mv tugas_so.txt /home/user/Dokumen/
```

### 9. `rm` (Remove)
* **Fungsi:** Menghapus file atau folder.
* **Sintaks:** `rm [opsi] [nama_file]`
* **Contoh:**
```bash
rm tugas_so.txt
# Menghapus file tugas_so.txt
rm -rf folder_penting
# Menghapus folder beserta seluruh isinya secara paksa
```

### 10. `cat` (Concatenate)
* **Fungsi:** Menampilkan isi file teks langsung di terminal.
* **Sintaks:** `cat [nama_file]`
* **Contoh:**
```bash
cat catatan.txt
```

### 11. `less`
* **Fungsi:** Membaca file teks besar halaman per halaman.
* **Sintaks:** `less [nama_file]`
* **Contoh:**
```bash
less log_sistem.txt
# Gunakan tombol spasi untuk ke bawah, 'q' untuk keluar.
```

### 12. `head`
* **Fungsi:** Menampilkan beberapa baris pertama dari sebuah file.
* **Sintaks:** `head -n [jumlah_baris] [nama_file]`
* **Contoh:**
```bash
head -n 5 data.csv
# Menampilkan 5 baris pertama dari data.csv
```

### 13. `tail`
* **Fungsi:** Menampilkan beberapa baris terakhir dari sebuah file (sangat berguna untuk log).
* **Sintaks:** `tail -n [jumlah_baris] [nama_file]`
* **Contoh:**
```bash
tail -n 10 /var/log/syslog
# Menampilkan 10 baris terakhir log sistem
tail -f /var/log/syslog
# Memantau log secara real-time
```

---

## 2. Pencarian dan Filter Teks

### 14. `find`
* **Fungsi:** Mencari file atau direktori berdasarkan nama atau kriteria tertentu.
* **Sintaks:** `find [lokasi] -name [nama_file]`
* **Contoh:**
```bash
find /home/user -name "*.txt"
# Mencari semua file berformat .txt di dalam folder home user
```

### 15. `grep`
* **Fungsi:** Mencari teks atau pola tertentu di dalam file.
* **Sintaks:** `grep [pola] [nama_file]`
* **Contoh:**
```bash
grep "error" /var/log/syslog
# Mencari baris yang mengandung kata "error" di file syslog
```

### 16. `locate`
* **Fungsi:** Mencari file secara cepat menggunakan database sistem.
* **Sintaks:** `locate [nama_file]`
* **Contoh:**
```bash
locate nginx.conf
```

### 17. `wc` (Word Count)
* **Fungsi:** Menghitung jumlah baris, kata, dan karakter dalam file.
* **Sintaks:** `wc [nama_file]`
* **Contoh:**
```bash
wc -l catatan.txt
# Menghitung jumlah baris dalam file catatan.txt
```

---

## 3. Manajemen Pengguna dan Hak Akses (Permissions)

### 18. `sudo` (Superuser Do)
* **Fungsi:** Menjalankan perintah dengan hak istimewa administrator (root).
* **Sintaks:** `sudo [perintah]`
* **Contoh:**
```bash
sudo apt update
```

### 19. `su` (Switch User)
* **Fungsi:** Beralih ke pengguna lain atau akun root.
* **Sintaks:** `su [nama_pengguna]`
* **Contoh:**
```bash
su root
```

### 20. `useradd` / `adduser`
* **Fungsi:** Menambahkan pengguna baru ke sistem.
* **Sintaks:** `sudo adduser [nama_user]`
* **Contoh:**
```bash
sudo adduser budi
```

### 21. `passwd`
* **Fungsi:** Mengubah kata sandi pengguna.
* **Sintaks:** `passwd [nama_user]`
* **Contoh:**
```bash
passwd
# Mengubah password user yang sedang aktif
```

### 22. `chmod` (Change Mode)
* **Fungsi:** Mengubah izin akses file atau folder (read, write, execute).
* **Sintaks:** `chmod [izin] [nama_file]`
* **Contoh:**
```bash
chmod 755 skrip.sh
# Memberikan izin rwx untuk owner, rx untuk group dan others
```

### 23. `chown` (Change Owner)
* **Fungsi:** Mengubah kepemilikan file atau folder.
* **Sintaks:** `sudo chown [user]:[group] [nama_file]`
* **Contoh:**
```bash
sudo chown budi:budi index.html
```

---

## 4. Manajemen Proses dan Sistem

### 24. `ps` (Process Status)
* **Fungsi:** Menampilkan daftar proses yang sedang berjalan.
* **Sintaks:** `ps [opsi]`
* **Contoh:**
```bash
ps aux
# Menampilkan seluruh proses yang berjalan di sistem
```

### 25. `top` / `htop`
* **Fungsi:** Memantau penggunaan sumber daya sistem (CPU, RAM) secara real-time.
* **Sintaks:** `top` atau `htop`
* **Contoh:**
```bash
top
# Tekan 'q' untuk keluar.
```

### 26. `kill`
* **Fungsi:** Menghentikan proses yang sedang berjalan berdasarkan Process ID (PID).
* **Sintaks:** `kill [PID]`
* **Contoh:**
```bash
kill 1234
# Menghentikan proses dengan PID 1234
kill -9 1234
# Menghentikan proses secara paksa
```

### 27. `killall`
* **Fungsi:** Menghentikan proses berdasarkan nama aplikasinya.
* **Sintaks:** `killall [nama_aplikasi]`
* **Contoh:**
```bash
killall firefox
```

### 28. `df` (Disk Free)
* **Fungsi:** Menampilkan kapasitas dan penggunaan ruang hard disk.
* **Sintaks:** `df -h`
* **Contoh:**
```bash
df -h
# '-h' membuat format ukuran mudah dibaca (Human-readable, misal GB/MB)
```

### 29. `du` (Disk Usage)
* **Fungsi:** Memeriksa ukuran penggunaan folder atau file.
* **Sintaks:** `du -sh [nama_folder]`
* **Contoh:**
```bash
du -sh /var/www/html
```

### 30. `free`
* **Fungsi:** Menampilkan informasi penggunaan memori RAM dan Swap.
* **Sintaks:** `free -h`
* **Contoh:**
```bash
free -h
```

### 31. `uname`
* **Fungsi:** Menampilkan informasi sistem operasi dan kernel.
* **Sintaks:** `uname -a`
* **Contoh:**
```bash
uname -a
```

### 32. `uptime`
* **Fungsi:** Menampilkan berapa lama komputer/server telah menyala.
* **Sintaks:** `uptime`
* **Contoh:**
```bash
uptime
```

### 33. `history`
* **Fungsi:** Menampilkan riwayat perintah yang pernah diketikkan di terminal.
* **Sintaks:** `history`
* **Contoh:**
```bash
history
```

---

## 5. Jaringan (Networking)

### 34. `ping`
* **Fungsi:** Menguji koneksi internet atau jaringan ke server tujuan.
* **Sintaks:** `ping [alamat_ip / domain]`
* **Contoh:**
```bash
ping google.com
# Tekan Ctrl + C untuk berhenti.
```

### 35. `ifconfig` / `ip`
* **Fungsi:** Menampilkan konfigurasi antarmuka jaringan (IP Address, MAC Address).
* **Sintaks:** `ip a` atau `ifconfig`
* **Contoh:**
```bash
ip a
```

### 36. `netstat` / `ss`
* **Fungsi:** Menampilkan koneksi jaringan, port yang terbuka, dan statistik socket.
* **Sintaks:** `ss -tuln`
* **Contoh:**
```bash
ss -tuln
# Menampilkan port yang sedang mendengarkan (listening)
```

### 37. `curl`
* **Fungsi:** Mengirim atau menerima data dari server via URL (mendukung HTTP, HTTPS, FTP).
* **Sintaks:** `curl [url]`
* **Contoh:**
```bash
curl -I https://google.com
# Mengambil header HTTP dari website google.com
```

### 38. `wget`
* **Fungsi:** Mengunduh file dari internet melalui terminal.
* **Sintaks:** `wget [url_file]`
* **Contoh:**
```bash
wget https://wordpress.org/latest.zip
```

### 39. `traceroute`
* **Fungsi:** Melacak jalur (hop) paket data saat menuju ke server tujuan.
* **Sintaks:** `traceroute [domain]`
* **Contoh:**
```bash
traceroute github.com
```

---

## 6. Arsip dan Kompresi (Backup)

### 40. `tar`
* **Fungsi:** Mengompres atau mengekstrak file arsip `.tar` atau `.tar.gz`.
* **Sintaks:** 
  * Kompres: `tar -czvf [nama_arsip.tar.gz] [folder]`
  * Ekstrak: `tar -xzvf [nama_arsip.tar.gz]`
* **Contoh:**
```bash
tar -czvf backup_web.tar.gz /var/www/html
# Mengompres folder html menjadi backup_web.tar.gz
tar -xzvf backup_web.tar.gz
# Mengekstrak file arsip
```

### 41. `zip` & `unzip`
* **Fungsi:** Membuat dan mengekstrak file berformat `.zip`.
* **Sintaks:** 
  * Kompres: `zip file.zip [file_sumber]`
  * Ekstrak: `unzip file.zip`
* **Contoh:**
```bash
zip dokumen.zip catatan.txt tugas_so.txt
unzip dokumen.zip
```

---

## 7. Manajemen Paket (Package Manager - APT)

### 42. `apt update`
* **Fungsi:** Memperbarui daftar repositori software terbaru di Ubuntu.
* **Sintaks:** `sudo apt update`
* **Contoh:**
```bash
sudo apt update
```

### 43. `apt upgrade`
* **Fungsi:** Melakukan pembaruan (upgrade) pada semua aplikasi yang terinstal.
* **Sintaks:** `sudo apt upgrade`
* **Contoh:**
```bash
sudo apt upgrade -y
```

### 44. `apt install`
* **Fungsi:** Menginstal aplikasi baru.
* **Sintaks:** `sudo apt install [nama_aplikasi]`
* **Contoh:**
```bash
sudo apt install nginx -y
# Menginstal web server Nginx
```

### 45. `apt remove` / `apt purge`
* **Fungsi:** Menghapus aplikasi yang terinstal.
* **Sintaks:** `sudo apt remove [nama_aplikasi]`
* **Contoh:**
```bash
sudo apt remove nginx
```

### 46. `apt search`
* **Fungsi:** Mencari paket aplikasi yang tersedia di repositori Ubuntu.
* **Sintaks:** `apt search [nama_aplikasi]`
* **Contoh:**
```bash
apt search python3
```

---

## 8. Utilitas Tambahan

### 47. `echo`
* **Fungsi:** Menampilkan teks ke layar terminal atau menulis ke dalam file.
* **Sintaks:** `echo "[teks]"`
* **Contoh:**
```bash
echo "Halo, Sistem Operasi!"
echo "Teks baru" > file.txt
# Menulis teks ke file.txt (menimpa isi lama)
```

### 48. `clear`
* **Fungsi:** Membersihkan layar terminal.
* **Sintaks:** `clear` (atau shortcut `Ctrl + L`)
* **Contoh:**
```bash
clear
```

### 49. `date`
* **Fungsi:** Menampilkan atau mengatur tanggal dan waktu sistem.
* **Sintaks:** `date`
* **Contoh:**
```bash
date
```

### 50. `man` (Manual)
* **Fungsi:** Membuka panduan manual penggunaan suatu perintah terminal.
* **Sintaks:** `man [perintah]`
* **Contoh:**
```bash
man ls
# Menampilkan manual lengkap perintah ls. Tekan 'q' untuk keluar.
```
