# <h1 align="center">Laporan Praktikum Modul Tipe Data</h1>
<p align="center">Egi Rizkiyansyah</p>

## Dasar Teori
1. Program untuk Menampilkan Output Berdasarkan Input Pengguna:

Dasar Teori:
Variabel dalam pemrograman memegang peran penting dalam menyimpan dan memanipulasi data. Mereka seperti wadah yang dapat diisi dengan nilai-nilai yang berbeda, memungkinkan program untuk berinteraksi dengan data secara dinamis. Deklarasi variabel biasanya melibatkan penentuan tipe data dan nama variabel yang unik.
Variabel lokal, seperti yang telah disebutkan sebelumnya, hanya dikenali di dalam blok kode tempat mereka dideklarasikan. Mereka biasanya digunakan untuk menyimpan nilai sementara atau variabel yang hanya relevan dalam konteks tertentu, seperti variabel yang hanya dibutuhkan dalam sebuah fungsi.
Variabel global, di sisi lain, dapat diakses dari mana pun dalam program. Mereka berguna untuk menyimpan informasi yang perlu diakses oleh banyak bagian dari program, tetapi penggunaan yang berlebihan dapat menyebabkan kompleksitas dan kesulitan dalam pemeliharaan program.
Struktur (Struct) 
adalah cara untuk menggabungkan beberapa tipe data menjadi satu kesatuan logis. Ini memungkinkan programmer untuk membuat tipe data khusus yang sesuai dengan kebutuhan mereka. Misalnya, sebuah struktur untuk merepresentasikan buku dapat memiliki anggota seperti judul, penulis, tahun terbit, dll.
Dengan menggunakan struktur, kita dapat membuat variabel yang memiliki tipe data struktur tersebut, dan kemudian mengakses setiap anggota struktur untuk membaca atau mengubah nilainya. Ini memungkinkan untuk merepresentasikan entitas yang lebih kompleks dalam program, dengan setiap variabel struktur memiliki properti dan perilaku yang terkait dengannya.
Pemahaman konsep variabel dan struktur sangat penting dalam pengembangan perangkat lunak, karena mereka membentuk dasar dari bagaimana data disimpan, diakses, dan dimanipulasi dalam program. Dengan pemahaman yang baik tentang konsep ini, programmer dapat membuat kode yang lebih efisien, mudah dimengerti, dan mudah dipelihara.

## Guided 

### 1. [Program Input Array Struct data buku]

