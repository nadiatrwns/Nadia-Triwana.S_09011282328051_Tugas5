### The following is article on how install Linux, I want you to format them for README Github, maket them looka bit fancy and keep the language in Indonesian:

## 1.	Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard output ke file baru.
![1](https://github.com/user-attachments/assets/5bcc11c9-6a36-4c24-a482-d142432883e2)
# •	ls -la: Menampilkan daftar lengkap file dan direktori di dalam direktori saat ini. Opsi -l menampilkan dalam format panjang (dengan detail seperti hak akses, ukuran, tanggal, dsb.), sedangkan opsi -a menampilkan file tersembunyi (file yang dimulai dengan titik).
# •	>: Mengalihkan output dari perintah ke file. Dalam hal ini, hasil perintah ls -la disimpan ke file daftar_direktori.txt. Jika file sudah ada, isinya akan dihapus dan diganti dengan hasil baru.

## 2.	Lihat daftar secara lengkap pada direktori /etc/paswd, belokkan tampilan standard output ke file baru tanpa menghapus file baru sebelumnya.
![2](https://github.com/user-attachments/assets/ad64f90b-1047-4708-af1f-4b3762910af8)
# •	ls -la /etc/passwd: Menampilkan detail lengkap dari file /etc/passwd.
# •	>>: Menambahkan output dari perintah ke file yang sudah ada. Jika file daftar_direktori.txt sudah ada, hasil baru ditambahkan ke akhir file, tanpa menghapus konten yang sudah ada sebelumnya.

## 3.	Urutkan file baru dengan cara membelokkan standard input.
![3](https://github.com/user-attachments/assets/2de3bccf-90ef-4f9b-8032-56fd15d5526c)
# •	sort: Mengurutkan isi file berdasarkan urutan alfabetik.
# •	<: Mengalihkan input dari file. Dalam hal ini, perintah sort membaca data dari file daftar_direktori.txt dan mengurutkan isinya. Outputnya akan ditampilkan ke layar (terminal).

## 4.	Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut
![4](https://github.com/user-attachments/assets/8e6320ee-9771-47f1-902d-87274263e846)
# •	sort: Mengurutkan isi file.
# •	<: Mengalihkan input dari file daftar_direktori.txt.
# •	>: Mengalihkan output ke file baru.urut. Jika file baru.urut sudah ada, isinya akan dihapus dan diganti dengan output dari perintah sort.

## 5.	Buatlah direktori latihan6 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt
![5](https://github.com/user-attachments/assets/24305c43-a940-4849-8549-a6ec81168170)
# •	mkdir latihan6: Membuat direktori bernama latihan6.
# •	2>: Mengalihkan output error (standard error) ke file rmdirerror.txt. Jika direktori sudah ada, mkdir akan menghasilkan error, dan error tersebut akan dialihkan ke file rmdirerror.txt.
# •	2>>: Sama seperti 2>, tetapi menambahkan error ke file tanpa menghapus isinya.

## 6.	Urutkan kalimat berikut:
# Jakarta
# Bandung
# Surabaya
# Padang
# Palembang
# Lampung
# Dengan menggunakan notasi here document (<@@@...@@@)
![6](https://github.com/user-attachments/assets/6aef18d1-df3e-4ce6-a4b8-9627cf390659)
# •	<<@@@: Notasi here document digunakan untuk memasukkan beberapa baris input secara langsung ke dalam perintah. Semua baris yang ditulis di antara @@@ akan menjadi input untuk perintah sort.
# •	sort: Mengurutkan daftar kota secara alfabetis.

## 7.	Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru.
![7](https://github.com/user-attachments/assets/1dd0aea0-10e8-4aaf-9816-505db3193d2b)
# •	wc: Word count, menghitung jumlah baris, kata, dan karakter dalam file.
# •	wc baru.urut: Menghitung jumlah baris, kata, dan karakter dari file baru.urut.
# •	>>: Menambahkan hasil dari perintah wc ke file daftar_direktori.txt tanpa menghapus isinya.

## 8.	Gunakan perintah di bawah ini dan perhatikan hasilnya.
# $ cat /etc/passwd | sort | pr –n | grep tty03  
![8a](https://github.com/user-attachments/assets/56161be6-7c49-43a8-91aa-32e03260eb2d)
# •	cat /etc/passwd: Menampilkan isi file /etc/passwd.
# •	|: Pipa (pipe), mengalihkan output dari satu perintah sebagai input ke perintah berikutnya.
# •	sort: Mengurutkan output dari cat /etc/passwd.
# •	pr -n: Menambahkan nomor halaman pada output yang sudah diurutkan.
# •	grep tty03: Mencari string "tty03" dalam hasil yang sudah diurutkan dan dinomori

# $ find /etc –print | head  
![8b](https://github.com/user-attachments/assets/8447f8fb-cae2-4128-a013-ef4fd39f8037)
# •	find /etc -print: Mencari dan menampilkan semua file dan direktori di dalam /etc.
# •	head: Menampilkan 10 baris pertama dari hasil pencarian.

# $ head /etc/passwd | tail –5 | sort  
![8c](https://github.com/user-attachments/assets/385ddb3b-2895-4d81-a8e1-ac79f2005210)
# •	head /etc/passwd: Menampilkan 10 baris pertama dari file /etc/passwd.
# •	tail -5: Menampilkan 5 baris terakhir dari output perintah head.
# •	sort: Mengurutkan 5 baris terakhir tersebut.

## 9.	Gunakan perintah $ who | cat | cat | sort | pr | head | cat | tail dan perhatikan hasilnya.
![9](https://github.com/user-attachments/assets/e4e64f0e-7046-40a3-874c-76ec8e186246)
# •	who: Menampilkan daftar pengguna yang sedang login ke sistem.
# •	cat: Menampilkan output tanpa memodifikasi (di sini digunakan beberapa kali untuk menunjukkan chaining tanpa efek nyata).
# •	sort: Mengurutkan output dari who.
# •	pr: Menambahkan nomor halaman pada hasil.
# •	head: Menampilkan 10 baris pertama.
# •	tail: Menampilkan 10 baris terakhir dari hasil head.
# Perintah ini mengilustrasikan chaining (menggabungkan perintah) untuk memproses output secara berurutan.
