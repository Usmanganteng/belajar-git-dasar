# GIT DASAR 

1. Poin utama :
   
  a. Apa itu git?

    Git, yang diciptakan oleh Linus Torvalds pada tahun 2005, menjadi populer karena
    sifatnya yang terdistribusi dan fleksibilitasnya, terutama dalam proyek-proyek sumber
    terbuka yang kolaboratif.

  b. Cara Kerja git

    1. Cara membuat repository git
 
      - Repositori git dapat diinisialisasi di dalam folder proyek yang sudah ada, baik yang kosong maupun yang berisi file. Untuk menginisialisasi repositori, gunakan perintah "git init" di dalam terminal/git bash.
  
      - Setelah inisialisasi, sebuah folder baru bernama .git akan dibuat untuk menyimpan data repositori. Hindari memodifikasi konten folder ini.
  
      - Git mengikuti alur kerja tiga langkah: modified, staged, dan committed. File dimodifikasi di working directory, staging untuk commit, lalu dicommit ke repositori.
  
      -Git menggunakan penunjuk yang disebut "head" untuk menunjukkan commit terakhir dalam repositori.
  
      -Setelah perubahan dicommit, tidak ada cara langsung untuk membatalkannya, pilihannya seperti rollback, reset, atau revert, masing-masing dengan implikasi yang berbeda.
  
      -Mengganti nama file di Git dapat dideteksi sebagai operasi penghapusan dan penambahan. Git mendeteksi kemiripan dalam konten file untuk mengidentifikasi penggantian nama secara akurat.

    2. Code git dasar
 
      - Gunakan 'git status' untuk memeriksa perubahan dalam repositori, seperti file baru, file yang dimodifikasi, atau file yang dihapus.
  
      - Untuk menambahkan perubahan secara permanen ke repository Git, gunakan perintah 'git commit' setelah melakukan perubahan.
  
      - Git menyediakan perintah seperti 'git diff' untuk melihat perubahan yang dibuat pada berkas di repositori.
  
      - Perubahan pada beberapa file dapat dilakukan dengan menggunakan "git add" sebelum melakukan commit.
  
      - Penghapusan dan penambahan file dapat dilacak menggunakan "git status" dan dikelola dengan 'git add' dan 'git commit'.
  
      -Membatalkan perubahan dapat dilakukan dengan 'git restore' untuk modifikasi atau penghapusan yang dilakukan di working directory.
  
      -Untuk membatalkan perubahan yang staging untuk commit, 'git restore --staged' dapat digunakan untuk memindahkan perubahan kembali ke working directory.

  c. git log 

    1. Git memungkinkan Anda untuk melihat riwayat commit menggunakan perintah 'git log'.
  
    2. Perintah 'git log' menampilkan detail commit seperti penulis, tanggal, dan pesan.
  
    3. Untuk menyederhanakan output 'git log', Anda dapat menggunakan opsi '--oneline' untuk menampilkan satu commit per baris.
  
    4. Membandingkan commit di Git berfokus pada status akhir file daripada perubahan individual.
  
    5. Perintah 'git diff' membandingkan perbedaan antara komit atau cabang.

  d. Reset commit

    - Menggunakan 'git reset' dengan opsi '--soft' memindahkan penunjuk HEAD ke commit yang berbeda tanpa mengubah staging index dan working directory, menjadikannya opsi yang aman untuk membatalkan komit.
 
    - 'git reset' dengan opsi '--mixed' memindahkan penunjuk HEAD dan mengatur ulang staging index ke commit yang ditentukan sambil mempertahankan perubahan di working directory, sehingga memungkinkan penyesuaian lebih lanjut sebelum melakukan commit.
 
    - 'git reset' dengan opsi '--hard' mereset penunjuk HEAD, staging index, dan working directory ke commit yang ditentukan, secara efektif menghapus semua perubahan, menjadikannya opsi yang paling merusak.
 
    - Setelah operasi reset, perubahan dapat dipulihkan jika commit baru belum dibuat, tetapi membuat commit baru akan menggantikan riwayat commit, membuat perubahan tidak dapat dipulihkan.
 
    - Mengatur ulang commit dapat berguna untuk memperbaiki kesalahan atau menambahkan perubahan yang terlupakan sebelum membuat commit baru.

  e. amend commit

    - Git menyediakan perintah 'git commit --amend' untuk menambahkan perubahan secara otomatis pada snapshot terakhir, menggabungkannya dengan perubahan pada commit sebelumnya.
 
    - Menggunakan 'git commit --amend' memungkinkan untuk menambahkan perubahan pada commit sebelumnya tanpa membuat commit baru, menyederhanakan prosesnya dibandingkan dengan mengatur ulang dan melakukan commit ulang.
 
    - Ketika menggunakan 'git commit --amend', bahkan menambahkan satu karakter pun akan secara otomatis mengubah konten dan tanda tangan snapshot.

  f. git checkout

    - Dengan menggunakan 'git checkout' untuk menavigasi ke commit tertentu, perubahan pada berkas dapat dilakukan secara bertahap, sehingga memungkinkan pemeriksaan tanpa mengubah repositori secara permanen.
 
    - 'git checkout' dengan nama branch memungkinkan untuk berpindah di antara branch-branch yang berbeda di repositori. Untuk menavigasi ke commit tertentu, "git checkout" diikuti dengan hash commit atau nama branch yang dapat digunakan.
 
    - Perintah 'git checkout' seperti mesin waktu, memungkinkan pengguna untuk berpindah-pindah di antara snapshot yang berbeda dalam riwayat repositori.

  g. git revert

    - Fitur 'git revert' dari Git memungkinkan untuk membatalkan commit sebelumnya dengan membuat commit baru dengan perubahan yang berlawanan dengan perubahan yang dikembalikan.
 
    - Tidak seperti reset, git revert tidak menghapus riwayat tetapi membuat commit baru yang membalikkan perubahan yang dibuat oleh commit sebelumnya.
 
    - Ketika menggunakan Git, perintah "git revert" dapat secara otomatis membatalkan perubahan yang dibuat pada commit tertentu, membuat commit baru dengan perubahan yang berlawanan.

  h. gitignore

    - File .gitignore memungkinkan Anda menentukan file atau directory mana yang harus diabaikan oleh Git, berguna untuk mengecualikan file yang dibuat, log, atau jenis file tertentu dari kontrol versi.

  i. git blame

    - Perintah 'git blame' Git membantu melacak siapa yang membuat perubahan pada sebuah file dan kapan, memberikan tampilan terperinci tentang kepengarangan setiap baris dan komit terkait.


2. catatan tambahan
   
   a. git bisa berguna untuk berkerja tim dan sangat feleksibel karena ketika kita berganti device kita tidak perlu khawatir dengan projeck kita

3. Kesimpulan
  - Git Branch memungkinkan kita untuk membuat cabang (branch) dari proyek utama dan bekerja pada cabang tersebut secara independen.

  - Dengan branch, kita dapat mengembangkan fitur baru tanpa mengganggu pengembangan di branch utama.
  
  - Konflik dapat terjadi saat menggabungkan perubahan dari branch yang berbeda, dan kita harus mengatasi konflik secara manual.

  - Merge adalah proses menggabungkan perubahan dari satu branch ke branch lain.

  - Cherry pick memungkinkan kita untuk memilih commit tertentu dari satu branch dan menerapkannya ke branch lain