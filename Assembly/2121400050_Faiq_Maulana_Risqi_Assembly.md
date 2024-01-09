1. Kode perakitan(Assembly) pertama di mana bahasa digunakan untuk mewakili instruksi kode mesin ditemukan dalam karya Kathleen dan Andrew Donald Booth tahun 1947, Coding for A. Karena perakitan tergantung pada instruksi kode mesin, setiap bahasa assembly khusus untuk arsitektur komputer tertentu. Sebagian besar bahasa assembly tidak menyediakan sintaks khusus untuk panggilan sistem operasi, dan sebagian besar bahasa assembly dapat digunakan secara universal dengan sistem operasi apa pun, karena bahasa tersebut menyediakan akses ke semua kemampuan nyata prosesor, di mana semua mekanisme panggilan sistem pada akhirnya beristirahat. Berbeda dengan bahasa assembly, sebagian besar bahasa pemrograman tingkat tinggi umumnya portabel di beberapa arsitektur tetapi memerlukan penafsiran atau kompilasi, tugas yang jauh lebih rumit daripada assembling. Pada dekade pertama komputasi, adalah hal biasa bagi pemrograman sistem dan pemrograman aplikasi untuk berlangsung sepenuhnya dalam bahasa assembly.Meskipun masih tak tergantikan untuk beberapa tujuan, sebagian besar pemrograman sekarang dilakukan dalam bahasa yang ditafsirkan dan dikompilasi tingkat tinggi. «Saat ini, adalah tipikal untuk menggunakan sejumlah kecil kode bahasa assembly dalam sistem yang lebih besar yang diimplementasikan dalam bahasa tingkat yang lebih tinggi, untuk alasan kinerja atau untuk berinteraksi langsung dengan perangkat keras dengan cara yang tidak didukung oleh bahasa tingkat yang lebih tinggi. » .

2. a.Syntax untuk Deklarasi Data Dasar (Intel x86)
   String: Menggunakan directive DB (Define Byte) untuk mendefinisikan string.
    Integer: Menggunakan directive DD (Define Doubleword) untuk mendefinisikan integer 32-bit.
    Boolean: Tidak ada tipe data boolean secara langsung; gunakan integer atau byte.
    Float 32-bit: Menggunakan directive DD untuk mendefinisikan angka desimal 32-bit.

  b. Syntax untuk Branching (If...Else...) (Intel x86):

    Menggunakan instruksi seperti CMP (Compare) diikuti oleh instruksi percabangan seperti JE (Jump if Equal) dan JNE (Jump if Not Equal).
  c. Syntax untuk Looping (Intel x86):
  
    While Loop: Menggunakan instruksi percabangan (misalnya, JMP) bersama dengan kondisi perulangan.
    For Loop: Bergantung pada assembler; variasinya berbeda.
    
  d. Syntax untuk Deklarasi Fungsi dan Pemanggilannya (Intel x86):
  
    Deklarasi Fungsi: Menggunakan directive PROC dan ENDP untuk menentukan awal dan akhir fungsi.
    Pemanggilan Fungsi: Menggunakan instruksi CALL untuk memanggil fungsi yang telah dideklarasikan sebelumnya.
