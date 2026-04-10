# StrukturData-Q1-2501010008-IPutuAdityaPerdana-A


---

 1. Karakteristik Memori dan Akses Data

 Array (O(1))
Menggunakan memori kontinu (berurutan). Karena ukurannya tetap dan letaknya berdampingan, komputer bisa langsung menghitung alamat memori elemen ke-n hanya dengan rumus matematika sederhana.

 Linked List (O(n))
Menggunakan memori non-kontinu (terpencar). Komputer tidak tahu di mana alamat elemen ketiga sebelum melewati elemen pertama dan kedua. Kita harus menelusuri rantai satu per satu.



 2. Analisis Efisiensi Operasi Manipulasi

Linked List lebih unggul saat kita sering melakukan penyisipan (insertion) atau penghapusan (deletion) di awal atau di tengah daftar.

Alasan:
Pada Array, jika kita menghapus elemen di tengah, semua elemen di belakangnya harus bergeser (shifting) untuk menutup celah. Pada Linked List, kita cukup mengubah arah "tali" (pointer) antar node tanpa menggeser data lainnya.



 3. Konsep Doubly Linked List

 Anatomi:
Satu node memiliki tiga bagian:
- Data  
- Pointer Next (ke depan)  
- Pointer Prev (ke belakang)  

 Dampak Memori:
Penggunaan memori lebih boros karena harus menyimpan dua alamat pointer di setiap node.

 Fleksibilitas:
Jauh lebih fleksibel karena kita bisa melakukan penelusuran dua arah (maju dan mundur), memudahkan operasi seperti menghapus node tepat sebelum node saat ini.



 4. Mekanisme Circular Linked List

 Perbedaan:
Pada Linked List biasa, node terakhir menunjuk ke NULL.  
Pada Circular Linked List, node terakhir menunjuk kembali ke node pertama (head).

 Use Case:
- Sistem Round Robin CPU Scheduling  
- Aplikasi pemutar musik (setelah lagu terakhir selesai, otomatis kembali ke lagu pertama tanpa henti)



 5. Array Dinamis di Python

Saat kapasitas penuh dan kita melakukan append, Python melakukan mekanisme over-allocation:

1. Membuat array baru dengan ukuran lebih besar (biasanya 1.5x atau 2x lipat)
2. Menyalin semua elemen dari array lama ke array baru
3. Menghapus array lama dari memori

Meskipun ada proses penyalinan, secara rata-rata (amortized), operasi ini tetap dianggap cepat.
