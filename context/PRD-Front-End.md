# **PRD \- Website UI Referensi & Streaming Film**

**Nama:** Ilham Dwi Putranto  
**Kelas:** FWD 13  
**Tugas:** Day 5 \- Mini Project

| Keterangan | Informasi |
| :---- | :---- |
| **Versi** | 1.0 |
| **Status** | Draft untuk tugas |
| **Konteks** | Pembelajaran Front-End Development |
| **Teknologi** | HTML, CSS, Tailwind CSS, FontAwesome |
| **Scope** | Halaman Beranda (Home) dan Halaman Streaming/Detail (Watch) |

## **1\. Product Overview**

Platform web streaming dan katalog film interaktif yang dirancang untuk memberikan rekomendasi film/serial terkini, kemudahan navigasi pencarian, serta antarmuka pemutar video dan detail episode bagi pengguna yang ingin menikmati konten multimedia secara online.  
Pada versi ini, sistem berfokus pada dua halaman utama, yaitu **Halaman Beranda (home.html)** yang menampilkan hero banner film unggulan, daftar tren, serta rilisan terbaru, dan **Halaman Watch (watch.html)** yang menyajikan pemutar video, informasi detail film/series, pemilih episode, daftar ulasan, serta rekomendasi konten terkait.

### **Contoh Entitas Konten Utama:**

* **Film Utama (Hero Banner):** Avatar: The Way of Water (Genre: Action, Adventure, Sci-Fi)  
* **Series Unggulan (Watch Detail):** Silo (Genre: Drama, Sci-Fi | Season 1\)  
* **Navigasi & Pencarian:** Filter berdasarkan Genre, Country, Movies, Series, dan Animation  
* **Fitur Interaktif:** Pemilih Season & Episode, Form Komentar & Rating, Bookmark (Watch Later / Add to Favourite)

## **2\. Problem \+ Target User**

### **Problem**

Pengguna layanan hiburan digital sering kali kesulitan menemukan platform rekomendasi film yang memiliki tampilan bersih, navigasi responsif, serta informasi detail episode yang terstruktur dengan rapi.  
**Masalah yang ingin diselesaikan:**

> 1. Tata letak katalog film dan serial yang tidak responsif pada berbagai ukuran layar.  
> 2. Pengelompokan episode dan variasi season pada serial TV yang rumit dan tidak intuitif.  
> 3. Antarmuka pemutar video dan informasi detail film yang terpisah atau sulit diakses dalam satu halaman.  
> 4. Kurangnya kolom interaksi pengguna seperti area ulasan/komentar interaktif.

### **Target User**

Pencinta film dan serial TV yang mengakses platform melalui perangkat desktop, tablet, maupun smartphone untuk mencari referensi film, melihat informasi lengkap, dan menonton episode terbaru.  
**Kebutuhan Utama:** Mengakses katalog film terbaru, memutar video dengan kontrol lengkap, memilih episode serial, serta membaca dan menulis komentar.

## **3\. Goals \+ Non-Goals**

### **Goals**

> 1. Mengimplementasikan antarmuka responsif menggunakan HTML, CSS, dan Tailwind CSS.  
> 2. Menyediakan **Halaman Beranda (home.html)** dengan hero banner, kategori trending, new release, dan rekomendasi.  
> 3. Menyediakan **Halaman Detail (watch.html)** yang dilengkapi video player, metadata film, pemilih episode, dan kolom komentar.  
> 4. Menyiapkan sistem komponen UI yang menarik dengan tema gelap (*dark mode*) modern.

### **Non-Goals**

Versi ini tidak mencakup:

* Integrasi *backend streaming server* (Video Player menggunakan *mockup UI/video player static*).  
* Sistem Otentikasi/Login real (hanya elemen UI tombol Login/Signup).  
* Penyimpanan data komentar/favorit ke Database nyata.  
* Fitur *Payment Gateway* atau berlangganan *VIP premium*.

## **4\. User Flow**

### **Flow Halaman Beranda (home.html):**

> 1. Pengguna membuka home.html.  
> 2. Pengguna melihat tayangan film unggulan di *Hero Section* (misal: *Avatar: The Way of Water*).  
> 3. Pengguna dapat mengeklik tombol **"Watch Now"** pada banner atau memilih salah satu kartu film dari daftar *Trending* / *New Release*.  
> 4. Pengguna diarahkan ke halaman detail streaming (watch.html).

### **Flow Halaman Watch (watch.html):**

> 1. Pengguna berada di watch.html untuk menonton serial/film (misal: *Silo*).  
> 2. Pengguna memutar video melalui antarmuka pemutar video di bagian atas.  
> 3. Pengguna membaca informasi metadata film (Genre, Release Date, Cast, Synopsis).  
> 4. Pengguna memilih nomor episode yang ingin ditonton pada bagian *Season & Episodes Selector*.  
> 5. Pengguna membaca atau menulis tanggapan pada section *Comments* di bagian bawah.

