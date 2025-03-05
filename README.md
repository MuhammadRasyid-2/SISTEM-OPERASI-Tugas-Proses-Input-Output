# SISTEM-OPERASI-Tugas-Proses-Input-Output
Muhammad Rasyid
09030182428016
TK2A
1. Menampilkan Daftar Perangkat I/O (Character Device) di Sistem

Menampilkan daftar perangkat yang ada di sistem Linux, termasuk perangkat block (hard disk, USB) dan perangkat karakter (keyboard, mouse, dll):

ls -l /dev

2. Membuat Subdirektori januari, februari, dan maret

Membuat subdirektori di dalam direktori latihan5:

mkdir -p latihan5/januari latihan5/februari latihan5/maret

Opsi -p memastikan bahwa jika direktori latihan5 belum ada, maka akan dibuat terlebih dahulu.
3. Membuat File dataku dan Menyalinnya ke Subdirektori Lain

Membuat file dataku dengan informasi pribadi dan menyalinnya ke subdirektori februari dan maret:

echo -e "Nama: [Nama Anda]\nNIM: [NIM Anda]\nAlamat: [Alamat Anda]" > latihan5/januari/dataku

Salin file ke direktori februari dan maret:

cp latihan5/januari/dataku latihan5/februari/
cp latihan5/januari/dataku latihan5/maret/

4. Mengubah Izin Akses File dataku di Direktori januari

Memberikan izin read dan write kepada semua pengguna (user, group, dan others):

chmod 666 latihan5/januari/dataku

5. Mengubah Izin Akses File dataku di Direktori februari

Memberikan izin penuh kepada user dan izin read dan execute kepada group dan others:

chmod 755 latihan5/februari/dataku

6. Mengubah Izin Akses File dataku di Direktori maret

Memberikan izin penuh (read, write, execute) kepada semua pengguna:

chmod 777 latihan5/maret/dataku

Menghapus direktori maret:

rm -r latihan5/maret

7. Mengubah Izin Akses Direktori februari agar Hanya Bisa Dibaca

Memberikan izin read-only untuk semua pengguna:

chmod 444 latihan5/februari

Mencoba membuat direktori baru dalam februari (akan gagal karena izin read-only):

mkdir latihan5/februari/haha

8. Mengubah umask untuk Pengaturan Izin Default File

Mengubah umask menjadi 027 untuk memastikan file baru memiliki izin default rw-r-----:

umask 027
umask

9. Membuat Hard Link dan Symbolic Link dari File dataku

Membuat hard link ke file dataku:

ln latihan5/januari/dataku latihan5/januari/dataku.ini

Membuat symbolic link (symlink) ke file dataku:

ln -s latihan5/januari/dataku latihan5/januari/dataku.juga

Menampilkan jumlah link yang ada pada file dataku:

ls -l latihan5/januari/

Semoga ini membantu! Anda bisa menempelkan teks di atas langsung ke README GitHub Anda.

echo digunakan untuk menulis teks ke dalam file. \n digunakan untuk memberikan baris baru dalam teks.

cp latihan5/januari/dataku latihan5/februari/
cp latihan5/januari/dataku latihan5/maret/

Image

cp digunakan untuk menyalin file dari satu lokasi ke lokasi lain.
4. Ubah izin akses file dataku pada direktori januari sehingga group dan others dapat melakukan write

chmod 666 latihan5/januari/dataku

Image

chmod 666 memberikan izin read dan write untuk semua (user, group, dan others).
5. Ubah izin akses file dataku pada direktori februari

chmod 755 latihan5/februari/dataku

Image

chmod 755 memberikan user izin penuh (rwx), sedangkan group dan others hanya bisa read dan execute.
6. Ubah izin akses file dataku pada direktori maret sehingga semua dapat melakukan write, read, dan execute

chmod 777 latihan5/maret/dataku

Image

chmod 777 memberikan izin penuh kepada semua (user, group, dan others).

    Hapus direktori maret
    rm -r latihan5/maret

Image

rm -r digunakan untuk menghapus direktori beserta isinya.
8. Ubah kepemilikan sub direktori februari sehingga user dan group hanya dapat read

chmod 444 latihan5/februari

Image

chmod 444 memberikan izin read-only ke semua pengguna.
Coba buat direktori baru dalam februari

mkdir latihan5/februari/haha

Image
9. Modifikasi umask menjadi 027 dan cek nilai defaultnya

umask 027
umask

Image

umask 027 memastikan file baru memiliki izin default 640 (rw-r-----).
10. Buat link dari file dataku

ln latihan5/januari/dataku latihan5/januari/dataku.ini

Image
Hard link: file ini akan berbagi inode yang sama dengan file asli.

ln -s latihan5/januari/dataku latihan5/januari/dataku.juga

Image
Symbolic link: ini hanya menjadi referensi ke file asli.
Cek jumlah link yang terjadi

ls -l latihan5/januari/

Image
