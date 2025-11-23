# Assignment: Vue.js – Simple To-Do List

## Identitas
- **Nama** : Putra Heryan Gagah Perkasa
- **NIM** : F1D022087

---

## Deskripsi Tugas
Pada tugas ini saya membuat aplikasi To-Do List sederhana menggunakan Vue.js.
Aplikasi memiliki fitur:
- Menambah tugas
- Menghapus tugas
- Menampilkan pesan saat daftar kosong
- Menggunakan reaktifitas dengan `ref()`

---

## Hasil

### 1. Screenshot Hasil Program
![WhatsApp Image 2025-11-23 at 10 35 34 PM](https://github.com/user-attachments/assets/1a30f78e-4c55-438f-a5e1-734dedd8ce3f)

### 2. Penjelasan Singkat

#### Cara kerja `addTask()`
Fungsi `addTask()` bekerja dengan cara memvalidasi input terlebih dahulu. Jika input tidak kosong, nilai dari variabel reaktif `newTask` akan ditambahkan ke dalam array `tasks` menggunakan metode `.push()`. Setelah itu, kolom input dikosongkan kembali dengan mengatur `newTask.value = ''`.

#### Bagaimana data ditampilkan menggunakan `v-for`
Data ditampilkan menggunakan direktif `v-for="(task, index) in tasks"`. Direktif ini melakukan *looping* pada array `tasks` dan merender elemen `<li>` untuk setiap tugas yang ada. Atribut `:key="index"` digunakan agar Vue dapat melacak identitas setiap elemen secara efisien.

#### Cara kerja tombol hapus
Tombol hapus menggunakan *event listener* `@click` yang memanggil fungsi `deleteTask(index)`. Fungsi ini menerima parameter index dari item yang diklik, lalu menggunakan metode JavaScript `splice(index, 1)` untuk menghapus item tersebut dari array `tasks`, yang secara otomatis memperbarui tampilan karena sifat reaktif Vue.
