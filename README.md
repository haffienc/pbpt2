# Barang Gelap

Nama: Haffie Noorcahyo

NPM: 2206081515

Kelas: PBP A

Link Adaptable: https://barang-gelap.adaptable.app/

# TUGAS 2
# mengimplementasikan checklist secara step-by-step
- membuat direktori baru bernama Tugas2
- mengaktifkan virtual enviroment
- membuat berkas requirements.txt dengan isi isinya
- membuat repositori bernama pbpt2 di github
- membuat project django
- menambahkan ["*"] pada variable ALLOWED_HOST di settings.py
- mengunggah proyek ke repositori dengan menambah berkas .gitignore
- membuat Aplikasi main dalam Tugas2 dengan python manage.py startapp main
- mendaftarkan aplikasi main ke dalam proyek dengan cara menambah 'main' di INSTALLED_APPS pada berkas settings.py
- membuat direktori templates dalam main
- membuat berkas main.html dalam berkas templates dengan isi sesuai ketentuan
- buka dan isi berkas models.py sesuai ketentuan
- melakukan migrasi model untuk melacak perubahan pada model dengan python manage.py makemigration untuk menciptakan berkas migrasi yang berisi perubahan model dan python manage.py migrate untuk mengaplikasikan perubahan model yang tercantum dalam berkas migrasi ke basis data
- buka berkas views.py tambahkan from django.shortcuts import render. tambahkan fungsi show_main dan ubah isinya sesuai ketentuan soal
- modifikasi berkas main.html
- melakukan konfigurasi routing URL dalam main dengan menambah path('', show_main, name='show_main'), untuk dapat mengimport rute URL dari berkas
- melakukan konfigurasi routing URL Tugas2 dengan menambah path('main/', include('main.urls')), untuk memungkinkan aplikasi dalam proyek django untuk bersifat modular dan terpisah
- cek django yang sudah berhasil dibuat
- mengunggah kembali ke github dengan add, commit, push
- Deploy aplikasi ke adaptable.io

