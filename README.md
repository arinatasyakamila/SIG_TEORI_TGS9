# SIG_TEORI_TGS9
 working with WMS data

# Langkah Kerja :

1. Buka QGIS dan klik Open Data Source Manager.

2. Di kotak dialog Pengelola Sumber Data beralih ke WMS/WMTS, klik New.

3. Di kotak dialog Buat Koneksi WMS/WMTS Baru di bawah Detail Koneksi, masukkan Nama sebagai SEDAC, dan tempel URL yang disalin di kotak teks URL. Klik Oke. Jika Anda mendapatkan kesalahan dengan URL yang disalin, coba dengan URL alternatif https://sedac.ciesin.columbia.edu/geoserver/ows.

4. Sekarang di kotak dialog Data Source Manager, klik Connect. Semua lapisan yang tersedia akan dimuat. Anda akan melihat ID berbeda yang tercantum di sebelah lapisan. ID 0 berarti Anda mendapatkan peta dari semua lapisan. Jika Anda tidak menginginkan semua lapisan, Anda dapat memperluas daftar dengan mengeklik ikon ▸ dan memilih lapisan yang diinginkan.

5. Untuk tutorial ini, kami tertarik pada lapisan tertentu. Cari Probabilities of Urban Expansion to 2030. Pilih versi default lapisan ekspansi perkotaan 2030.

6. Di bagian Pengkodean Gambar, Anda harus memilih format gambar. Format gambar itu penting, dan itu tergantung pada kasus penggunaan. Berdasarkan perspektif pengguna berikut adalah beberapa petunjuk,

7. Kualitas: Kompresi file untuk PNG adalah lossless, untuk JPEG ini adalah kompresi lossy dan TIFF dapat berupa keduanya. Itu berarti kualitas PNG akan lebih baik dibandingkan dengan JPEG. Jika tujuan utama Anda adalah mencetak peta, gunakan PNG.

8. Kecepatan: Karena gambar PNG tidak terkompresi dan dengan demikian ukurannya lebih besar, mereka akan membutuhkan waktu lebih lama untuk dimuat. Jika Anda menggunakan lapisan dalam proyek Anda sebagai lapisan referensi dan perlu banyak memperbesar/menggeser, gunakan JPEG.

9. Dukungan Klien: QGIS mendukung sebagian besar format, tetapi jika Anda mengembangkan aplikasi web, browser biasanya tidak mendukung TIFF, jadi Anda harus memilih format lain.

10. Jenis data: Jika lapisan Anda sebagian besar adalah vektor, PNG akan memberikan hasil yang lebih baik. Untuk lapisan citra, JPEG biasanya merupakan pilihan yang lebih baik.

11. Sekarang lapisan Probabilities of Urban Expansion to 2030 akan dimuat di kanvas. Gunakan alat Zoom/Pan untuk menjelajahi lapisan. Cara kerja layanan WMS adalah setiap kali Anda memperbesar/menggeser, ia mengirimkan koordinat area pandang Anda ke server dan server membuat gambar untuk area pandang tersebut dan mengembalikannya ke klien. Jadi, akan ada beberapa penundaan sebelum Anda melihat gambar untuk area tersebut setelah Anda memperbesar. Oleh karena itu, koneksi internet selalu diperlukan untuk mengakses lapisan ini.

12. Sekarang, perbesar ke tempat yang diketahui dan klik ikon Identify Features di bilah alat.

13. Klik pada piksel apa saja di kanvas, itu akan memunculkan kotak dialog dengan nilai sel. Ini adalah nilai piksel dalam lapisan - yang mewakili kemungkinan bahwa piksel tersebut akan mengalami urbanisasi pada tahun 2030. Karena lapisan tersebut tidak disimpan secara lokal, nilai ini diambil dari penyedia layanan. Anda dapat melihat hasilnya lebih baik dengan memilih Format as HTML dan View as Tree.

14. Untuk melihat, informasi tambahan tentang layer klik kanan pada layer dan pilih Properties….

15. Di kotak dialog Layer Properties, alihkan ke tab Informasi di sini semua informasi seperti penyedia data, proyeksi, jangkauan dapat ditemukan. Klik OK untuk menutup kotak dialog setelah menjelajah.

16. Di Browser QGIS, cari Ubin XYZ dan klik dan seret OpenStreetMap ke kanvas.

17. Klik pada ikon panel Open the Layer Styling dan beralih ke Transparency.

18. Atur opasitas Global menjadi 50%

19. Sekarang di kanvas, lapisan Urban dapat dieksplorasi dengan referensi geografis.

20. Untuk mendapatkan lebih banyak akses ke transparansi layer, klik kanan pada layer dan pilih Properties….

21. Di kotak dialog Properties Lapisan, alihkan ke tab Legend, di bawah Widget yang tersedia pilih penggeser Opasitas dan klik Tambahkan ikon widget yang dipilih. Klik OK.

22. Sekarang widget penggeser akan tersedia untuk mengontrol opacity layer.
