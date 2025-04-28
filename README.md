# Remedial-Perbaikan-Tugas-5-A

---

Praktikum ini bertujuan untuk membuat kalkulator sederhana yang dapat menghitung volume dan berat dua jenis bangun ruang, **Kerucut** dan **Balok**. Program ini mengimplementasikan konsep **Object-Oriented Programming (OOP)** seperti **polymorphism**, **inheritance**, dan **interface** di Java.

---

### **Deskripsi Program**
Program memungkinkan pengguna untuk memilih antara menghitung volume dan berat **Kerucut** atau **Balok**. Konsep **polymorphism** diterapkan untuk memungkinkan objek-objek ini diperlakukan sebagai **BangunRuang** yang umum. Output juga dilengkapi dengan warna menggunakan **ANSI escape codes**.

---

### **Struktur Program**
- **`HitungRuang` (Interface)**: Mendeklarasikan metode **hitungVolume()** dan **hitungBerat()**.
- **`BangunRuang` (Abstract Class)**: Menyimpan atribut **nama** dan **massa**, serta deklarasi metode **printInfo()**.
- **`Kerucut` dan `Balok` (Subclass)**: Mengimplementasikan **HitungRuang** untuk perhitungan volume dan berat.
- **`KalkulatorBangunRuangMini` (Main Program)**: Menyediakan menu untuk interaksi pengguna dengan pilihan bangun ruang dan perhitungan.

---

### **Polymorphism**
Polymorphism diterapkan di **`main()`** dengan deklarasi objek **Kerucut** dan **Balok** sebagai tipe **BangunRuang**, sehingga dapat menggunakan metode **printInfo()** meskipun implementasinya berbeda di masing-masing kelas.

---

### **Input dan Output**
Pengguna memasukkan data untuk menghitung volume dan berat bangun ruang. Program menampilkan hasil perhitungan dan informasi tambahan seperti garis pelukis untuk **Kerucut**. Output disertai pewarnaan untuk meningkatkan keterbacaan.

---

### **Implementasi OOP**
- **Abstraction**: Proses perhitungan volume dan berat disembunyikan dalam kelas masing-masing bangun ruang.
- **Encapsulation**: Atribut seperti **radius**, **tinggi**, **panjang**, dan **massa** dijaga agar bersifat **private**.
- **Inheritance**: **Kerucut** dan **Balok** mewarisi kelas **BangunRuang** untuk berbagi metode umum.
- **Polymorphism**: Program menggunakan **BangunRuang** untuk objek yang berbeda, sehingga memungkinkan pemanggilan metode yang sama meskipun objeknya berbeda.

---

### **Pengujian Program**
Contoh input:
```
Nama Kerucut    : Kerucut
Radius          : 7
Tinggi          : 14
Massa           : 5
```
Output:
```
Nama            : Kerucut
Volume          : 539.33
Berat           : 50.0
Garis pelukis   : 14.28
```

---

### **Kesimpulan**
Program berhasil menerapkan **OOP** dengan baik. **Polymorphism** memungkinkan penggunaan objek berbeda melalui tipe yang sama. Program berjalan sesuai ekspektasi dengan output yang terformat baik dan interaktif.

