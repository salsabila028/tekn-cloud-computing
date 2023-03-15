# Instalasi Git For Window

   Sebelum install Git di Windows, anda harus sudah mempunyai editor teks yang didukung oleh Windws. Editor yang bisa dipilih banyak, tetapi disarankan menggunakan Notepad++ atau Visual Studion Code atau Vim. Keberadaan editor teks ini akan menentukan keberhasilan instalasi.

1. Setelah download Git, double click pada file yang di-download. Akan dimunculkan lisensi. Klik Next untuk lanjut. 

![01](PrakTC/instal-git/g01.jpg)

2. Setelah itu, pilih lokasi instalasi. Secara default akan terisi C:\Program Files\Git. Ganti lokasi jika memang anda menginginkan lokasi lain, klik Next

![02](PrakTC/instal-git/g02.jpg)

3. Pilih komponen. Tidak perlu diubah-ubah, sesuai dengan default saja. Klik pada Next.

![03](PrakTC/instal-git/g03.jpg)

4. Mengisi shortcut untuk menu Start. Gunakan default (Git), ganti jika ingin mengganti - misalnya Git VCS.

![04](PrakTC/instal-git/g04.jpg)

5. Pilih editor yang akan digunakan bersama dengan Git. Pada pilihan ini, digunakan Vim editor.

![05](PrakTC/instal-git/g05.jpg)

6. Pada saat instalasi, Git menyediakan akses git melalui Bash maupun command prompt. Pilih pilihan kedua supaya bisa menggunakan dari dua antarmuka tersebut. Bash adalah shell di Linux. Dengan menggunakan bash di Windows, pekerjaan di command line Windows bisa dilakukan menggunakan bash - termasuk ekskusi dari Git.

![06](PrakTC/instal-git/g07.jpg)



7. Pilih OpenSSL untuk HTTPS. Git menggunakan https untuk akes ke repo GitHub atau repo-repo lain (GitLab, Assembla).

![07](PrakTC/instal-git/g09.jpg)

8. Pilih pilihan pertama untuk konversi akhir baris (CR-LF).

![08](PrakTC/instal-git/g10.jpg)

9. Pilih PuTTY untuk terminal yang digunakan untuk mengakses Git Bash.

![09](PrakTC/instal-git/g11.jpg)

10. Untuk opsi ekstra, pilih serta aktifkan 1 dan 2.

![10](PrakTC/instal-git/g14.jpg)

11. Setelah itu proses instalasi akan dilakukan.

![11](PrakTC/instal-git/g16.jpg)

12. Jika selesai akan muncul dialog pemberitahuan. Klik pada Finish.

![12](PrakTC/instal-git/g17.jpg)

13. Untuk menjalankan, dari Start menu, ketikkan "Git", akan muncul beberapa pilihan. Pilih "Git Bash" atau "Git GUI".

![13](PrakTC/instal-git/git/g18.jpg)

14. Tampilan jika akan menggunakan "Git Bash"

![14](PrakTC/instal-git/git/GitBash.jpg)

15. Tampilan jika akan menggunakan "Git GUI"

![15](PrakTC/instal-git/git/GitGui.jpg)

16. Untuk mencoba dari command prompt, masuk ke command prompt, setelah itu eksekusi "git --version" untuk melihat apakah sudah terinstall atau belum. Jika sudah terinstall dengan benar, makan akan muncul hasil berikut:

![16](PrakTC/instal-git/git/GitCMD.jpg)


## Konfigurasi Git

Ada 2 hal yang perlu dikonfigurasi yaitu username dan email. Untuk itu gunakan perintah berikut :

![17](PrakTC/konfigurasi-git/g01.jpg)

Isian di atas harus disesuaikan dengan nama serta email yang digunakan untuk mendaftar di GitHub. Untuk melihat konfigurasi yang sudah ada:

![18](PrakTC/konfigurasi-git/g02.jpg)

Langkah ini cukup dilakukan sekali saja, kecuali jika ingin melakukan perubahan nama dan email.

# Mengelola Repo Sendiri di Account Sendiri

Setiap orang yang telah mempunyai account di GitHub bisa membuat repo dengan. Secara umum, langkah-langkahnya adalah sebagai berikut:
1. Buat repo kosong di GitHub, bisa public maupun private.
2. Cloe repo kosong tersebut di komputer lokal
3. Perintah berikutnya terkait dengan perubahan repo serta sinkronisasi antara GitHub dengan lokal.

## Membuat Repo

Untuk membuat repo, gunakan langkah-langkan berikut:
1. Klik tanda + pada bagian atas setelah login, pilih New repository

![19](PrakTC/mengelola-repo-sendiri-account/membuat-repo/g01.jpg)

2. Isikan nama, keterangan, serta lisensi. Jika dikehendaki, bisa membuat repo Private

![20](PrakTC/mengelola-repo-sendiri-account/membuat-repo/g02.jpg)

3. Klik Create Repository

Setelah langkah-langkah tersebut, repo akan dibuat dan bisa diakses menggunakan pola https://github.com/username/reponame. Pada repo tersebut, hanya akan muncul 1 file, yaitu LICENSE. Jika memilih membuat README pada saat langkah ke 2, juga akan muncul README.md. Ada atau tidak ada README.md tidak mempunyai efek apapun pada langkah ini.


## Clone Repo

