# GIT branching

##  Poin utama :

### Apa itu git branch ?
    
  - Git Branch adalah fitur pada sistem pengontrol versi Git yang memungkinkan pengguna untuk membuat cabang (branch) dari proyek utama dan bekerja pada cabang tersebut secara independen. Manajemen Git Branch adalah proses pemeliharaan dan pengaturan cabang dalam sebuah proyek Git. Dengan menggunakan branch.

### cara kerja git branch

1.  pembuatan branch
  -Ketika kita ingin mengembangkan fitur baru atau memperbaiki bug, kita membuat branch baru dari branch utama (biasanya bernama “master” atau “main”).
  -Branch ini berfungsi sebagai salinan dari branch utama, dan kita dapat bekerja di dalamnya tanpa mempengaruhi kode di branch utama.
    
2.  pemindahan ke branch baru
  -Setelah membuat branch baru, kita beralih ke branch tersebut menggunakan perintah `git checkout [nama_branch]`.
  -Misalnya, jika kita membuat branch dengan nama “fitur-login”, kita akan mengetik git checkout fitur-login.

3.  Pengembangan di Branch Baru
-Di dalam branch baru, kita dapat membuat perubahan pada kode tanpa memengaruhi branch utama.
-Kita bisa menambahkan fitur baru, memperbaiki bug, atau melakukan perubahan lain sesuai kebutuhan.

4.  Penggabungan Kembali (Merge):
-Setelah selesai mengembangkan fitur di branch baru, kita ingin menggabungkannya kembali ke branch utama.
-Kita menggunakan perintah `git merge [nama_branch]` untuk menggabungkan perubahan dari branch baru ke branch utama.

5.  Manajemen Branch:
-Kita dapat membuat, menghapus, dan beralih antara branch menggunakan perintah-perintah seperti `git branch`, `git branch -d`, dan `git checkout`.

### cara kerja git merge

  - Merge adalah proses menggabungkan perubahan dari satu branch ke branch lain dalam sistem pengontrol versi Git. Mari kita jelajahi cara kerja merge

    1.  Pemilihan Branch Tujuan
     -Pertama, kita memilih branch yang akan menerima perubahan. Biasanya, ini adalah branch utama (seperti “master” atau “main”).
     -Misalnya, kita ingin menggabungkan perubahan dari branch fitur-login ke branch utama.

    2.  Eksekusi Merge
     -Kita menggunakan perintah `git merge [nama_branch]` untuk menggabungkan perubahan dari branch lain ke branch tujuan.
     -Git akan mencari perubahan yang ada di branch lain dan menggabungkannya dengan branch tujuan.

    3.  Penanganan Konflik
     -Jika ada konflik antara perubahan di kedua branch, Git akan memberi tahu kita.
     -Kita perlu memeriksa dan memperbaiki konflik secara manual sebelum melanjutkan.

    4.  Commit Hasil Merge
     -Setelah mengatasi konflik, kita melakukan commit untuk menyimpan hasil merge.
     -Perubahan dari branch lain sekarang ada di branch tujuan.

### cara menangani konflik

  - Konflik pada merge adalah situasi di mana terjadi pertentangan antara perubahan dari dua branch yang berbeda saat kita mencoba menggabungkannya. Berikut adalah cara mengatasi konflik pada saat melakukan merge:

    1.  Deteksi Konflik
     -Ketika kita menjalankan perintah git merge, Git akan mencoba menggabungkan perubahan dari branch lain ke branch tujuan.
     -Jika ada perubahan yang bertentangan pada file atau komponen tertentu, Git akan menunjukkan pesan konflik.

    2.  Buka File yang Bertanda Konflik
     -Buka file yang ditandai dengan konflik menggunakan editor teks.
     -Di dalam file tersebut, kita akan melihat bagian yang menunjukkan konflik dan perubahan dari kedua branch.

    3.  Perbaiki Konflik Secara Manual:
     -Perbaiki konflik dengan memilih perubahan yang sesuai atau menggabungkan keduanya.
     -Kita dapat memutuskan mana yang harus dipertahankan dan mana yang harus dihapus.

    4.  Commit Hasil Merge
     -Setelah mengatasi konflik, kita lakukan commit untuk menyimpan hasil merge.
     -Perubahan dari branch lain sekarang ada di branch tujuan.

     