```C++

#include <iostream>
using namespace std;

// Mendefinisikan struktur buku
struct buku {
    string judulBuku;
    string pengarang;
    string penerbit;
    int tebalHalaman;
    int hargaBuku;
};

int main() {
    // Mendeklarasikan variabel favorit dengan tipe buku
    buku favorit;

    // Mengisi data ke dalam variabel favorit
    favorit.judulBuku = "The Alpha Girl's Guide";
    favorit.pengarang = "Henry Manampiring";
    favorit.penerbit = "Gagas Media";
    favorit.tebalHalaman = 253;
    favorit.hargaBuku = 79000;

    // Menampilkan informasi buku favorit
    cout << "\tBuku Favorit Saya" << endl;
    cout << "\tJudul Buku : " << favorit.judulBuku << endl;
    cout << "\tPengarang : " << favorit.pengarang << endl;
    cout << "\tPenerbit : " << favorit.penerbit << endl;
    cout << "\tTebal Halaman: " << favorit.tebalHalaman << " halaman" << endl;
    cout << "\tHarga Buku : Rp " << favorit.hargaBuku << endl;
 
    return 0;
}
```
#### Full code Screenshot:
![Screenshot 2024-04-28 190128](https://github.com/egirizkiyan/egirizkiyansyah/assets/162097461/2f542792-c12c-4a87-afbe-5733b006c57c)

#### Output:
![Screenshot 2024-04-28 190445](https://github.com/egirizkiyan/egirizkiyansyah/assets/162097461/fcecf4d4-fbdb-4255-afdd-7a939f534c46)

Kode tersebut adalah contoh penggunaan struktur (struct) dalam bahasa pemrograman C++. Struktur digunakan untuk mengelompokkan beberapa tipe data menjadi satu kesatuan logis, memungkinkan untuk merepresentasikan objek kompleks dalam program.
Dalam kode tersebut, sebuah struktur bernama buku didefinisikan, yang memiliki beberapa atribut seperti judul buku, pengarang, penerbit, tebal halaman, dan harga buku. Kemudian, sebuah variabel favorit dari tipe buku dideklarasikan di dalam fungsi main(), dan informasi tentang buku favorit dimasukkan ke dalam variabel tersebut.
Selanjutnya, informasi tersebut ditampilkan ke layar menggunakan cout, sehingga pengguna dapat melihat detail buku favorit. Setelah semua informasi ditampilkan, program mengembalikan nilai 0, menandakan bahwa program telah selesai dijalankan tanpa ada masalah.
Dengan menggunakan struktur, kode tersebut menjadi lebih terstruktur dan mudah dipahami, karena memungkinkan untuk mengelompokkan informasi yang terkait bersama-sama. Ini adalah contoh bagaimana struktur dapat digunakan untuk mengorganisir dan memanipulasi data dengan lebih baik dalam program.

### 2. [Program Mencari Nilai Array struktur data hewan]

```C++
#include <iostream>
using namespace std;

struct hewan {
    string namaHewan;
    string jenisKelamin;
    string caraBerkembangbiak;
    string alatPernafasan;
    string tempatHidup;
    bool Karnivora;
};

struct hewanDarat {
    int jumlahKaki;
    bool menyusui;
    string suara;
};

struct hewanLaut {
    string bentukSirip;
    string bentukPertahananDiri;
};

int main() {
    hewanDarat kelinci; // Menggunakan tipe data hewanDarat untuk kelinci
    kelinci.jumlahKaki = 4;
    kelinci.menyusui = true;
    kelinci.suara = "Citcit";

    hewanLaut ikan; // Menggunakan tipe data hewanLaut untuk ikan
    ikan.bentukSirip = "Sirip ekor";
    ikan.bentukPertahananDiri = "Sisik";

    hewan serigala; // Tetap menggunakan tipe data hewan untuk serigala
    serigala.namaHewan = "Serigala";
    serigala.jenisKelamin = "Jantan";
    serigala.caraBerkembangbiak = "Melahirkan";
    serigala.alatPernafasan = "Paru-paru";
    serigala.tempatHidup = "Hutan terbuka";
    serigala.Karnivora = true;

    cout << "\t\tHewan" << endl;
    cout << "\t" << serigala.namaHewan << endl;
    cout << "\tJenis kelamin : " << serigala.jenisKelamin << endl;
    cout << "\tCara berkembangbiak : " << serigala.caraBerkembangbiak << endl;
    cout << "\tAlat pernafasan : " << serigala.alatPernafasan << endl;
    cout << "\tTempat hidup : " << serigala.tempatHidup << endl;
    cout << "\tKarnivora : " << (serigala.Karnivora ? "Yes" : "No") << endl << endl;

    cout << "\t\tHewan Darat" << endl;
    cout << "\tKelinci" << endl;
    cout << "\tJumlah kaki : " << kelinci.jumlahKaki << endl;
    cout << "\tMenyusui : " << (kelinci.menyusui ? "Yes" : "No") << endl;
    cout << "\tSuara : " << kelinci.suara << endl << endl;

    cout << "\t\tHewan Laut" << endl;
    cout << "\tIkan" << endl;
    cout << "\tBentuk sirip : " << ikan.bentukSirip << endl;
    cout << "\tBentuk pertahanan diri: " << ikan.bentukPertahananDiri << endl;

    return 0;
}
```
#### Full code Screenshot:
![Screenshot 2024-04-28 192153](https://github.com/egirizkiyan/egirizkiyansyah/assets/162097461/1d2d2847-3fbf-441e-81e9-afab373bbd97)

#### Output:
![Screenshot 2024-04-28 192454](https://github.com/egirizkiyan/egirizkiyansyah/assets/162097461/e565f6bd-a6b9-4147-8eb3-92109240c106)

Kode tersebut menggunakan struktur (struct) dalam bahasa pemrograman C++ untuk mengorganisir informasi tentang hewan, baik itu hewan darat maupun laut. Berikut adalah kesimpulan yang lebih jelas:

Definisi Struktur:
- hewan: Mendefinisikan atribut umum untuk semua jenis hewan.
- hewanDarat: Menyimpan atribut spesifik untuk hewan darat.
- hewanLaut: Menyimpan atribut spesifik untuk hewan laut.
Deklarasi Variabel:
- Variabel kelinci dan ikan dideklarasikan menggunakan tipe data yang sesuai dengan lingkungan hidup hewan tersebut, yaitu hewanDarat dan hewanLaut.
- Variabel serigala tetap menggunakan tipe data hewan.
Inisialisasi Atribut:
- Setiap atribut dari variabel diinisialisasi dengan nilai yang sesuai.
Output Informasi:
- Informasi tentang setiap hewan, baik hewan darat maupun laut, ditampilkan dengan menggunakan cout.
Setiap atribut dari setiap hewan diakses dan ditampilkan sesuai dengan format yang diinginkan.
Dengan menggunakan struktur, program dapat menyimpan dan mengelola informasi tentang berbagai jenis hewan dengan cara yang terstruktur dan terorganisir. Ini memudahkan pemahaman tentang data yang disimpan dan meningkatkan keterbacaan serta pemeliharaan kode.

## Unguided 
### 1. [Soal]

```C++
#include <iostream>
#include <string> // Untuk menggunakan std::string

// Mendefinisikan struct buku
struct buku {
    std::string judulBuku;
    std::string pengarang;
    std::string penerbit;
    int tebalHalaman;
    float hargaBuku;
};

int main() {
    // Mendeklarasikan objek dari struct buku
    struct buku favorit;

    // Mengisi data ke dalam objek struct buku
    favorit.judulBuku = "The Alpha Girl's Guide";
    favorit.pengarang = "Henry Manampiring";
    favorit.penerbit = "Gagas Media";
    favorit.tebalHalaman = 253;
    favorit.hargaBuku = 79000;

    // Menampilkan data dari objek struct buku
    std::cout << "\tBuku Favorit Saya" << std::endl;
    std::cout << "\tJudul Buku : " << favorit.judulBuku << std::endl;
    std::cout << "\tPengarang : " << favorit.pengarang << std::endl;
    std::cout << "\tPenerbit : " << favorit.penerbit << std::endl;
    std::cout << "\tTebal Halaman: " << favorit.tebalHalaman << " halaman" << std::endl;
    std::cout << "\tHarga Buku : Rp " << favorit.hargaBuku << std::endl;

    return 0;
}

```
#### Output:
![Screenshot 2024-04-28 193758](https://github.com/egirizkiyan/egirizkiyansyah/assets/162097461/7447675e-01c0-4a11-a291-e20c7e5a21cd)

#### Full code Screenshot:
![Screenshot 2024-04-28 193636](https://github.com/egirizkiyan/egirizkiyansyah/assets/162097461/a4909251-1386-4f41-923d-ab98b3af7e93)

Kode di atas adalah contoh penggunaan struktur (struct) dalam bahasa pemrograman C++. Berikut adalah kesimpulan dari kode tersebut:

1. Definisi Struktur buku:
  - Struktur buku memiliki beberapa atribut yang mencakup informasi tentang buku, seperti judul, pengarang, penerbit, tebal halaman, dan harga.
2. Deklarasi Objek Struct:
  - Objek favorit dari tipe buku dideklarasikan di dalam fungsi main().
3. Inisialisasi Atribut Objek Struct:
  - Setiap atribut dari objek favorit diisi dengan nilai yang sesuai menggunakan operator ..
4. Output Informasi:
  - Informasi tentang buku favorit ditampilkan ke layar menggunakan std::cout. Setiap atribut dari objek favorit diakses dan ditampilkan sesuai dengan format yang diinginkan.

Keseluruhan, kode tersebut memberikan gambaran bagaimana struktur digunakan untuk mengorganisir data yang terkait bersama-sama dalam bahasa C++. Dalam kasus ini, struktur digunakan untuk merepresentasikan informasi tentang buku, memungkinkan untuk menyimpan dan mengakses data dengan lebih terstruktur dan terorganisir.


### 2. [Soal]

```C++
#include <iostream>
#include <string>

using namespace std;

// Mendefinisikan struktur buku
struct buku {
    string judulBuku;
    string pengarang;
    string penerbit;
    int tebalHalaman;
    int hargaBuku;
};

int main() {
    // Mendeklarasikan array dari struktur buku dengan ukuran 5
    buku array_buku[5];

    // Mengisi data ke dalam array dari struktur buku
    for (int i = 0; i < 5; i++) {
        array_buku[i].judulBuku = "The Alpha Girl's Guide";
        array_buku[i].pengarang = "Henry Manampiring";
        array_buku[i].penerbit = "Gagas Media";
        array_buku[i].tebalHalaman = 253;
        array_buku[i].hargaBuku = 79000;
    }

    // Menampilkan data dari array dari struktur buku
    cout << "Data Buku:\n";
    for (int i = 0; i < 5; i++) {
        cout << "Buku ke-" << i + 1 << endl;
        cout << "Judul: " << array_buku[i].judulBuku << endl;
        cout << "Pengarang: " << array_buku[i].pengarang << endl;
        cout << "Penerbit: " << array_buku[i].penerbit << endl;
        cout << "Tebal Halaman: " << array_buku[i].tebalHalaman << " halaman" << endl;
        cout << "Harga Buku: Rp " << array_buku[i].hargaBuku << endl;
        cout << endl;
    }

    return 0;
}

```
#### Output:
![Screenshot 2024-04-28 194422](https://github.com/egirizkiyan/egirizkiyansyah/assets/162097461/638d9f3e-99df-484e-a54a-13983c636cbf)

#### Full code Screenshot:
![Screenshot 2024-04-28 194306](https://github.com/egirizkiyan/egirizkiyansyah/assets/162097461/5a4dfb4d-5a54-4074-b867-69a888b46b1b)

Kode di atas merupakan contoh penggunaan struktur (struct) dalam C++ dengan array. Berikut adalah kesimpulan dari kode tersebut:

1. Definisi Struktur buku:
  - Struktur buku memiliki beberapa atribut yang mencakup informasi tentang buku, seperti judul, pengarang, penerbit, tebal halaman, dan harga.
2. Deklarasi Array dari Struktur buku:
  - Array array_buku dari tipe buku dideklarasikan dengan ukuran 5 di dalam fungsi main().
3. Inisialisasi Data ke dalam Array dari Struktur buku:
  - Dalam loop for, setiap elemen dari array array_buku diisi dengan data yang sama tentang buku favorit menggunakan operator ..
4. Output Informasi dari Array Struktur buku:
  - Setelah data diisi, informasi tentang setiap buku dalam array array_buku ditampilkan ke layar menggunakan cout.
Setiap atribut dari setiap buku diakses dan ditampilkan sesuai dengan format yang diinginkan.

Keseluruhan, kode tersebut menunjukkan bagaimana struktur dan array dapat digunakan bersama untuk menyimpan dan mengelola informasi yang terstruktur dalam C++. Dengan pendekatan ini, program dapat dengan efisien mengelola kumpulan data yang terkait, seperti dalam kasus ini, kumpulan informasi tentang buku-buku yang berbeda.

## Kesimpulan
Kesimpulan dari ketiga program di atas adalah sebagai berikut:

Program Membuat struct data buku dan hewan dalam Array:

Dalam kode tersebut, terdapat definisi dari sebuah struktur yang disebut buku. Struktur ini memiliki beberapa atribut seperti judul, pengarang, penerbit, tebal halaman, dan harga buku. Kemudian, dalam fungsi main(), sebuah array dari struktur buku dengan ukuran 5 dideklarasikan.
Selanjutnya, dalam loop for, setiap elemen dari array tersebut diisi dengan data yang sama tentang buku favorit menggunakan operator .. Setelah semua data diisi, program menampilkan informasi tentang setiap buku dalam array tersebut. Setiap atribut dari setiap buku diakses dan ditampilkan sesuai dengan format yang diinginkan.
Dengan menggunakan struktur dan array bersama-sama, program dapat dengan mudah mengelola kumpulan data yang terstruktur, seperti dalam kasus ini, kumpulan informasi tentang beberapa buku. Ini meningkatkan efisiensi dan keterbacaan kode, serta memudahkan pengelolaan dan manipulasi data.
tentu! Mari kita tambahkan lebih banyak analisis pada kode tersebut:

1. Struktur untuk Representasi Data: Penggunaan struktur buku memungkinkan untuk mengorganisir informasi tentang sebuah buku dalam satu entitas yang terstruktur. Dengan cara ini, setiap buku direpresentasikan sebagai satu objek yang memiliki atribut-atributnya sendiri.
2. Deklarasi dan Pengisian Array: Dengan mendeklarasikan array array_buku dari tipe buku, program dapat menyimpan informasi tentang beberapa buku dalam satu struktur data yang terorganisir. Dalam loop for, setiap elemen array diisi dengan data yang sama, yang menghasilkan kumpulan data tentang buku-buku favorit.
3. Penggunaan Loop untuk Akses Data: Penggunaan loop for untuk mengakses dan menampilkan informasi tentang setiap buku dalam array memungkinkan program untuk secara efisien menangani kumpulan data yang besar. Dengan menggunakan loop, program dapat secara otomatis menampilkan informasi tentang setiap buku tanpa perlu menulis kode yang sama berkali-kali.
4. Output Informasi yang Terstruktur: Informasi tentang setiap buku, seperti judul, pengarang, penerbit, tebal halaman, dan harga, ditampilkan secara terstruktur dan mudah dibaca. Ini membuat output menjadi informatif dan dapat dipahami dengan mudah oleh pengguna.
5. Manfaat dari Penggunaan Struktur dan Array: Dengan menggunakan struktur dan array bersama-sama, program dapat mengelola data yang terkait secara efisien dan terorganisir. Pendekatan ini mempermudah untuk mengelola, menyimpan, dan mengakses informasi tentang kumpulan data yang besar, seperti dalam kasus ini, informasi tentang beberapa buku.
Dengan demikian, kode tersebut mengilustrasikan bagaimana struktur dan array dapat digunakan untuk mengorganisir dan mengelola data yang terstruktur dalam bahasa pemrograman C++. Ini adalah pendekatan yang umum digunakan dalam pengembangan perangkat lunak untuk mengelola informasi yang kompleks dan terstruktur.

## Referensi
[1] Novi Anisa. (2021). Penggunaan variabel array dalam pengolahan data. Digilib Unila. [PDF] penggunaan variabel array dalam pengolahan data - Digilib Unila
[2] Khotibul Umam. (2023). ALGORITMA DAN PEMROGRAMAN KOMPUTER DENGAN PYTHON. Tujuan dan Capaian Pembelajaran. Setelah mempelajari materi dalam bab ini, mahasiswa diharapkan mampu menjelaskan dan mengimplementasikan tipe data array. b.
[3] Novi Anisa(2020, September 18). Belajar Python: Mengenal Array pada Bahasa Pemrograman Python. DQLab.