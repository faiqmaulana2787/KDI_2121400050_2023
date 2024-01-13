1. Bahasa assembly adalah bahasa level rendah yang merupakan representasi teks dari kode mesin yang bisa dibaca oleh manusia.
Setiap jenis prosesor CPU memiliki bahasa assembly nya masing-masing, seperti x86 untuk prosesor Intel, MIPS untuk CPU MIPS, dan ARM untuk ARM prosesor.
Bahasa assembly berbeda dari bahasa mesin karena menggunakan mnemonic atau penamaan, sehingga lebih mudah untuk dibaca dan ditulis.
Program assembly ditulis dengan assembly source code, kemudian dikompilasi oleh assembler menjadi kode mesin sebelum bisa dieksekusi oleh mesin.
Bahasa assembly sangat dekat dengan hardware sehingga memungkinkan pengaturan register, akses memori, dan fitur hardware lain secara langsung.
Assembly sering digunakan untuk menulis program inti sistem operasi, driver, firmware, dan rutin-rutin tertentu yang membutuhkan kecepatan dan akses hardware tingkat rendah.
Mayoritas program saat ini lebih banyak menggunakan bahasa pemrograman level tinggi dan library untuk meningkatkan produktivitas.
2.  a. Deklarasi data dasar seperti string menggunakan directive DB contohnya "nama DB "John"", integer 16 bit pakai DW misal "umur DW 20", integer 32 bit pakai DD seperti "gaji DD 2500", boolean 0 atau 1 seperti "lulus DB 1", dan float point 32 bit juga pakai DD misal "ipk DD 3.5".

    b. Percabangan if-else dilakukan dengan membandingkan nilai register atau variabel menggunakan instruksi CMP lalu diikuti lompat bersyarat sesuai kondisi yang diinginkan seperti JE untuk lompat jika sama, JNE untuk lompat jika tidak sama. Contoh "CMP umur, 17" dan "JL di_bawah_17".

    c. Perulangan while menggunakan label sebagai penanda awal loop dan instruksi lompat bersyarat ke label tersebut. Perulangan definite seperti for dan do-while menggunakan register counter CX atau ECX sebagai pencacah interasinya. Contoh while "label: loop label" dan for "mov cx,5; label: loop label".

    d. Deklarasi fungsi diawali label nama fungsi, berisi kode fungsi, dan diakhiri instruksi ret. Pemanggilannya menggunakan call nama_fungsi dengan parameter lewat stack. Contoh "tambah_dd: kode fungsi ret" dan "main: push arg1; push arg2; call tambah_dd; add esp, 8".