Proses clone adalah proses untuk menduplikasikan remote repo di GitHub ke komputer lokal. Untuk melakukan proses clone, gunakan perintah berikut:

![21](PrakTC/mengelola-repo-sendiri-account/clone-repo/g01.jpg)

Setelah perintah ini, di direktori awesome-project akan disimpan isi repo yang sama dengan di GitHub. Perbedaannya, di komputer lokal terdapat direktori .git yang digunakan secara internal oleh Git.


## Mengelola Repo

Beberapa hal yang bisa dilakukan akan diuraikan sebagai berikut.

### Mengubah Isi - Push Tanpa Branching dan Merging

Perubahan isi bisa terjadi karena satu atau kombinasi beberapa hal berikut:
1. File dihapus
2. File diedit
3. Membuat file / direktori baru
4. Menghapus direktori

Untuk kasus-kasus tersebut, lakukan perubahan di komputer lokal, setelah itu push ke repo.

![22](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g01.jpg)

Cara ini lebih mudah tetapi mempunyai resiko jika terjadi kesalahan dalam edit. Cara yang lebih aman tetapi memerlukan langkah yang lebih panjang adalah branching and merging.

## Mengubah Isi dengan Branching and Merging

Cara ini lebih aman, terstruktur, terkendali, dan mempunyai history yang lebih baik. Jika perubahan yang kita buat sudah terlalu kacau dan kita menyesal, maka ada cara untuk "membersihkan" repo lokal kita. Secara umum, langkahnya adalah sebagai berikut:

1. Buat branch untuk menampung perubahan-perubahan
2. Lakukan perubahan-perubahan
3. Add dan commit perubahan-perubahan tersebut ke branch
4. Kembali ke repo master
5. Buat pull request di GitHub
6. Merge pull request di GitHub
7. Merge branch untuk menampung perubahan-perubahan tersebut ke master.
8. Selesai.

![23](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g02.jpg)

Setelah itu, kirim pull request (PR):

![24](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g04.jpg)

Setelah membuat PR, PR tersebut bisa di-merge:

![25](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g05.jpg)

Setelah itu, Confirm Merge, branch yang kita kirimkan tadi sudah dimasukkan ke branch master. Setelah itu, merge di komputer lokal:

![26](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g06.jpg)

## Sinkronisasi

Suatu saat, bisa saja terjadi kita menggunakan komputer lain dan mengedit repo melalui repo lokal di komputer lain, setelah itu pindah ke kamputer lain lagi. Saat itu, kita perlu melakukan sinkronisasi ke kemputer lokal. Perintah untuk sinkronisasi adalah:

![27](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g07.jpg)

Perintah ini dikerjakan di direktori tempat repo lokal kita berada.

## Membatalkan Perubahan

 Jika perubahan-perubahan yang kita lakukan sudah sedemikian kacaunya, maka kita bisa membuat supaya perubahan-perubahan yang kacau tersebut hilang dan kembali ke kondisi bersih seperti semula.
 
 ![28](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g08.jpg)
 
 ## Undo Commit Terakhir
 
 Suatu saat, mungkin kita sudah terlanjur mem-push perubahan ke repo GitHub, setelah itu kita baru menyadari bahwa perubahan tersebut salah. Untuk itu, kita bisa melakukan git revert.
 
 ![29](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g09.jpg)
  
  Contoh di atas adalah contoh untuk mengubah README.md dengan beberapa commit. Setelh itu, kita akan mengembalikan ke posisi terakhir sebelum commit terakhir.
  
 ![30](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/G10.jpg)
 
 Perintah di atas akan membuka editor. Pada editor tersebut kita bisa mengetikkan pesan revert ( = pesan commit untuk pembatalan). Setelah selesai, simpan.
 Selanjutnya, tinggal di-push ke repo GitHub.
 
 ![31](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g11.jpg)
 
 Jika commit sudah dilakukan, tetapi belum di-push ke repo GitHub (masih berada di lokal), cara membatalkannya:
 
 ![32](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g12.jpg)
 
 Untuk kembali ke perubahan pada saat yang sudah lama, yang perlu dilakukan adalah melakukan git revert <posisi> kemudian mengedit secara manual kemudian push ke repo.
  
 ![33](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g13.jpg)
  
  Setelah itu, jika dilihat pada file, akan muncul tambahan untuk memudahkan meng-edit. File ini harus di-resolve terlebih dahulu, setelah itu baru di add dan commit, Edit file tersebut, setelah itu simpan.
  
  ![34](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g14.jpg)
  
  Setelah itu, lanjutkan proses revert. Saat git revert --continue isikan pesan revert.
  
   ![35](PrakTC/mengelola-repo-sendiri-account/mengelola-repo/g15.jpg)
  
  
  # Mengelola Repo Sndiri di Organisasi
  
  Repo yang dibuat bisa diletakkan pada account kita maupun berada pada suatu organisasi. Organisasi bisa kita buat sendiri maupun kita dimasukkan menjadi anggota organisasi. Pada dasarnya, bagian ini sama dengan bagian sebelumnya, hanya saja, pada saat membuat repo Owner dari repo adalah organisasi seperti berikut ini:

 ![36](PrakTC/mengelola-repo-sendiri-di-organisasi/g01.jpg)
  
  ### Clone Repo
  
  ![37](PrakTC/mengelola-repo-sendiri-di-organisasi/g02.jpg)
  
  Untuk operasi-operasi lainnya sama saja dengan pembahasan sebelumnya.
