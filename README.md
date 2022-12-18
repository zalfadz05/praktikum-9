# Nama  : Zalfa Dewi Zahrani
# Nim   : 312210320
# Kelas : TI.22.A3

# Python Exception

• Eksepsi (exception) merupakan suatu kesalahan (error) yang terjadi saat proses eksekusi program sedang berjalan.

• Secara umum, ketika skrip Python menemukan situasi yang tidak dapat diatasi, hal itu menimbulkan pengecualian.

• Exception adalah objek Python yang mewakili kesalahan.

# Syntax Error

• Syntax error bisa disamakan dengan kesalahan tata bahasa atau gramatika.

• Contoh kesalahan yang termasuk dalam kategori ini adalah menuliskan perintah yang sebenarnya tidak ada, lupa menuliskan tanda kurung kotak, tanda kurung bulat dan titik koma, serta salah mengeja variabel.

contoh:

              if x < 5
              File "<stdin>", line 1
              if x <5
              ^
SyntaxError : invalid syntax

# Fitur Exception

Python menyediakan dua fitur yang sangat penting untuk menangani kesalahan tak terduga dalam program dan menambahkan kemampuan debugging di dalamnya.

• Exception Handling

adalah suatu mekanisme penanganan flow normal program karena terjadi exception dengan melanjutkan flow ke code block lainnya. Kenapa harus menangani exception? Karena terjadi exception dan kita tidak tangani, maka
program akan berhenti.

• Assertions Exception

adalah sebuah peristiwa, yang terjadi selama pelaksanaan program yang mengganggu aliran normal instruksi program. Secara umum, ketika skrip Python menemukan situasi yang tidak dapat diatasi, hal itu menimbulkan pengecualian. Exception adalah objek Python yang mewakili kesalahan.

# Runtime Error

• Runtime error adalah error yang muncul ketika program dijalankan / run. Misal error pembagian dengan nol. Syntax error tidak bisa mengendus error ini karena memang tidak ada syntax yang dilanggar, namun ketika program dijalankan dan ada error ini maka program akan berhenti.
  
• Misalnya, bila kita membuka file yang tidak ada, maka akan muncul pesan kesalahan FileNotFoundError

• Bila kita membagi bilangan dengan nol akan muncul pesan ZeroDivisionError.

contoh:

                        print(0 / 0)
                        Traceback (most recent call last):
                        File "<stdin>", line 1, in <module>

ZeroDivisionError: integer division or modulo by zero

# Membangkitkan Exception dengan Rise

• Ada banyak tipe eksepsi di dalam python, yang semuanya bisa dibangkitkan baik pada saat penanganan kesalahan (error) atau bisa juga kita bangkitkan secara paksa dengan menggunakan perintah raise

contoh:

                          x = 10
                          if x > 5:
                          raise Exception('x should not exceed 5. The value of x was:
                          {}'.format(x))
                          Traceback (most recent call last):
                          File "<input>", line 4, in <module>

Exception: x should not exceed 5. The value of x was: 10

• Blok try memungkinkan kamu untuk menguji blok kode error.

• Blok except memungkinkan kamu menangani error.

• Ketika ada kesalahan maka kode di blok except akan dieksekusi, sebaliknya jika program tidak memiliki kesalahan maka blok except akan di abaikan.

contoh:

                          try:
                          #kode
                          except TipeEksepsi:
                          # Penanganan kesalahan

contoh code:

                          try:
                          with open('file.log') as file: 
                          read_data = file.read() 
                          except FileNotFoundError as fnf_error: 
                          print(fnf_error)

jika file log tidak ditemukan maka akan muncul pesan error

[Erno 2] No such file or directory: 'file.log'



  
  
