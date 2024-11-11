# Praktikum 1

**1. Jelaskan maksud dari langkah 4 pada praktikum tersebut! Mengapa dilakukan demikian?**

membuat file data_layer.dart  untuk menggabungkan ekspor model plan.dart dan task.dart.Tujuannya agar proses impor  lebih mudah dan bersih sehingga Anda hanya perlu mengimpor satu file data_layer.dart untuk mengakses semua model yang Anda perlukan.Hal ini membuat kode Anda lebih efisien, mudah dipelihara, dan  mudah dibaca.

**2. Mengapa perlu variabel plan di langkah 6 pada praktikum tersebut? Mengapa dibuat konstanta ?**

Variabel plan pada langkah 6 diperlukan untuk menyimpan data plan yang berisi daftar tugas di aplikasi Anda.Variabel-variabel ini digunakan untuk mengedit dan memperbarui informasi jadwal sepertI
Menambah tugas baru atau mengubah status tugas.

Nilai default seperti nama dan daftar tugas ditetapkan melalui konstruktor saat objek Plan dibuat, sehingga dibuat sebagai konstanta.
Konstanta memastikan bahwa nilai awal suatu objek tidak dapat diubah setelah  dibuat, sehingga menjaga integritas data dan mencegah perubahan yang tidak perlu.

**SCREENSHOOT HASIL PRAKTIKUM 1**

![2](https://github.com/user-attachments/assets/5dba3e7c-4241-4be4-a6db-1c3853c101af)

**3. Apa kegunaan method pada Langkah 11 dan 13 dalam lifecyle state ?**

Pada Langkah 11 dan Langkah 13, dua metode penting dalam siklus hidup StatefulWidget digunakan, yaitu initState() dan dispose().

initState() (Langkah 11): Metode ini dipanggil satu kali ketika State pertama kali dibuat. Di tahap ini, 
kita menginisialisasi variabel seperti scrollController dan menambahkan listener untuk menangani peristiwa scroll. 
initState() memastikan bahwa konfigurasi awal untuk scroll controller dilakukan sebelum widget ditampilkan.

dispose() (Langkah 13): Metode ini dipanggil saat State widget sudah tidak digunakan lagi, biasanya ketika widget dihapus dari widget tree. 
Pada tahap ini, kita membebaskan sumber daya dengan membersihkan scrollController menggunakan dispose() agar terhindar dari kebocoran memori dan melepaskan sumber daya yang dimanfaatkan oleh controller.

# Praktikum 2

**Jelaskan mana yang dimaksud InheritedWidget pada langkah 1 tersebut! Mengapa yang digunakan InheritedNotifier?**

Pada langkah 1, InheritedWidget adalah widget yang memungkinkan data diteruskan ke widget anak tanpa perlu meneruskannya secara manual. 
InheritedNotifier adalah subclass dari InheritedWidget yang dirancang khusus untuk menangani perubahan data dengan menggunakan ValueNotifier untuk mengelola perubahan state. 
Ini memungkinkan widget yang bergantung padanya secara otomatis memperbarui UI ketika data berubah, sehingga pengelolaan state menjadi lebih efisien dan sederhana.

**Jelaskan maksud dari method di langkah 3 pada praktikum tersebut! Mengapa dilakukan demikian?**

Tujuan penambahan kedua metode ini adalah untuk memudahkan perhitungan dan tampilan status progres dari task dalam Plan.
Dengan metode ini, kita dapat langsung menampilkan jumlah task yang selesai dan progres keseluruhan tanpa perlu menghitungnya berulang kali di bagian lain kode, 
sehingga logika aplikasi menjadi lebih terstruktur dan efisien.

**SCREENSHOT HASIL PRAKTIKUM 2**

![3](https://github.com/user-attachments/assets/f4e9c007-31dc-4bf3-beb4-2943d0e48061)

# Praktikum 3

**Berdasarkan Praktikum 3 yang telah Anda lakukan, jelaskan maksud dari gambar diagram berikut ini!**

![image](https://github.com/user-attachments/assets/5765be11-3b3f-4486-9e37-fb8a58b86254)

Diagram ini menunjukkan struktur hirarki widget pada dua layar aplikasi yang dihubungkan melalui Navigator.push.

Diagram Kiri:

- Ini adalah hirarki widget dari layar PlanCreatorScreen.

- Hierarki dimulai dari MaterialApp, yang membungkus seluruh aplikasi.

- PlanProvider digunakan sebagai pengelola state yang menyediakan data atau state ke widget anaknya.

- PlanCreatorScreen adalah widget utama dari layar ini, dan di dalamnya terdapat widget Column.

- Di dalam Column, ada TextField untuk input teks dan Expanded yang berisi ListView untuk menampilkan daftar item atau tugas.

Diagram Kanan:

- Ini adalah struktur widget dari layar PlanScreen yang ditampilkan setelah Navigator.push dipanggil dari PlanCreatorScreen.

- MaterialApp tetap membungkus keseluruhan aplikasi, tetapi di sini langsung diikuti oleh PlanScreen sebagai widget utama layar ini.

- Scaffold digunakan untuk menyediakan struktur dasar layar, seperti app bar, body, dan lainnya.

- Di dalam Scaffold, ada widget Column yang mengatur tata letak vertikal widget.

- Column ini berisi dua widget: Expanded yang membungkus ListView (untuk menampilkan daftar) dan SafeArea yang membungkus Text (untuk menampilkan teks), 
  yang memastikan teks tidak terhalang oleh area layar yang sensitif, seperti notch atau status bar.

Diagram ini menggambarkan bagaimana aplikasi berpindah dari satu layar ke layar lain. Navigator.push digunakan untuk navigasi dari PlanCreatorScreen ke PlanScreen, yang memiliki antarmuka lebih lengkap dengan elemen Scaffold dan SafeArea untuk memastikan konten tampil dengan aman di berbagai ukuran layar.

**SCREENSHOOT HASIL PARKTIKUM 3**

![4](https://github.com/user-attachments/assets/c4395301-6d5c-4c9d-9997-d515851c37d6)
