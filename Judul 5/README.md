# Calculator Scientific 

Kalkulator Scientific berbasis web yang dibuat dengan HTML, CSS, dan JavaScript dasar (tanpa framework).

## Penjelasan Kode

### 1. HTML
Bagian HTML membangun struktur tampilan kalkulator, terdiri dari:
- **Header**: Judul kalkulator
- **Display**: Menampilkan ekspresi dan hasil
- **Memory Bar**: Tombol memori (MC, MR, MS, M+, M−)
- **Buttons**: Tombol angka, operator, fungsi scientific, dan kontrol
- **History**: Riwayat perhitungan terakhir

### 2. CSS
Bagian CSS mengatur tampilan agar kalkulator terlihat modern dan minimalis (tema monokrom):
- Warna latar belakang, border, dan bayangan
- Grid tombol agar rapi dan responsif
- Efek hover dan active pada tombol
- Penyesuaian warna untuk tombol operator, fungsi, dan hasil

### 3. JavaScript
Bagian JavaScript mengatur seluruh logika kalkulator:

- **Variabel utama**:
	- `currentValue`: Menyimpan nilai yang sedang ditampilkan
	- `expression`: Menyimpan ekspresi matematika yang sedang dibangun
	- `waitingForOperand`: Status input operand/operator
	- `history`: Array riwayat perhitungan
	- `memory`: Menyimpan nilai memori kalkulator
	- `lastResult`: Hasil perhitungan terakhir

- **Fungsi utama**:
	- `updateDisplay()`: Memperbarui tampilan display, memori, dan history
	- `digit(d)`, `decimal()`: Input angka dan desimal
	- `addOperator(op)`: Menambah operator ke ekspresi, mengatur prioritas operator
	- `addFunction(fn)`, `applyFunction(fn)`: Menambah/menjalankan fungsi saintifik (sin, cos, tan, log, ln, akar, pangkat, faktorial, dll)
	- `insertConstant(constant)`: Memasukkan konstanta π atau e
	- `equals()`: Mengeksekusi ekspresi dan menampilkan hasil
	- `memoryStore()`, `memoryAdd()`, `memorySubtract()`, `memoryRecall()`, `memoryClear()`: Fungsi memori kalkulator
	- `clear()`, `clearEntry()`, `backspace()`: Kontrol input
	- `evaluateExpression(expr)`: Mengubah ekspresi ke format JavaScript dan menghitung hasil dengan prioritas operator yang benar

- **Keyboard Support**: Event listener untuk input dari keyboard (angka, operator, Enter, Escape, Backspace)

### 4. Logika Perhitungan
- Ekspresi matematika dibangun secara bertahap sesuai input user
- Operator dikonversi ke format JavaScript (`×` jadi `*`, `÷` jadi `/`, dll)
- Fungsi `evaluateExpression` menggunakan `Function` untuk menghitung ekspresi dengan prioritas operator yang benar
- Riwayat perhitungan disimpan dan ditampilkan
- Fungsi memori mengikuti standar kalkulator (MC hanya menghapus memori, bukan history)

## Kontributor
Proyek oleh Rendy Antono untuk "Tugas Akhir Praktikum Pemrograman Web".

---
