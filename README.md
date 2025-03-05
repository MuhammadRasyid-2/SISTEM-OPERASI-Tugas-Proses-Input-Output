# SISTEM-OPERASI-Tugas-Proses-Input-Output
Muhammad Rasyid
09030182428016
TK2A
1. Lihat peralatan I/O, character device, yang ada pada sistem komputer

ls -l /dev

Image

Menampilkan daftar perangkat yang ada di sistem Linux, termasuk perangkat block (hard disk, USB) dan character device (keyboard, mouse, dll).
2. Buat sub direktori januari, februari, dan maret sekaligus pada direktori latihan5

mkdir -p latihan5/januari latihan5/februari latihan5/maret

Image

mkdir digunakan untuk membuat direktori. Opsi -p memastikan bahwa jika direktori latihan5 belum ada, maka akan dibuat terlebih dahulu.
3. Buat file dataku dan salin ke sub direktori lainnya

echo -e "Nama: [Nama Anda]\nNIM: [NIM Anda]\nAlamat: [Alamat Anda]" > latihan5/januari/dataku

Image

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