# Buatlah bagan yang berisi request client ke web aplikasi berbasis Django beserta responnya dan jelaskan pada bagan tersebut kaitan antara urls.py, views.py, models.py, dan berkas html.
![image](https://github.com/haffienc/pbpt2/assets/126487038/e1cdcac7-2827-4d28-8648-128cc2d43251)


# Jelaskan mengapa kita menggunakan virtual environment? Apakah kita tetap dapat membuat aplikasi web berbasis Django tanpa menggunakan virtual environment?
Kita menggunakan virtual environment dalam pengembangan aplikasi web, seperti berbasis Django, untuk mengisolasi dan mengelola dependensi proyek secara terpisah. Hal ini memungkinkan kita untuk menghindari konflik antar-versi dan mengatur lingkungan pengembangan yang konsisten. Meskipun mungkin memungkinkan untuk membuat aplikasi web Django tanpa virtual environment, ini dapat menciptakan masalah dalam manajemen dependensi yang dapat memengaruhi stabilitas dan portabilitas proyek, sehingga penggunaan virtual environment sangat disarankan untuk menjaga kebersihan dan keandalan pengembangan perangkat lunak.

# Jelaskan apakah itu MVC, MVT, MVVM dan perbedaan dari ketiganya.
MVC (Model-View-Controller):

Model: Mewakili data dan bisnis logic aplikasi. Ini adalah bagian yang bertanggung jawab untuk mengelola data, logika bisnis, dan interaksi dengan database.
View: Menangani tampilan dan presentasi data kepada pengguna. Ini adalah bagian yang mengatur bagaimana data dari Model ditampilkan kepada pengguna.
Controller: Bertindak sebagai perantara antara Model dan View. Menerima input dari pengguna melalui View, memprosesnya melalui Model, dan mengembalikan respons ke View. Ini adalah bagian yang mengatur alur kendali aplikasi.
Perbedaan: MVC adalah pola desain yang lebih umum digunakan dalam pengembangan perangkat lunak pada umumnya, tidak hanya pada aplikasi web.

MVT (Model-View-Template):

Model: Sama seperti dalam MVC, mewakili data dan logika bisnis.
View: Menangani tampilan data dan logika tampilan, seperti dalam MVC.
Template: Ini adalah komponen tambahan dalam MVT yang digunakan dalam kerangka kerja Django, yang merupakan kerangka kerja web Python yang populer. Template bertanggung jawab untuk menghasilkan tampilan HTML yang diberikan kepada pengguna.
Perbedaan: MVT adalah varian dari MVC yang digunakan secara khusus dalam kerangka kerja web Django.

MVVM (Model-View-ViewModel):

Model: Mirip dengan MVC dan MVT, ini mewakili data dan logika bisnis aplikasi.
View: Bertanggung jawab untuk tampilan dan presentasi data kepada pengguna, seperti dalam MVC dan MVT.
ViewModel: Ini adalah komponen unik dalam MVVM. ViewModel bertanggung jawab untuk menghubungkan Model dan View. Ini mengubah data dari Model menjadi bentuk yang dapat digunakan oleh View dan mengelola interaksi pengguna yang diteruskan kembali ke Model.
Perbedaan: MVVM adalah pola desain yang sering digunakan dalam pengembangan aplikasi berbasis antarmuka pengguna (UI) yang kompleks, seperti aplikasi mobile dan desktop.

# TUGAS 3
# 1. Apa perbedaan antara form POST dan form GET dalam Django?
JAWAB: Django Forms (POST dan GET) merupakan sebuah built-in feature dari Django. Berikut ini merupakan perbedaan dari keduanya:
- Segi Data Types --- Method post dapat menggunakan data types yang berbeda seperti, string, binary, numeric, dan lain-lain. Sedangkan, method get, hanya dapat menggunakan string data type.
- Segi Penggunaan --- Method post digunakan saat ingin melakukan pemrosesan pengiriman data dari form ke server. Sebagai contoh, permintaan untuk mengubah status server atau menyimpan data di dalam database. Sedangkan, method get digunakan saat ingin mendapatkan data dari server. Jadi, proses mendapatkan data ini tidak melakukan perubahan pada status server yang digunakan.
- Segi Cacheable--- Pada umumnya, method post bersifat hardly cacheable. Sedangkan, method get, pada umumnya, bersifat cacheable.
- Segi Security --- Method post lebih aman daripada method get untuk melakukan pengiriman data sensitif (tak nampak pada URL dan tak mudah diakses oleh user). Sedangkan, pada method get, data sensitif dapat nampak di URL, jadi kurang aman untuk digunakan.
- Segi Ukuran Pengiriman Data --- Method post dapat mengirim data dalam jumlah yang lebih besar. Jadi, post cocok untuk meng-upload file dengan size yang besar. Sedangkan, method get, data yang dapat dikirimkan size-nya lebih rendah.

# 2. Apa perbedaan utama antara XML, JSON, dan HTML dalam konteks pengiriman data?
- XML Tidak didesain untuk men-display data, melainkan untuk membawa dan mengirim data yang bersifat human-readable dan machine-readable. XML tidak mendukung array, tetapi mendukung tipe data namespace
- JSON Format data ringkas yang terdiri dari key and value pairs. Syntax dari JSON mirip dengan objek dalam javascript. Secara ukuran, JSON lebih ringan dibanding XML. JSON tidak mendukung tipe data namespace, tetapi mendukung array.
- HTML Markup Language yang didesain khusus untuk menampilkan konten web, bukan untuk pengiriman data antaraplikasi/server.

# 3. Mengapa JSON sering digunakan dalam pertukaran data antara aplikasi web modern?
- JSON merupakan text-based format. Jadi, dapat dibaca oleh mesin dan manusia. JSON juga menggunakan konsep key-value pairs seperti yang telah dijelaskan sebelumnya.
- JSON didukung oleh banyak bahasa pemrograman lainnya. Jadi, JSON berguna untuk pertukaran data antara sistem yang beraneka ragam.
- JSON adalah alat yang sangat serbaguna dari data structure-nya.
- JSON memiliki pemrosesan yang cepat dan mudah dari sisi client. Hal tersebut disebabkan oleh data structure yang dimiliki JSON kedudukannya sejajar dengan objek JavaScript.

# 4. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step
# Membuat input form untuk menambahkan objek Item
- Membuat file forms.py untuk membuat forms sesuai model Item menggunakan Django ModelForm
- Membuat function create_item untuk mengatur implementasi forms yang sudah dibuat tadi.
- Mengonfigurasi url pada file urls.py untuk mengakses function create_item.
- Membuat tampilan forms dalam file create_product.html.
# Tambahkan 5 fungsi views untuk melihat objek yang sudah ditambahkan dalam format HTML, XML, JSON, XML by ID, dan JSON by ID.
- Dalam file views.py, tambahkan import berikut:
  
  from django.http import HttpResponse
  
  from django.core import serializers
  
- Untuk mengembalikan semua objek yang ada, tambahkan fungsi untuk mengambil semua objek dari Item dan mengembalikannya dalam format yang diinginkan menggunakan HttpResponse dan serializers.
  - JSON
    
    def show_json(request):
    
    data = Item.objects.all()
    
    return HttpResponse(serializers.serialize("json", data), content_type="application/json")

  - XML

    def show_xml(request):
    
    data = Item.objects.all()
    
    return HttpResponse(serializers.serialize("xml", data), content_type="application/xml")

  - HTML

    def show_main(request):
    
    products = Item.objects.all()
    
    context = {
    
        'name': 'Haffie Noorcahyo',
    
        'class': 'PBP A',
    
        'apps': 'Barang Gelap',
    
        'products': products
    
    }

    return render(request, "main.html", context)

- XML and JSON by ID:
Buka views.py pada folder main. Kemudian, buat function show_xml_by_id dan show_json_by_id, keduanya memiliki parameter request, serta beri return function HttpResponse yang isinya adalah parameter data hasil query dan parameter content_type="application/xml" (untuk show_xml_by_id) dan content_type="application/json" (untuk show_json_by_id). Lalu, buka urls.py dalam folder main dan import kedua function. Tak lupa, tambahkan path url-nya ke dalam urlpatterns agar dapat diakses.

# Membuat routing URL 
- Pada file urls.py, import semua function yang sudah dibuat
- Kemudian, tambahkan path untuk mengakses masing-masing fungsi.
  
  path('', show_main,name='show_main'),
  
  path('json/', show_json, name="show_json"),

  path('xml/', show_xml, name="show_xml"),

  path('xml/<int:id>/', show_xml_by_id, name='show_xml_by_id'),

  path('json/<int:id>/', show_json_by_id, name='show_json_by_id'),

# Mengakses kelima URL menggunakan Postman
![Screenshot 2023-09-20 095313](https://github.com/haffienc/pbpt2/assets/126487038/9000529d-83c6-483a-af37-3616eefabf96)
![Screenshot 2023-09-20 095458](https://github.com/haffienc/pbpt2/assets/126487038/09c62484-64d6-4295-929f-3ffa2107fdc2)
![Screenshot 2023-09-20 095642](https://github.com/haffienc/pbpt2/assets/126487038/fadc04b1-7812-47b3-9f2f-f7ed8cc58433)
![Screenshot 2023-09-20 095722](https://github.com/haffienc/pbpt2/assets/126487038/2cd8ff96-b987-4590-8d0d-6a387a3107b2)
![Screenshot 2023-09-20 095848](https://github.com/haffienc/pbpt2/assets/126487038/f374157c-bdf8-4467-9554-1014269b3c55)

# TUGAS 4
# Apa itu Django UserCreationForm, dan jelaskan apa kelebihan dan kekurangannya?
Django UserCreationForm adalah sebuah built-in form yang disediakan oleh Django yang memungkinkan untuk membuat form registrasi pengguna pada web kita. Form ini mewarisi UserCreationForm class dalam kerangka otentikasi Django dan mencakup fields untuk username dan password.
- Kelebihan dari UserCreationForm ini di antaranya adalah:
  - Mempermudah pendaftaran user baru
  - Validasi input yang sesuai
  - Terintegrasi dengan object User
  - Relatif mudah untuk digunakan.
- Kekurangannya adalah:
  - Memiliki tampilan standar
  - Fungsi fitur yang terbatas
  - Error message customization

# Apa perbedaan antara autentikasi dan otorisasi dalam konteks Django, dan mengapa keduanya penting?
- Perbedaan antara Authentication dan Otorisasi:
  - Authentication adalah proses verifikasi identitas pengguna, sedangkan Authorization adalah proses penentuan hak akses pengguna setelah identitasnya diverifikasi.
  - Proses otentikasi dilakukan terlebih dahulu sebelum proses Authorization.
  - Authentication memeriksa apakah pengguna memiliki kredensial yang valid, seperti username dan password, sedangkan Authorization memeriksa apakah pengguna memiliki hak akses untuk melakukan tindakan tertentu.
- Pentingnya Authentication dan Otorisasi:
  - Authentication dan Authorization sangat penting dalam pengamanan aplikasi karena dapat mencegah akses yang tidak sah ke data sensitif.
  - Authentication dan Authorization dapat membantu mencegah serangan siber seperti peretasan akun dan pencurian data.
  - Dalam Django, otentikasi dan Authorization dapat diimplementasikan dengan menggunakan kerangka otentikasi bawaan Django atau dengan menggunakan teknologi otentikasi lain seperti OAuth 2.0.

# Apa itu cookies dalam konteks aplikasi web, dan bagaimana Django menggunakan cookies untuk mengelola data sesi pengguna?
Cookies adalah tempat penyimpanan kecil yang disimpan di browser pengguna dan digunakan untuk menyimpan informasi yang dapat diakses oleh server di halaman web tersebut. Cookies biasanya digunakan untuk: Authentication, User tracking, and Maintaining user preferences

Untuk mengelola data di client-side, Django menggunakan cookies untuk melakukan proses authentication & authorization yang bernama cookie-based user sessions. Hal ini dilakukan dengan menyimpan Session ID di dalam cookies untuk dapat melakukan holding state pada HTTP yang stateless.

# Apakah penggunaan cookies aman secara default dalam pengembangan web, atau apakah ada risiko potensial yang harus diwaspadai?
Secara default, penggunaan dari cookies dapat dibilang relatif aman, terutama jika pengimplementasiannya dilakukan dengan baik dan benar. Hal tersebut karena cookies dibuat untuk menyimpan informasi pada users' browser dan hanya dapat diakses oleh situs web yang mengaturnya. Namun, tetap saja terdapat beberapa risiko potensial yang harus diwaspadai, di antaranya:
- Pencurian Data Pribadi --- Cookies yang memiliki informasi sensitif seperti data pribadi sering dijadikan target dari pencurian data. Jadi, cookies haruslah dienkripsi dengan baik dan benar.
- Pelacakan User --- Cookies terkadang dipakai untuk melacak apa saja yang user lakukan di seluruh situs web dan melintasi berbagai domain. Jadi, jelas bahwa ini merupakan suatu pelanggaran privasi.
- Serangan Cookies --- Contohnya seperti Cross-Site Scripting (XSS), sebuah kerentanan keamanan yang mana attacker menempatkan malicious client-end code ke dalam halaman web.

# Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).
Mengimplementasikan fungsi registrasi, login, dan logout untuk memungkinkan user untuk mengakses aplikasi sebelumnya dengan lancar.
- Untuk fungsi registrasi, jalankan virtual environment, lalu buka views.py yang ada di dalam main. Kemudian, buat fungsi register dengan parameter request. Tak lupa, importlah juga redirect, UserCreationForm dan messages. Masukkan juga beberapa baris kode yang akan berfungsi untuk menghasilkan formulir registrasi dan membuat akun user saat data user di-submit. Lalu, buatlah juga file register.html dalam folder main/templates. Pada urls.py dalam main juga harus diimpor fungsi register tersebut. Terakhir, masukkan path URL ke dalam urlpatterns.
- Untuk fungsi login, buka views.py yang ada di dalam main. Kemudian, buat fungsi login_user dengan parameter request. Tak lupa, importlah juga authenticate dan login. Masukkan juga beberapa baris kode yang akan berfungsi untuk mengautentikasi user yang login. Lalu, buatlah juga file login.html dalam folder main/templates. Pada urls.py dalam main juga harus diimpor fungsi login_user tersebut. Terakhir, masukkan path URL ke dalam urlpatterns.
- Untuk fungsi logout, buka views.py yang ada di dalam main. Kemudian, buat fungsi logout_user dengan parameter request. Tak lupa, importlah logout. Masukkan juga beberapa baris kode yang akan berfungsi untuk meng-logout user. Lalu, buka file main.html dalam folder main/templates. Setelah hyperlink tag, tambahkan beberapa baris kode. Pada urls.py dalam main juga harus diimpor fungsi logout_user tersebut. Terakhir, masukkan path URL ke dalam urlpatterns.

Membuat dua akun pengguna dengan masing-masing tiga dummy data
- Masuk ke halaman http://localhost:8000/register, kemudian daftarkan username dan password sesuai dengan syarat yang ditentukan.
- Login menggunakan akun yang sudah didaftarkan.
- Setelah berhasil login, klik button Add New Item dan isi form dengan data yang ingin diinput. Kemudian klik Add Item.
- Ulangi langkah-langkah tersebut untuk akun dummy yang lain.

Menghubungkan model Item dengan User.
-  Untuk menghubungkan model Item dengan User, pertama-tama buka models.py yang ada di dalam main dan import-lah User. Pada model Item juga tambahkan kode: user = models.ForeignKey(User, on_delete=models.CASCADE). Hal tersebut akan menghubungkan satu item dengan satu user.
-  Kemudian, buka views.py dalam main, dan ubah potongan kode dalam function create_item menjadi commit=False agar mencegah Django untuk langsung menyimpan objek yang dibuat dari form ke database.
-  Tak lupa, lakukanlah migrate dengan python manage.py makemigrations dan python manage.py migrate.

Menampilkan detail informasi pengguna yang sedang logged in seperti username dan menerapkan cookies seperti last login pada halaman utama aplikasi.
- Untuk username dapat dilakukan dengan mengubah function show_main menjadi items = Item.objects.filter(user=request.user) dan 'name': request.user.username, dalam context.
- Untuk last login dapat dilakukan dengan buka views.py dalam main dan import HttpResponseRedirect, reverse, dan datetime. Lalu, dalam fungsi login_user, tambahkan fungsi last_login untuk melihat waktu terakhir kali user login ke dalam website. Pada fungsi show_main juga tambahkan kode 'last_login': request.COOKIES['last_login'],. Pada logout_user juga ubah kodenya dan response.delete_cookie('last_login') berguna untuk hapus cookie last_login saat user logout. Terakhir, tambahkan kode yang berfungsi untuk menampilkan data last login tersebut ke dalam main.html.

# TUGAS 5
# Jelaskan manfaat dari setiap element selector dan kapan waktu yang tepat untuk menggunakannya.
Digunakan untuk memilih elemen-elemen HTML berdasarkan tipe atau jenis elemennya. Penggunaan yang tepat untuk setiap jenis element selector dalam CSS tergantung pada kebutuhan desain web kita dan struktur HTML yang akan kita gunakan.

# Jelaskan HTML5 Tag yang kamu ketahui.
Berguna untuk membuat dan memperkaya struktur konten pada web pages dan merupakan versi yang terbaru.

# Jelaskan perbedaan antara margin dan padding.
- Margin:
  - Margin adalah ruang kosong di luar elemen.
  - Margin digunakan untuk mengatur jarak antara elemen dengan elemen-elemen lain di sekitarnya, sehingga mengontrol ruang di luar elemen tersebut.
  - Margin tidak memiliki warna atau latar belakang, dan elemen-elemen di luar margin tidak bisa mengisi atau mengubahnya.
  - Margin tidak mempengaruhi ukuran sebenarnya dari elemen tersebut, melainkan hanya mengatur seberapa jauh elemen tersebut berjarak dari elemen-elemen lain.

- Padding:
  - Padding adalah ruang kosong di dalam elemen.
  - Padding digunakan untuk mengatur jarak antara konten elemen dan batas (border) elemen tersebut.
  - Padding memiliki warna dan latar belakang yang sama dengan elemen, sehingga elemen-elemen di dalam padding bisa menimpa atau mengubah warna latar belakang tersebut.
  - Padding mempengaruhi ukuran sebenarnya dari elemen tersebut, karena jika Anda menambahkan padding, maka ukuran elemen akan bertambah sesuai dengan jumlah padding yang ditetapkan.
 
# Jelaskan perbedaan antara framework CSS Tailwind dan Bootstrap. Kapan sebaiknya kita menggunakan Bootstrap daripada Tailwind, dan sebaliknya?
Tailwind CSS dan Bootstrap adalah dua framework CSS yang digunakan untuk membangun tampilan dan tata letak web dengan cepat. Mereka memiliki beberapa perbedaan utama dalam pendekatan desain dan penggunaan.
- Tailwind:
  - Fokusnya untuk menciptakan elemen UI yang bersifat fungsional, rapi, dan fleksibel.
  - Dalam aspek kustomisasi, lebih fleksibel karena mudah untuk penyesuaian tampilannya.
  - Dalam aspek file size, lebih ringan karena hanya menggunakan class yang dibutuhkan.
  - Dalam aspek kompleksitas proyek, cocok untuk proyek kecil yang kebutuhan kustomisasinya besar.
  - Waktu penggunaannya saat mengembangkan tampilan yang memiliki fleksibilitas tinggi dan adaptabilitas tinggi, proyek kecil-menengah, dan pembangunan tampilan dengan pendekatan berbasis kelas dalam HTML.

- Bootstrap:
  - Lebih tradisional (komponen dan gayanya sebelumnya sudah ditentukan, jadi tinggal digabungkan ke dalam proyek). Berfokus pada pengembangan segala komponen untuk penggunaan website.
  - Dalam aspek kustomisasi, lebih terstruktur dan lebih sulit karena harus mengganti atau menambahkan style CSS tambahan.
  - Dalam aspek file size, lebih besar karena menggunakan seluruh komponen dan style.
  - Dalam aspek kompleksitas proyek, cocok untuk proyek besar atau butuh pengembangan yang cepat.
  - Waktu penggunaannya saat mengembangkan proyek yang cepat dan tidak membutuhkan kustomisasi lebih. Digunakan juga untuk proyek besar dengan konsistensi tampilan dan fungsionalitas.

# Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).
- menambahkan tag meta name="viewport" ke dalam file base.html di dalam subdirektori templates.
- menambahkan Bootstrap CSS dan juga JS.
- menambahkan fitur edit pada aplikasi
  - Pada subdirektori main kita menambahkan fungsi baru bernama edit_item dalam berkas views.py.
    ![image](https://github.com/haffienc/pbpt2/assets/126487038/bfaadcd1-43e7-407c-929f-c153ad4ad770)
  - membuat berkas HTML baru yang bernama edit_item.html pada subdirektori main/templates
    ![image](https://github.com/haffienc/pbpt2/assets/126487038/af627137-e2c0-4f59-ba16-e5b42c2b3677)
  - mengimport fungsi yang telah dibuat dan menambahkan path url untuk dapat mengakses fungsi yang telah kita buat
    ![image](https://github.com/haffienc/pbpt2/assets/126487038/3cbeaaf7-9cbe-43b9-be90-fe0b7423f48d)
    ![image](https://github.com/haffienc/pbpt2/assets/126487038/03f9f78d-d11e-4a9e-8376-0b40ca6c786b)
  - menambahkan kode pada main.html agar tombol edit dapat muncul pada halaman main
    ![image](https://github.com/haffienc/pbpt2/assets/126487038/c1e53702-adff-490b-9ad1-6d485a3abe9d)
- menambahkan fitur delete pada aplikasi
  - membuat fungsi delete_item pada berkas views.py yang terdapat pada subdirektori main.
    ![image](https://github.com/haffienc/pbpt2/assets/126487038/27bf27b0-eae4-4921-bc6a-a369d9fe7a3d)
  - mengimpor fungsi yang telah kita buat lalu menambahkan path url ke dalam urlpatterns agar fungsi dapat diakses.
    ![image](https://github.com/haffienc/pbpt2/assets/126487038/05038424-255e-4128-8155-32a2cae2aa76)
    ![image](https://github.com/haffienc/pbpt2/assets/126487038/95bd9875-a591-49b7-9275-cad01a692d0a)
  - menambahkan tombol delete pada main.html
    ![image](https://github.com/haffienc/pbpt2/assets/126487038/10005d5e-2c2c-4f8e-af0e-ad594c06b891)
- kustomisasi desain
  - pada background semua halaman saya menjadikan warna hitam dan untuk semua teks pada halaman basicnya dengan warna warning
  - pada halaman login mengedit tombol login dengan warna dark, dan link register menjadi warna light
  - pada halaman main saya menjadikan input input menjadi sebuah card card dan merubah warna card tersebut, menuruh judul ditengah tengah ditambah dengan background tulisan kuning, button edit-delete menjadi warna kuning.
  - pada halaman register saya hanya merubah warnanya saja

# TUGAS 6
# Jelaskan perbedaan antara asynchronous programming dengan synchronous programming.
Synchronous Programming
   - Membaca _file_ pemrograman.
   - Tugas atau operasi akan dieksekusinya berurutan (satu per satu).
   - Saat ada tugas yang sedang dalam proses, program akan tetap menunggu sampai tugas tersebut selesai. Barulah program akan melanjutkan ke tugas berikutnya.
   - Data baru dapat diambil / di-_edit_ setelah tugas sebelumnya sudah selesai.

Asynchronous Programming
   - Mengunduh suatu _file_ dari internet.
   - Tugas atau operasi akan dieksekusi secara satu sama lain.
   - Program tidak harus menunggu tugas yang lainnya untuk lanjut mengerjakan tugas selanjutnya. 
   - Hal tersebut akan memungkinkan aplikasi agar tetap responsif karena tidak akan mengalami penundaan.
# Jelaskan maksud dari paradigma tersebut dan sebutkan salah satu contoh penerapannya pada tugas ini.
Event-driven programming adalah paradigma pemrograman di mana alur program ditentukan oleh kejadian atau event tertentu, seperti tindakan pengguna dari mouse, keyboard, atau layar sentuh. Event-driven programming adalah paradigma yang dominan digunakan dalam antarmuka pengguna grafis dan aplikasi lain yang berpusat pada melakukan tindakan tertentu sebagai respons terhadap masukan pengguna. Contoh dari event-driven programming adalah ketika pengguna mengklik tombol pada antarmuka pengguna, program akan merespons dengan menjalankan fungsi atau tindakan tertentu, seperti membuka jendela baru atau menyimpan data ke database.
# Jelaskan penerapan asynchronous programming pada AJAX.
AJAX (Asynchronous JavaScript and XML) adalah teknik pengembangan aplikasi web yang memungkinkan aplikasi web untuk bekerja secara asynchronous (tidak langsung) dan membuat aplikasi web menjadi lebih responsif terhadap interaksi pengguna. Penerapan asynchronous programming pada AJAX memungkinkan aplikasi web untuk mengirim dan menerima data dari server secara asynchronous tanpa harus mereload keseluruhan halaman.
 step by step penggunaan asynchronous programming pada AJAX:
- Buat objek XMLHttpRequest pada JavaScript untuk mengirim permintaan ke server.
- Buat fungsi callback untuk menangani respon dari server.
- Buat permintaan AJAX dengan menggunakan objek XMLHttpRequest dan fungsi callback.
- Setelah permintaan dikirim, program akan tetap berjalan dan menunggu respon dari server.
- Ketika respon dari server diterima, fungsi callback akan dijalankan untuk menangani respon tersebut.
- Hasil dari respon dapat ditampilkan pada halaman web tanpa harus mereload keseluruhan halaman.
# Pada PBP kali ini, penerapan AJAX dilakukan dengan menggunakan Fetch API daripada library jQuery. Bandingkanlah kedua teknologi tersebut dan tuliskan pendapat kamu teknologi manakah yang lebih baik untuk digunakan.
**Fetch API** merupakan aktivitas pengiriman _request_ ke _service endpoint backend_ pada aplikasi web. Pada umumnya, hasil respons dari API adalah data yang berformat JSON dan XML. Beberapa karakteristik yang dimiliki oleh fetch API, di antaranya:

a. **JavaScript Asli ---** Fetch API sudah terintegrasi sebagai bagian dari JavaScript yang asli. Jadi, tidak perlu untuk melakukan pengunduhan atau pengimporan _library_ tambahan.

b. **_Promises_ ---** Fetch API menggunakan Promises (menyediakan cara yang lebih modern dan bersih untuk pengelolaan operasi _asynchronous_). 

c. **Ringan ---** Fetch API bersifat lebih ringan daripada jQuery.

d. **Fleksibilitas ---** Fetch API memiliki lebih banyak fleksibilitas dalam hal penanganan _request_ dan respons. Jadi, pengembang akan dapat bekerja dengan banyak jenis data seperti JSON, teks, XML, dan lain-lain.

Sedangkan, **jQuery** merupakan sebuah _framework_ atau _library_ JavaScript. Penggunaannya akan dapat mempercepat dan mempermudah proses pengembangan aplikasi web. Beberapa karakterirstik yang dimiliki oleh jQuery, di antaranya:

a. **Kompatibilitas Cross-Browser ---** Pada awal mulanya, jQuery dikembangkan untuk mengatasi inkonsistensi dalam JavaScript di berbagai browser. Jadi, jQuery lebih konsisten untuk melakukan _request_ AJAX, terutama di browser lama.

b. **Abstraksi:** jQuery mengabstraksi banyak kompleksitas _object_ XMLHttpRequest, memberikan API yang lebih sederhana, dan mudah digunakan untuk operasi AJAX.

c. **Berat ---** jQuery bersifat lebih berat daripada fetch API.

d. **Utilitas Tambahan:** jQuery merupakan sebuah _library_ komprehensif dengan berbagai fungsi utilitas dan _plugin_ untuk menangani tidak hanya permintaan AJAX tetapi juga manipulasi DOM, animasi, dan tugas-tugas pengembangan web umum lainnya.

Pendapat saya adalah Fetch API lebih baik untuk digunakan karena lebih modern dan lebih sederhana dibandingkan dengan jQuery. Selain itu, Fetch API juga lebih fleksibel dan dapat digunakan dengan mudah dalam berbagai jenis proyek web. Meskipun jQuery lebih mudah digunakan dan lebih populer, Fetch API lebih disarankan karena lebih modern dan lebih sederhana.
# Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).
a. Mengubah tugas 5 yang telah dibuat sebelumnya menjadi menggunakan AJAX. Pertama-tama, buat _function_ baru dalam `views.py` (tampilkan data item pada HTML dengan fetch & gunakan AJAX untuk tambahkan _new item_ ke dalam _database_). Tak lupa, tambahkan juga _path_-nya di dalam `urls.py`. Dalam `main.html`, tambahkan id dan blok kode _script_. Terakhir, di dalam `main.html`, buatlah modal sebagai _form_.

b. Melakukan perintah collectstatic dapat dilakukan setelah mengaktifkan environmen. Jalankan _command_ `python manage.py collectstatic`.

c. Menjawab 5 pertanyaan berikut pada README.md pada _root folder_

d. Melakukan `add-commit-push` ke GitHub. Lakukan dengan `git add .`, `git commit -m "TUGAS 6"`, dan `git push origin dev2`.
