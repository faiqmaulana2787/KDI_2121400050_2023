1.	Bahasa rakitan, atau lebih umum dikenal sebagai assembly language, adalah bentuk bahasa pemrograman tingkat rendah yang digunakan dalam pemrograman komputer, mikroprosesor, pengendali mikro, dan perangkat lain yang dapat diprogram. Dalam bahasa rakitan, representasi kode mesin diimplementasikan dalam simbol-simbol yang lebih dapat dipahami oleh manusia daripada representasi langsung dalam bahasa mesin.

Berbeda dengan bahasa pemrograman tingkat tinggi yang umumnya portabel, bahasa rakitan biasanya dikhususkan untuk suatu arsitektur komputer tertentu. Meskipun kurang portabel, bahasa rakitan memungkinkan programmer memanfaatkan sepenuhnya kemampuan perangkat keras yang mungkin terbatas jika menggunakan bahasa pemrograman tingkat tinggi.

Dalam penggunaannya, programmer biasanya menggunakan perakitan (assembler) untuk menerjemahkan kode bahasa rakitan ke dalam kode mesin khusus perangkat keras. Instruksi dalam bahasa rakitan diterjemahkan menjadi instruksi mnemonic dalam kode mesin, berbeda dengan kompiler pada bahasa pemrograman tingkat tinggi yang menghasilkan sejumlah instruksi dalam kode mesin dari satu perintah.

Beberapa perangkat lunak bahasa rakitan terkenal menyediakan fitur tambahan untuk memfasilitasi pengembangan program, pengendalian proses perakitan, dan alat bantu debugging.

Ada beberapa alasan dasar untuk menggunakan bahasa rakitan. Pertama, dibandingkan dengan bahasa mesin, bahasa rakitan memberikan representasi lebih mudah dipahami oleh manusia, menggunakan simbol-simbol yang lebih dimengerti daripada simbol mnemonic kode mesin secara langsung. Selain itu, bahasa rakitan memungkinkan penggunaan pelabelan yang memudahkan penggunaan mekanisme lompatan daripada menggunakan alamat memori langsung.

Kedua, dibandingkan dengan bahasa pemrograman tingkat tinggi, bahasa rakitan memungkinkan programmer untuk mengontrol dan memanfaatkan penuh kapabilitas perangkat keras. Hal ini menjadikan bahasa rakitan menjanjikan tingkat unjuk kerja maksimum karena menerjemahkan instruksi rakitan secara langsung menjadi instruksi mesin, tanpa perantaraan sejumlah kode mesin.

Dalam bahasa rakitan, setiap instruksi merupakan representasi langsung dari instruksi kode mesin. Sebagai contoh, instruksi untuk memindahkan nilai 97 ke dalam register prosesor AL pada prosesor x86 dapat direpresentasikan dalam kode mesin dan diubah ke dalam bentuk yang lebih mudah dibaca manusia dengan menggunakan bilangan heksadesimal.

Bahasa rakitan memungkinkan programmer menambahkan komentar pada setiap instruksi, memudahkan pembacaan dan pemahaman kode. Meskipun kurang portabel, bahasa rakitan memberikan fleksibilitas dan kendali penuh kepada programmer atas perangkat keras yang digunakan.

2.	a. Syntax untuk deklarasi data dasar (string, integer, boolean, float 32-bit):
Dalam bahasa rakitan Intel x86, deklarasi data biasanya dilakukan dengan mengalokasikan ruang di memori. Contoh syntax untuk deklarasi variabel integer dan float 32-bit adalah sebagai berikut:
section .data
    ; Deklarasi variabel integer
    integer_var dd 0

    ; Deklarasi variabel float 32-bit
    float_var dd 0.0

    ; Deklarasi string
    string_var db 'Hello, World!', 0
Pada contoh di atas, dd digunakan untuk mendeklarasikan double word (32-bit) dan db digunakan untuk mendeklarasikan byte (8-bit) untuk string.

b. Syntax untuk branching (if ... else ...) beserta variasinya:
Percabangan (branching) dalam bahasa rakitan Intel x86 sering kali diimplementasikan menggunakan instruksi-jump berdasarkan kondisi. Contoh untuk branching if-else adalah sebagai berikut:
section .text
    mov eax, 5
    cmp eax, 10 ; Membandingkan nilai eax dengan 10
    jl  kurang_dari_10 ; Jika kurang dari, lompat ke label kurang_dari_10
    ; Kode yang dijalankan jika lebih dari atau sama dengan 10
    jmp selesai ; Lompat ke label selesai
kurang_dari_10:
    ; Kode yang dijalankan jika kurang dari 10
selesai:
    ; Kode setelah percabangan
Instruksi jl (jump if less) digunakan untuk melompat jika nilai eax kurang dari 10. Terdapat juga instruksi seperti je (jump if equal), jg (jump if greater), dan sebagainya untuk variasi kondisi lainnya.

c. Syntax untuk looping (while loop, for loop, dsb) beserta variasinya:
Looping dalam bahasa rakitan Intel x86 umumnya diimplementasikan menggunakan instruksi jump dan label. Berikut adalah contoh untuk while loop dan for loop:

While Loop:

assembly
Copy code
section .text
    xor ecx, ecx ; Inisialisasi counter
while_loop:
    cmp ecx, 5 ; Membandingkan nilai counter dengan 5
    jge  end_while ; Jika lebih atau sama dengan 5, keluar dari loop
    ; Kode yang dijalankan dalam loop
    inc ecx ; Increment counter
    jmp while_loop ; Lompat ke awal loop
    end_while:
    ; Kode setelah loop
For Loop:
section .text
    mov ecx, 0 ; Inisialisasi counter
    mov ebx, 5 ; Batas atas loop
for_loop:
    cmp ecx, ebx ; Membandingkan nilai counter dengan batas atas
    jge  end_for ; Jika lebih atau sama dengan, keluar dari loop
    ; Kode yang dijalankan dalam loop
    inc ecx ; Increment counter
    jmp for_loop ; Lompat ke awal loop
end_for:
    ; Kode setelah loop
d. Syntax untuk deklarasi fungsi dan pemanggilannya:
Deklarasi fungsi dan pemanggilannya dalam bahasa rakitan Intel x86 melibatkan penggunaan stack untuk menyimpan parameter dan alamat pengembalian. Contoh sederhana adalah sebagai berikut:
section .text

; Deklarasi fungsi
global main ; Fungsi utama (entry point program)
global my_function ; Deklarasi fungsi

my_function:
    ; Kode di dalam fungsi
    ret ; Instruksi pengembalian dari fungsi

section .text
    ; Fungsi utama
main:
    ; Pemanggilan fungsi
    call my_function
    ; Kode setelah pemanggilan fungsi
Instruksi call digunakan untuk memanggil fungsi, dan instruksi ret digunakan untuk kembali dari fungsi. Fungsi main sering digunakan sebagai entry point program.
