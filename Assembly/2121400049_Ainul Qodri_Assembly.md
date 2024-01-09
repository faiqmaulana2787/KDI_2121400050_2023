1.	Dalam pemrograman komputer, bahasa assembly (ASM) adalah bahasa pemrograman tingkat rendah dengan korespondensi yang sangat kuat antara instruksi dalam bahasa dan instruksi kode mesin arsitektur. Bahasa assembly biasanya memiliki satu pernyataan per instruksi mesin (1:1). Kode assembly pertama kali muncul pada 1947 dalam "Coding for ARC." Pada awalnya, pemrograman bahasa assembly umum dilakukan untuk tujuan sistem dan aplikasi.
	
	Namun, seiring berjalannya waktu, peralihan ke bahasa tingkat tinggi meningkatkan produktivitas, keandalan, dan kesederhanaan perangkat lunak. Sekarang, bahasa assembly sering digunakan dalam sistem yang lebih besar yang diimplementasikan dalam bahasa tingkat tinggi, dengan penggunaan yang lebih terbatas, misalnya, untuk kinerja atau interaksi langsung dengan perangkat keras.

	Bahasa assembly menggunakan mnemonik untuk mewakili instruksi mesin, dan beberapa assembler memiliki instruksi makro untuk menyederhanakan kode. Ada dua jenis assembler berdasarkan jumlah lintasan yang diperlukan, yaitu assembler satu jalan dan assembler multi-lintasan.

	Dalam bahasa assembly, elemen dasarnya mencakup mnemonik opcode, definisi data, dan instruksi peassembly. Mnemonik opcode adalah simbol untuk instruksi mesin, sementara instruksi peassembly dapat mencakup instruksi makro dan pseudo-opcode. Arahan data digunakan untuk mendefinisikan elemen data, termasuk jenis, panjang, dan perataan data.

	Makro dalam konteks assembler adalah sekumpulan instruksi atau pernyataan yang dapat didefinisikan oleh pemrogram untuk kemudian digunakan sebagai satu kesatuan oleh assembler. Ini membantu mempermudah dan mempersingkat penulisan kode, menggantikan pemanggilan makro dengan sejumlah pernyataan assembler yang telah ditentukan sebelumnya.

	Dalam bahasa assembly, makro dapat digunakan untuk berbagai tujuan, seperti mendefinisikan makro itu sendiri, mendefinisikan variabel, mengatur variabel hasil dari operasi aritmatika atau logika, membuat pernyataan kondisional, atau menghasilkan kode berdasarkan parameter yang kompleks.

	Makro sering digunakan untuk membuat program bahasa assembly tampak lebih singkat dan lebih mudah dibaca, serta memberikan struktur yang lebih tinggi ke dalam program. Beberapa assembler bahkan mendukung fitur-fitur canggih pada makro, seperti parameter opsional, variabel simbolik, manipulasi string, dan operasi aritmatika. Makro juga memungkinkan penggunaan parameter, yang memungkinkan pengguna membuat instruksi assembler yang lebih umum dan dapat diulang.

	Dalam beberapa kasus, makro bahkan dapat digunakan untuk menghasilkan kode dalam bahasa yang benar-benar berbeda, memberikan tingkat abstraksi yang tinggi dan portabilitas pada program peassembly.

	Beberapa assembler juga memungkinkan makro untuk mengambil parameter, memberikan fleksibilitas tambahan dalam penggunaannya. Sebagai contoh, makro "pengurutan" dapat menerima spesifikasi kunci pengurutan yang kompleks dan menghasilkan kode yang sesuai dengan spesifikasi tersebut.

	Penting untuk memperhatikan bahwa penggunaan makro juga dapat menimbulkan tantangan, seperti bug yang mungkin muncul akibat penggunaan parameter yang salah atau penggunaan makro dalam konteks yang tidak sesuai. Substitusi parameter makro terutama bergantung pada nama, dan pemrosesan makro dapat menyebabkan ambiguitas jika tidak digunakan dengan hati-hati.

	Pada akhirnya, makro membantu pemrogram assembler untuk membuat kode yang lebih efisien, mudah dibaca, dan terstruktur dengan baik.

2.

a. Deklarasi Data Dasar:

- String:

  		myString db 'Halo, Dunia!', 0   ; String berakhir dengan null
- Integer:

  		myInt dd 42   ; Bilangan bulat 32-bit
- Boolean:

  		myBool db 1   ; 1 untuk benar, 0 untuk salah
- Float 32-bit:

  		myFloat dd 3.14   ; Bilangan floating-point 32-bit
b. Branching (if ... else ...):

	cmp eax, ebx         ; Compare values in eax and ebx
	je  equal_label      ; Jump if equal
	jne not_equal_label  ; Jump if not equal	
	jmp end_label        ; Unconditional jump
 
 	equal_label:
    	; Code for equal condition
    	jmp end_label
		 
	not_equal_label:
   		; Code for not equal condition

	end_label:
c. Looping (while loop, for loop, dsb):

- While Loop:

  		while_condition:
  			; Check condition
  			cmp ecx, 10
  			jge end_while

  			; Loop body
  			; ...

  			; Increment counter
  			inc ecx

  			; Jump back to the condition
  			jmp while_condition
		
		end_while:
- For Loop:

		mov ecx, 0   ; Initialize counter
  
  		for_condition:
		    ; Check condition
		    cmp ecx, 10
		    jge end_for
				
		    ; Loop body
		    ; ...
				
		    ; Increment counter
		    inc ecx
			
		    ; Jump back to the condition
		    jmp for_condition

  		end_for:
d. Deklarasi Fungsi dan Pemanggilannya:

	; Function declaration
	myFunction:
	    ; Function body
	    ; ...
	
	    ret   ; Return from function
	
	; Function call
	call myFunction
