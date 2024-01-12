1. Desain bahasa assembly

Desain bahasa assembly merujuk pada struktur dan aturan yang membentuk bahasa pemrograman tingkat rendah yang berfungsi sebagai representasi langsung dari instruksi-instruksi mesin pada suatu arsitektur prosesor tertentu. Desain bahasa assembly sangat tergantung pada arsitektur prosesor yang digunakan. Setiap arsitektur memiliki instruksi dan konvensi tertentu yang tercermin dalam desain bahasa assembly-nya. Pemrograman dalam bahasa assembly memerlukan pemahaman yang mendalam tentang arsitektur perangkat keras yang ditargetkan.

 Penggunaan bahasa assembly

Bahasa assembly digunakan dalam berbagai konteks, bahasa assembly memberikan kontrol tinggi terhadap perangkat keras, penggunaannya semakin terbatas karena kompleksitas dan kerumitan penulisan kode. Oleh karena itu, dalam pengembangan umum, penggunaan bahasa tingkat tinggi lebih umum untuk meningkatkan produktivitas dan keterbacaan kode.

2. Mengikuti kesepakatan versi Intel x86, jelaskan:

a. Syntax untuk Deklarasi Data Dasar (Intel x86):

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
