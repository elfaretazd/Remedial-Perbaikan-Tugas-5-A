# Remedial-Perbaikan-Tugas-5-A

---

### 📌 1. Interface `HitungRuang`
- **Interface** ini berfungsi untuk mengatur bahwa semua bangun ruang wajib memiliki kemampuan menghitung **volume** dan **berat**.
- Terdapat dua method wajib: `hitungVolume()` dan `hitungBerat()`.
- Dengan interface ini, baik `Kerucut` maupun `Balok` dipaksa untuk mengimplementasikan cara menghitung volume dan berat masing-masing.

---

### 📌 2. Abstract Class `BangunRuang`
- `BangunRuang` adalah **abstract class** yang menjadi dasar bagi semua bentuk bangun ruang.
- Class ini memiliki **atribut** `nama` dan `massa` yang digunakan di semua bentuk.
- Selain itu, `BangunRuang` memiliki **method abstract** `printInfo()`, yang berarti setiap class anak seperti `Kerucut` dan `Balok` harus menyediakan implementasinya sendiri.

---

### 📌 3. Class `Kerucut`
- `Kerucut` adalah class **turunan** dari `BangunRuang` dan **mengimplementasikan** interface `HitungRuang`.
- Memiliki atribut **private** `radius` dan `tinggi`, serta konstanta `PI` sebesar 22/7.
- Disediakan **dua konstruktor**: default (`radius`, `tinggi` = 0) dan overload (mengisi semua data lewat input).
- `Kerucut` menghitung volume dengan rumus `(π × r² × t)/3`, berat dengan rumus `massa × 10`, serta garis pelukis menggunakan `√(r² + t²)`.
- Semua data objek dicetak menggunakan method `printInfo()`.

---

### 📌 4. Class `Balok`
- `Balok` juga merupakan **turunan** dari `BangunRuang` dan **mengimplementasikan** interface `HitungRuang`.
- Memiliki atribut **private** yaitu `panjang`, `lebar`, dan `tinggi`.
- Disediakan **dua konstruktor**: default (semua data 0) dan overload (input user).
- Volume balok dihitung dengan `panjang × lebar × tinggi`, dan berat = `massa × 10`.
- Informasi lengkap balok dicetak melalui method `printInfo()`.

---

### 📌 5. Main Class `KalkulatorBangunRuangMini`
- Class ini hanya berisi satu method yaitu `public static void main(String[] args)`.
- Di dalam `main()`, pertama dicetak **header** program dengan pewarnaan hijau.
- Dilakukan **pembuatan objek default** untuk `Kerucut` dan `Balok` menggunakan **polymorphism**, di mana tipe datanya adalah `BangunRuang` tapi objeknya adalah `Kerucut` atau `Balok`.
- Program menerima **input** dari user untuk membuat objek `Kerucut` dan `Balok` baru berdasarkan nilai yang dimasukkan.
- Setelah input, objek dicetak menggunakan method `printInfo()` yang otomatis menghitung volume, berat, dan garis pelukis (khusus untuk kerucut).
- Semua **pewarnaan output** (hijau, merah) hanya diatur di dalam `main()`, tidak di class lain, menggunakan **ANSI escape codes**.

---
