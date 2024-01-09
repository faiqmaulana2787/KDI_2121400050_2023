1. Bahasa rakitan atau lebih umum dikenal sebagai assembly language adalah bahasa pemrograman tingkat rendah yang digunakan dalam pemrograman komputer, mikroprosesor, pengendali mikro, dan perangkat lainnya yang dapat diprogram. Bahasa rakitan mengimplementasikan representasi atas kode mesin dalam bentuk simbol-simbol yang secara relatif lebih dapat dipahami oleh manusia. Berbeda halnya dengan bahasa-bahasa tingkat tinggi yang berlaku umum, bahasa rakitan biasanya mendukung secara spesifik untuk suatu ataupun beberapa jenis arsitektur komputer tertentu. Dengan demikian, portabilitas bahasa rakitan tidak dapat menandingi bahasa-bahasa lainnya yang merupakan bahasa pemrograman tingkat tinggi.Pada bahasa rakitan, programmer umumnya menggunakan sebuah program utilitas yang disebut sebagai perakit (bahasa Inggris: assembler) yang digunakan untuk menerjemahkan kode dalam bahasa rakitan tersebut ke dalam kode mesin untuk perangkat keras tertentu.
2. a. String: Menggunakan directive DB (Define Byte) untuk mendefinisikan string.
    Integer: Menggunakan directive DD (Define Doubleword) untuk mendefinisikan integer 32-bit.
    Boolean: Tidak ada tipe data boolean secara langsung; gunakan integer atau byte.
    Float 32-bit: Menggunakan directive DD untuk mendefinisikan angka desimal 32-bit.
  b. yntax untuk Branching (If...Else...) (Intel x86):
    Menggunakan instruksi seperti CMP (Compare) diikuti oleh instruksi percabangan seperti JE (Jump if Equal) dan JNE (Jump if Not Equal).
  c. Syntax untuk Looping (Intel x86):
    While Loop: Menggunakan instruksi percabangan (misalnya, JMP) bersama dengan kondisi perulangan.
    For Loop: Bergantung pada assembler; variasinya berbeda.
  d. yntax untuk Deklarasi Fungsi dan Pemanggilannya (Intel x86):
    Deklarasi Fungsi: Menggunakan directive PROC dan ENDP untuk menentukan awal dan akhir fungsi.
    Pemanggilan Fungsi: Menggunakan instruksi CALL untuk memanggil fungsi yang telah dideklarasikan sebelumnya.
