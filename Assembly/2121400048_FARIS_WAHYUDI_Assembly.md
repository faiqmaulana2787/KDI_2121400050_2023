1. Desain Bahasa Assembly:

    Digunakan untuk pemrograman tingkat rendah dengan kontrol langsung pada perangkat keras.
    Elemen dasar: mnemonik opcode, definisi data, dan arahan perakitan.
    Mnemonik opcode terdiri dari opcode dan operan.
    Arahan data mendefinisikan jenis, panjang, dan perataan data.
    Arahan perakitan (pseudo-opcode) memengaruhi assembler dan kode objek.

    Penggunaan Bahasa Assembly:

    Perdebatan seputar kinerja dan kegunaan dibandingkan dengan bahasa tingkat tinggi.
    Relevan untuk sistem dengan prosesor kuno, interaksi langsung dengan perangkat keras, dan instruksi khusus.
    Keuntungan melibatkan optimasi kinerja, kontrol penuh, dan penanganan kasus di mana bahasa tingkat tinggi kurang efektif.
    Relevan dalam pengembangan perangkat keras, perangkat lunak tertanam, dan program real-time.
    Tetap diajarkan untuk pemahaman konsep dasar komputer.

2.)    a. Syntax untuk Deklarasi Data Dasar (Intel x86):
    
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
