# Tugas writing week 4
# Day 1
Proses asynchronous sering digunakan untuk komunikasi data, karena data menjadi bagian inti dari sebuah aplikasi maka konsep asynchronous sangat penting untuk dipahami.

Pada konsep asynchronous, code akan dieksekusi tanpa menunggu eksekusi code lain selesai sehingga seakan-akan dieksekusi secara bersamaan.
- ## JavaScript Intermediate - Asynchronous - Fetch

  Fetch merupakan cara baru dalam melakukan network request. Pada dasarnya fungsi fetch memanfaatkan sebuah Promise, sehingga untuk menggunakan nya pastikan browser sudah mendukung ECMAScript 6 atau biasa disebut ES6. 
  
  Untuk menggunakan fetch, cukup gunakan keyword fetch() kemudian tuliskan URL yang akan dituju di dalam tanda kurung tersebut.
  
  ```
  fetch('<URL-to-the-resource-that-is-being-requested>');
  ```
  
  Karena fetch mengembalikan sebuah Promise, maka untuk response handling nya kita gunakan fungsi then (jika Promise tersebut mengembalikan resolve) dan catch (jika Promise tersebut mengembalikan reject)
  
  ```
  
        fetch('<URL-to-the-resource-that-is-being-requested>')
       .then(function (response) {
           return response.json()
       })
       .catch(function (err) {
           console.log(`Ups, ${err} :(`)
       })
  ```
  
  Dari kode diatas dapat disimpulkan seperti ini. Jika request pada fetch berhasil dilakukan, maka blok then akan terpanggil dan mengembalikan nilai objek sesuai response yang didapat. Apabila fungsi fetch gagal dilakukan, maka blok catch akan terpanggil dan menampilkan eror pada console.
  
- ## JavaScript Intermdiate - Asynchronous - Async Await

  Async/await adalah fitur yang hadir sejak ES2017. Fitur ini mempermudah kita dalam menangani proses asynchronous.Async/Await merupakan sebuah syntax khusus yang digunakan untuk menangani Promise agar penulisan code lebih efisien dan rapih. Async/Await terbagi menjadi Async dan Await
  
    - Async/Await adalah salah satu cara untuk mengatasai masalah asynchronous pada Javascript selain menggunakan callback dan promise.
    - Pada implementasi Async/Await, kita menggunakan kata kunci async sebelum fungsi. Await sendiri hanya bisa digunakan pada fungsi yang menggunakan async.
    - Untuk menggunakan Async/Await, kembalian dari suatu fungsi harus merupakan suatu Promise. Async/Await tidak dapat berdiri tanpa adanya Promise.
    - Tidak seperti Promise, dengan Async/Await maka suatu baris kode dapat tersusun rapi mirip dengan kode yang sifatnya synchronous.
    - Setiap baris yang menggunakan await, akan ditunggu sampai Asynchronous Promise tersebut di resolve.
 
 contoh
 ```
  const getAllUser = async ()=> {
	const data = await getUser()
	console.log(data)
}
```

Pada contoh diatas, pertama kita memiliki function dengan menambahkan async didepan function yang mana berfungsi untuk menjadikan function tersebut asynchronous, dan await berfungsi menunda eksekusi hingga proses asynchronous selesai, dari kode di atas berarti console.log(data) tidak akan di eksekusi sebelum proses getUser() selesai. await juga bisa digunakan berkali-kali di dalam function.

- # HTTP Request fetch()

Fetch adalah native web API untuk melakukan HTTP calls dari external network.

![image](https://user-images.githubusercontent.com/113356785/196038189-32b3e8d6-56c5-46d9-97a0-940884a3c1a3.png)

fetch() memiliki parameter utama yaitu URL/endpoint API, dan parameter kedua yaitu options, options ini berisi method, headers dan body. Tergantung keinginan.

![image](https://user-images.githubusercontent.com/113356785/196038215-3536440d-417f-42ea-9af1-75859ac0f440.png)

Contoh function untuk mengambil data dari API menggunakan fetch(), Promise based.

![image](https://user-images.githubusercontent.com/113356785/196038281-e2b838ba-1ebb-4bde-b443-8d4d2a4c4c5d.png)

Contoh function untuk mengambil data dari API menggunakan fetch(), Dengan Async Await.

# Day 2
- ## Git & Github Lanjutan
  - Kenapa harus menggunakan Git dan GitHub
  
  Dengan menggunakan GIT dan Github, kamu akan bisa bekerja dalam sebuat tim. Tujuan besarnya adalah kamu bisa berkolaborasi mengerjakan proyek yang sama tanpa harus repot copy paste folder aplikasi yang terupdate.
  
  Kamu juga tidak perlu menunggu rekan dalam satu tim kamu menyelesaikan suatu program dahulu untuk berkolaborasi. Kamu bisa membuat file didalam projek yang sama atau membuat code di file yang sama dan menyatukannya saat sudah selesai.
  - Perbedaan antara Git dan Github
  
  Git dan GitHub menangani commands secara berbeda

  Developer yang menggunakan Git dapat menggunakan command-line tool, yaitu pengubah kode dan dapat digabungkan menuju perangkat lokal. Sedangkan, GitHub menyediakan interface grafis berbasis cloud sebagai tempat untuk melakukan seluruh tugas.
  - Alur kerja dari Git dan Github
  
  cara kerja Git melibatkan beberapa file proyek yang tersimpan di direktori proyek. Kemudian, file yang tersimpan tadi akan diperbarui yang dipindah ke Staging Area. Setelah peninjauan, file kode tersebut dimuat ke Git Repository.
  
  Cara menggunakan GitHub pun cukup mudah:

   Membuat akun GitHub kemudian Memulai project baru dalam sebuah repository lalu Membuat dan mengedit file project selanjutnya Berkolaborasi dalam berbagai project open-source 
    
    
  - Membuat Repository Git
  
   Login Git. lalu Login Github. selanjutnya Buat Repository. Kemudian Buat Folder pada Windows. selanjutnya Buka Folder Menggunakan Git Bash. kemudian Ubah Folder Menjadi Repository. lalu Tambahkan File ke Repository. dan Buat Commit.
  - Melakukan commit pada Git
  
  commit adalah sebuah perintah GIT untuk mengubah staging atau register menjadi terdaftar sepenuhnya selain itu commit juga berguna sebagai history/riwayat mengenai apa yang kita rubah pada code kita.
![image](https://user-images.githubusercontent.com/113356785/196039773-da1dcb09-97c4-441b-b6d6-be8666e05531.png)
  - Melakukan merge pada Git
  
  Merge adalah suatu command dalam git untuk membuat branch yang bercabang menjadi satu kembali atau dengan kata lain mengintegrasikan kembali branch tersebut menjadi satu. Merge akan mengombinasikan beberapa tahapan commits menjadi satu branch yang terunifikasi.
  
  bagaimana cara kita melakukan merge?
    
   ![image](https://user-images.githubusercontent.com/113356785/196040139-9871bd9b-c051-4f14-8705-fc9940404491.png)

     kita telah berhasil melakukan merge secara manual.
  - Menyelesaikan conflict pada Git
  
  Pada suatu project yang memerlukan kolaborasi, terkadang kita membuat perubahan pada suatu file yang juga pihak lain sedang membuat perubahan. Sehingga nanti nya ketika melakukan git merge maka akan terjadi conflict.
  
  git menginginkan agar branch kamu dapat di merge dengan master branch maka kamu perlu melakukan resolve conflict.
Disinilah git rebase bisa menjadi solusi.

![image](https://user-images.githubusercontent.com/113356785/196040522-4ccfe766-f14a-4c74-a183-eca91bccf9f9.png)


  Disini git akan menginformasikan letak konflik dan kamu perlu meyelesaikan itu.
Edit file yang memiliki konflik tersebut. Setelah selesai:
  
  ![image](https://user-images.githubusercontent.com/113356785/196040561-d97bbcae-51e8-4571-8daf-8f221a6c51f6.png)


  Apabila sebelumnya branch fitur_a ini sudah menjadi pull_request yang ada di remote repository maka kamu bisa lakukan force push:
  
  ```
  git push -f <remote name> fitur_a
  ```
  - Mempublish aplikasi ke Github
  
  login ke akun github dan buat repository baru
  
  Mengisi Repository name: (Diisi nama repositorya) Desciption: (Diisi deskripsi repositorynya (tidak wajib)) lalu set Public, Private, default Public, lalu klik tombol berwarna hijau Create Repository.

  muncul halaman Create Repository ( ini berfungsi sebagai perintah command line\)
  
  Setelah itu buka project yang akan dimasukkan ke Github, caranya klik kanan pada folder project dan pilih Git Bash Here dan muncul command line
  
  Ketikkan perintah 
  ```
  echo "# Repository-Baru" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/brianetlab/Repository-Baru.git
git push -u origin master
```

  Project kamu sudah masuk ke Github!
  
  - Melakukan cloning Github ke local
  
  Langkah pertama kita harus mengakses link repository yang ingin kita clone
  
  Arahkan kursor ke bagian tombol Clone or download. Akan diberikan pilihan clone, yaitu Clone with SSH atau Clone use HTTPS.
  
  Selanjutnya kita copy link yang diberikan 
  
  Kini saatnya kita membuka terminal kita dan arahkan di directory mana akan kita simpan clone dari repository di github.
  
  Selanjutnya kita dapat menjalankan perintah git clone dengan menyertakan link yang sudah kita copy sebelumnya.
  
  Proses clone ini memerlukan koneksi internet, jadi pastikan jaringan internet yang anda gunakan dalam kondisi stabil.
  
  Kita dapat mengecek project yang sudah kita clone di directory yang kita pilih tadi.
  - Berkolaborasi dengan tim menggunakan Github
  
    1. Menambahkan Anggota Tim
    
      Organizations - Pemilik organisasi dapat membuat banyak tim dengan tingkat izin yang berbeda untuk berbagai repositori
      
      Collaborators - Pemilik repositori dapat menambahkan kolaborator dengan akses Baca + Tulis untuk satu repositori
      
        
    2. Pull Requests
      
      Pull Requests adalah cara yang mengagumkan untuk berkontribusi pada repositori secara mandiri dengan fork itu. Pada akhirnya, jika kita mau, kita dapat mengirim permintaan tarik ke pemilik repositori untuk menggabungkan perubahan kode kita. Pull request itu sendiri dapat memicu diskusi untuk kualitas kode, fitur atau bahkan strategi umum.
      
    3. Pelacakan Bug
    
    Di Github, pusat untuk semua pelacakan bug adalah Masalah. 
       
    4. Analytics
    
    Ada dua alat yang memberi wawasan tentang repositori - Grafik dan Jaringan. Github Graphs memberikan wawasan tentang kolaborator dan komitmen di balik setiap repositori kode, sementara Github Network menyediakan visualisasi pada setiap kontributor dan komitmennya di seluruh repositori bercabang. Analisis dan grafik ini menjadi sangat kuat, terutama ketika bekerja dalam tim.
    
    5. Manajemen Proyek
    
    Meskipun Masalah Github memiliki kemampuan manajemen proyek dengan Masalah dan Milestones, beberapa tim mungkin lebih memilih alat lain karena fitur lain atau alur kerja yang ada. Pada bagian ini, kita akan melihat bagaimana kita dapat menghubungkan Github dengan dua alat manajemen proyek populer lainnya - Trello dan Pivotal Tracker. Dengan kait layanan Github, kita dapat mengotomatiskan tugas pembaruan dengan komit, masalah, dan banyak aktivitas lainnya. Otomatisasi ini membantu tidak hanya menghemat waktu, tetapi juga meningkatkan akurasi dalam pembaruan untuk setiap tim pengembangan perangkat lunak.
    
    6. Continuous Integration
    
    Continuous Integration (CI) adalah bagian penting dari semua proyek pengembangan software yang bekerja dengan tim. CI memastikan bahwa, ketika seorang pengembang memeriksa dalam kode mereka, sebuah build otomatis (termasuk tes) mendeteksi kesalahan integrasi secepat mungkin. Ini jelas mengurangi kesalahan integrasi dan membuat iterasi cepat jauh lebih efisien.
    
    7. Code Review
    
    Dengan setiap commit, Github memungkinkan interface yang bersih untuk komentar umum atau bahkan komentar khusus pada baris kode. Kemampuan untuk mengajukan komentar atau pertanyaan pada setiap baris kode sangat berguna dalam melakukan tinjauan kode baris demi baris. Untuk melihat komentar inline, aktifkan kotak centang di kanan atas setiap commit.
    
    8. Documenting
    
    Di bagian ini, kita akan mengeksplorasi dua metode dokumentasi:

    Formal Documentation: Github Wiki untuk membuat dokumentasi untuk kode sumber
  
    Informal Documentation: Github Hubot untuk mendokumentasikan diskusi di antara anggota tim dan mengotomatiskan pengambilan informasi dengan berinteraksi dengan bot obrolan yang menyenangkan
  
  
# Day 3
- ## Responsive Web Design

  - Apa itu Responsive Web Design
  
  Responsive web design atau (RWD) adalah bertujuan membuat desain web kita dapat diakses dalam device apapun 
  
  - Tools untuk membuat website yang responsif
  
  Pada browser chrome biasa disebut dengan Chrome dev Tools
  
  ![image](https://user-images.githubusercontent.com/113356785/196042335-565fc6dc-1f8f-4fc8-8f1a-07f9523f4107.png)
  
  - viewport
  
  Viewport merupakan area yang dapat dilihat oleh pengguna kita pada halaman website. Ukuran viewport bervariasi berdasarkan peranti. Ukuran viewport pada sebuah peranti mobile, lebih kecil dibandingkan dengan layar komputer
  
  ![image](https://user-images.githubusercontent.com/113356785/196042438-77abeb8c-7f65-4e10-98fe-39621fb9b3de.png)

    Gambar diatas adalah Meta Viewport yang dibutuhkan pada responsive mobile
    
   ![image](https://user-images.githubusercontent.com/113356785/196042526-870c619f-05c2-4fca-8015-850568ee7613.png)

    Gambar diatas adalah HTML dengan Meta Viewport
   
  - Relative CSS Unit
  
  Ini adalah units yang mendapatkan nilainya dari beberapa nilai external lainnya. Ini berguna karena memungkinkan, misalnya, lebar gambar harus berdasarkan pada lebar browser.
  
  - Media Query
  
  Menggunakan Media Queries untuk meningkatkan mobile experience.
  
  Media Queries digunakan untuk membuat beberapa styles tergantung pada jenis device
  
  ada dua cara dalam menggunakan Media Queries
  
  pertama membuat file CSS berbeda untuk masing-masing device dan kedua menggabungkan 1 file CSS untuk setting styling erbagai device.
  
  - Flexbox dan Grid
  
  Flexbox mengubah konsep desain responsive ketika diperkenalkan beberapa tahun yang lalu, karena flexbox membuat website jauh lebih mudah untuk memposisikan element secara responsif di sepanjang sumbu. Untuk praktik menggunakan Flexbox kita akan membuat navbar di atas title.
  
  Sistem Grid adalah sistem layout dua dimensi yang berbasiskan row (baris) dan column (kolom). Tiap row memiliki width atau lebar sebesar 100% karena row merupakan sebuah baris, dan sebuah baris tidak diperuntukan bersejajar satu sama lainnya.
- ## Bootstrap 5

  - Bootstrap
  
  Bootstrap adalah framework yang digunakan untuk mempermudah dan mempercepat pembuatan halaman website. Kenapa mempercepat dan mempermudah, karena bootstrap sudah menyediakan css dan javascript yang siap pakai dan mudah dikembangkan.
  
  Tujuan dan fungsi Bootstrap adalah untuk membuat website responsive dan mobile-first. Jadi, semua elemen antarmuka website dipastikan bisa bekerja secara optimal di semua ukuran layar, baik desktop maupun perangkat seluler.
  
  Salah satu alasan Bootstrap sangat populer di kalangan developer dan desainer web adalah struktur filenya yang sederhana. File-filenya dikompilasi untuk akses yang mudah, dan hanya membutuhkan pengetahuan dasar HTML, CSS, serta JS untuk memodifikasinya.
  
  Untuk mempercepat loading website, Bootstrap memperkecil (minify) file CSS dan JavaScript. Selain itu, Bootstrap selalu menjaga konsistensi syntax di antara berbagai website dan para developer, yang membuatnya cocok untuk proyek kolaborasi tim.
  - layout pada Bootstrap
  
  Proses menciptakan fixed layout namun responsif pada dasarnya dimulai dengan kelas .container. Setelah itu kalian dapat membuat baris dengan kelas .row untuk wrap grup kolom horizontal. Baris harus ditempatkan di dalam .container untuk alignment dan padding yang tepat.

  Kolom lebih lanjut dapat dibuat di dalam baris menggunakan grid class yang telah ditentukan sebelumnya seperti .col-*, .col-sm-*, .col-md-*, .col-lg-* dan .col-xl-* di mana * mewakili nomor grid dan harus dari 1 hingga 12.
  
  - content pada Bootstrap
  
  CDN adalah singkatan dari Content Delivery Network, semacam server yang tersebar di seluruh dunia untuk mengantarkan konten secara optimal dan cepat.
  
  - component pada Bootstrap
  
  Beberapa komponen bootstrap telah tersedia dan dapat di gunakan sesuai kebutuhan, seperti : Accordion, Dropdown, Badge, Buttons, Card, Carousel, Navbar, Modal, Table, Form dan masih banyak lagi.
  
  - Website responsif menggunakan Bootstrap
  
   Bootstrap bersifat responsive berkat grid system yang digunakan. Sistem grid pada bootstrap menggunakan rangkaian containers, baris, dan kolom untuk menyesuaikan bentuk layout dan konten website kita. 
   
   unduh bootstrap, buat sebuah direktori baru lalu kemudian simpan hasil unduhan di folder tersebut.
   
   Di dalam folder bootstrap terdapat 2 sub folder yaitu css dan js yang berisikan file-file css dan library javascript.
   
   Buat juga folder gambar untuk menyimpan daftar gambar yang di perlukan pada template web responsive dengan bootstrap.
   
   Selanjutnya buat sebuah file dengan nama index.html melalui teks editor
   
   Kita bisa modifikasi untuk logo dan daftar menu pada bagian header serta bagian konten juga bisa kita sesuaikan dengan konten yang kita miliki.
   
   Saat jendela browser diperkecil sesuai dengan ukuran layar smartphone maka tampilan layout akan menyesuaikan dengan kebutuhan layar perangkat.

  
   Selanjutnya buatlah sebuah file baru dengan nama artikel.html.

   Halaman ini berfungsi untuk menampilkan detail isi artikel dari konten website kita.