## **5\. Features \+ Requirements**

| ID | Fitur | Requirement |
| :---- | :---- | :---- |
| **FR-01** | Navigation Bar | Menampilkan menu utama (Home, Genre, Country, Movies, Series, Animation), input pencarian, dan tombol Login/Signup. |
| **FR-02** | Hero Section Banner | Menampilkan gambar latar latar besar, judul film utama, tag genre, tahun, durasi, rating, serta tombol "Watch Now" & "Watch Later". |
| **FR-03** | Section Recently Updated & Trending | Menampilkan daftar *horizontal slider/grid* film & serial yang baru diperbarui beserta indikator episode dan genre. |
| **FR-04** | Section New Release & Recommended | Menampilkan kartu-kartu film lengkap dengan badge kualitas video (HD/CAM), durasi, dan judul. |
| **FR-05** | Video Player Container | Menampilkan komponen pemutar video responsif lengkap dengan kontrol play, progress bar, durasi, volume, dan pengaturan layar. |
| **FR-06** | Detail Metadata & Poster Film | Menampilkan poster resmi, judul, sinopsis, informasi negara, genre, tanggal rilis, studio produksi, dan jajaran pemeran (Cast). |
| **FR-07** | Season & Episode Selector | Menyediakan tombol dropdown Season dan daftar tombol Episode yang aktif/interaktif saat dipilih. |
| **FR-08** | Section "You May Also Like" | Menampilkan grid rekomendasi serial/film serupa. |
| **FR-09** | Form Komentar & Diskusi | Menyediakan bidang *input text* untuk menulis komentar serta daftar komentar pengguna lengkap dengan fitur *Like/Dislike/Reply*. |
| **FR-10** | Layout Responsif & Theme | Menggunakan tata letak *grid & flexbox* Tailwind CSS dengan tema warna gelap (*dark theme*) yang konsisten. |

## **6\. User Stories**

| ID | User Story |
| :---- | :---- |
| **US-01** | Sebagai pengunjung, saya ingin melihat halaman utama yang bersih dengan rekomendasi film populer agar dapat memilih tontonan dengan cepat. |
| **US-02** | Sebagai pengguna, saya ingin mencari film berdasarkan kata kunci di pencarian agar menemukan judul spesifik. |
| **US-03** | Sebagai penonton, saya ingin melihat pemutar video yang jelas di halaman tontonan agar dapat menikmati konten multimedia. |
| **US-04** | Sebagai penonton serial, saya ingin memilih daftar episode yang tersedia agar dapat melanjutkan tontonan ke episode berikutnya. |
| **US-05** | Sebagai penonton, saya ingin membaca sinopsis dan daftar pemeran film agar mengetahui latar belakang cerita. |
| **US-06** | Sebagai pengguna, saya ingin memberikan balasan atau komentar pada halaman film agar dapat berdiskusi dengan penonton lain. |

## **7\. Acceptance Criteria**

| ID | Skenario | Hasil yang Diharapkan |
| :---- | :---- | :---- |
| **AC-01** | Pengguna membuka home.html pertama kali | Hero banner *Avatar: The Way of Water*, section *Trending*, *New Release*, dan *Recommended* tampil dengan responsif. |
| **AC-02** | Pengguna mengeklik tombol "Watch Now" pada hero banner di home.html | Sistem secara otomatis mengarahkan navigasi pengguna ke file watch.html. |
| **AC-03** | Pengguna menekan tombol episode pada watch.html | Indikator episode yang dipilih berubah warna menjadi aktif (ter-highlight merah). |
| **AC-04** | Pengguna mengetik komentar di kolom input dan menekan kirim | Komentar terisi pada area input dengan tampilan UI yang sesuai desain. |
| **AC-05** | Halaman dibuka pada resolusi smartphone/layar kecil | Layout menyusut secara adaptif dari multiple column menjadi 1-2 kolom tanpa rusak (*overflow/horizontal scroll bar* yang tak diinginkan). |

## **8\. Constraints \+ Success Criteria**

### **Constraints**

* Menggunakan Tailwind CSS via CDN untuk kemudahan pengolahan tata letak responsif.  
* Tidak menggunakan *framework JavaScript heavy* (seperti React/Vue), murni *HTML/CSS Layouting*.  
* Penyajian data film disimulasikan melalui *static markup*.

### **Success Criteria**

Halaman dianggap berhasil apabila:

> 1. Seluruh elemen pada **Halaman Home (home.html)** dan **Halaman Watch (watch.html)** sesuai dengan acuan referensi desain gambar.  
> 2. Sistem *grid layout* dan *flexbox* Tailwind CSS responsif di layar mobile, tablet, maupun desktop.  
> 3. Navigasi antar halaman home.html dan watch.html terhubung dengan baik.