# StrukturData-Q1-2501010019-DewaGiri-A

**1. Karakter Memori dan Akses Data**
        
Pada Array, data yang disimpan akan diurutkan(kontinu) di memori, jadi setiap elemen memiliki posisi yang jelas dan bisa langsung diakses pakai index, sehingga aksesnya bisa cepat atau konstan O(1) karena cuma tinggal hitung alamat saja. sedangkan pada Singly Linked List, data yang disimpan tidak berurutan(non kontinu) di memori melainkan setiap elemen/node akan dihubungkan lewat pointer. jadi misal mau mengakses suatu elemen, akan di cek dari awal(head) satu persatu, sehingga waktunya jadi linear O(n)  
    
**2. Analisis Efisiensi Operasi Manipulasi** 

Linked List lebih diunggulkan dibanding Array dalam operasi penyisipan dan penghapusan. pada Array, karena disimpan secara kontigu, jika terjadi penyisipan atau penghapusan maka elemen setelahnya harus digeser untuk menjaga urutan sehingga disini membutuhkan lebih banyak waktu O(n) sedangkan pada LinkedList karena disimpan tidak berurutan(non kontigu) maka cukup mengubah pointernya saja tanpa menggeser elemen lain

**3. Konsep Doubly Linked List** 

Pada Doubly Linked List, tiap node nya terdiri dari tiga bagian utama, yaitu data, pointer ke node berikutnya (next), dan pointer ke node sebelumnya (prev), berbeda dengan Singly Linked List yang cuma punya satu pointer, disini setiap node tahu pasangan di depan dan di belakangnya. Adanya Pointer tambahan (prev) ini berdampak pada sisi memori dimana Doubly Linked List membutuhkan ruang lebih besar karena setiap node menyimpan dua pointer, bukan satu. lalu dari sisi fleksibilitas, struktur ini jauh lebih unggul karena traversal bisa dilakukan dua arah, maju dan mundur. Selain itu, operasi seperti penghapusan node di tengah menjadi lebih mudah karena tidak perlu mencari node sebelumnya terlebih dahulu (karena ada pointer prev). Jadi, meskipun lebih boros memori, Doubly Linked List lebih fleksibel dibanding Singly Linked List.

**4. Mekanisme Circular Linked List**

Perbedaan utama antara Circular Linked List dan Linked List biasa adalah pada node terakhirnya. Pada Linked List biasa, node terakhir menunjuk ke NULL yang menandakan akhir list, Sedangkan pada Circular Linked List node terakhir justru menunjuk kembali ke node pertama (head), sehingga membentuk struktur melingkar sehingga tidak ada elemen yang benar-benar menjadi “akhir” karena traversal bisa terus berputar. Hal ini juga membuat kita tidak perlu mengecek NULL saat melakukan iterasi, tetapi bisa juga terjadi loop tak berujung. Salah satu contoh use case yang cocok adalah pada sistem round robin, karena setiap proses dijalankan secara bergiliran dalam siklus. Circular Linked List efektif karena setelah proses terakhir selesai, sistem bisa langsung kembali ke proses pertama tanpa perlu reset atau penanganan khusus.

**5. Array Dinamis di Python (Python List)**

Python list sebenarnya diimplementasikan sebagai dynamic array dan ukuran array bisa bertambah secara otomatis saat dibutuhkan. Saat kita melakukan operasi append tapi kapasitas array sudah penuh, maka Python akan membuat array baru dengan ukuran yang lebih besar, lalu semua elemen dari array lama akan disalin ke array baru. Kemudian elemen baru dimasukkan, dan array lama akan dibuang atau dihapus. Mekanisme ini membuat operasi append secara umum memiliki kompleksitas amortized O(1), karena tidak setiap append memicu resize. Namun, saat resize terjadi, prosesnya menjadi O(n) karena harus menyalin seluruh elemen. Jadi, kelebihan dynamic array adalah fleksibilitas dan kemudahan penggunaan, tapi dengan trade-off berupa kemungkinan penggunaan memori lebih besar dari yang sebenarnya dibutuhkan dan adanya biaya mahal saat resizing.

