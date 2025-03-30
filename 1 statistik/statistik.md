Gareth James-Daniel Witten-Trevor Hastie-Robert Tibshirani-Jonathan Taylor

# Pengantar Pembelajaran Statistik dengan Aplikasi di Python

## Kata Pengantar

pembelajaran statistik mengacu pada seperangkat alat untuk memahami kumpulan data yang kompleks. dalam beberapa tahun terakhir, kita telah melihat peningkatan yang mengejutkan dalam skala dan cakupan pengumpulan data di hampir semua bidang ilmu pengetahuan dan industri. Hasilnya, pembelajaran statistik telah menjadi perangkat penting bagi siapa saja yang ingin memahami data - dan karena semakin banyak pekerjaan saat ini yang melibatkan data, ini berarti pembelajaran statistik dengan cepat menjadi perangkat penting bagi semua orang.

Salah satu buku pertama tentang pembelajaran statistik - The Elements of Statistical Learning (ESL, oleh Hastie, Tibshirani, dan Friedman) - yang diterbitkan pada tahun 2001, dengan edisi kedua pada tahun 2009. ESL telah menjadi teks yang populer tidak hanya di bidang statistik tetapi juga di bidang-bidang terkait. Salah satu alasan popularitas ESL adalah gayanya yang relatif mudah dipahami. Tetapi ESL paling cocok untuk individu dengan pelatihan lanjutan dalam ilmu matematika.

Pengantar Pembelajaran Statistik (Introduction to statistical learning), Dengan Aplikasi dalam R (ISLR) - pertama kali diterbitkan pada tahun 2013, dengan edisi kedua pada tahun 2021 - muncul dari kebutuhan yang jelas akan perlakuan yang lebih luas dan tidak terlalu teknis terhadap topik-topik utama dalam pembelajaran statistik. Selain tinjauan tentang regresi linier, ISLR mencakup banyak pendekatan pembelajaran statistik dan mesin yang paling penting saat ini, termasuk resampling, metode jarang untuk klasifikasi dan regresi, model aditif umum, metode berbasis pohon, mesin vektor pendukung, pembelajaran mendalam, analisis kelangsungan hidup, pengelompokan, dan pengujian berganda.

Sejak diterbitkan pada tahun 2013, ISLR telah menjadi andalan di kelas sarjana dan pascasarjana di seluruh dunia, serta penting bagi para ilmuwan data. Salah satu kunci keberhasilannya adalah bahwa, dimulai dari Bab 2, setiap bab berisi laboratorium R yang mengilustrasikan bagaimana menerapkan metode pembelajaran statistik yang ada di bab tersebut, memberikan pengalaman langsung yang berharga bagi para pembaca.

Namun, dalam beberapa tahun terakhir Python telah menjadi bahasa yang semakin populer untuk ilmu data, dan ada peningkatan permintaan untuk alternatif berbasis Python untuk ISLR. Oleh karena itu, buku ini, Pengantar Pembelajaran Statistik, Dengan Aplikasi dalam Python (ISLP), mencakup materi yang sama dengan ISLR tetapi dengan praktikum yang diimplementasikan dalam Python - sebuah prestasi yang dicapai dengan tambahan penulis baru, Jonathan Taylor. Beberapa lab menggunakan paket Python ISLP, yang telah kami tulis untuk memfasilitasi pelaksanaan metode pembelajaran statistik yang tercakup dalam setiap bab dalam Python. Lab-lab ini akan berguna bagi para pemula Python, dan juga bagi para pengguna yang sudah berpengalaman.

Tujuan di balik ISLP (dan ISLR) adalah untuk lebih berkonsentrasi pada aplikasi metode dan lebih sedikit pada detail matematika, jadi itu adalah sesuai untuk mahasiswa tingkat lanjut atau mahasiswa magister dalam bidang statistik atau bidang kuantitatif terkait, atau untuk individu dalam disiplin ilmu lain yang ingin menggunakan alat pembelajaran statistik untuk menganalisis data mereka. Buku ini dapat digunakan sebagai buku teks untuk mata kuliah yang berlangsung selama dua semester.

Kami berterima kasih kepada para pembaca yang telah memberikan komentar yang berharga pada ISLR edisi pertama: Pallavi Basu, Alexandra Chouldechova, Patrick Danaher, Will Fithian, Luella Fu, Sam Gross, Max Grazier G'Sell, Courtney Paulson, Xinghao Qiao, Elisa Sheng, Noah Simon, Kean Ming Tan, Xin Lu Tan. Kami berterima kasih kepada para pembaca atas masukan yang sangat membantu dalam edisi kedua ISLR: Alan Agresti, Iain Carmichael, Yiqun Chen, Erin Craig, Daisy Ding, Lucy Gao, Ismael Lemhadri, Bryan Martin, Anna Neufeld, Geof Tims, Carsten Voelkmann, Steve Yadlowsky, dan James Zou. Kami sangat berterima kasih kepada Balasubramanian “Naras” Narasimhan atas bantuannya di ISLR dan ISLP.

Merupakan suatu kehormatan dan keistimewaan bagi kami untuk melihat dampak yang cukup besar yang dimiliki ISLR terhadap cara pembelajaran statistik dipraktikkan, baik di dalam maupun di luar lingkungan akademis baik di dalam maupun di luar lingkungan akademis. Kami berharap edisi Python yang baru ini baru ini akan terus memberikan para ahli statistik terapan dan data dan ilmuwan data alat yang mereka butuhkan untuk sukses di dunia yang digerakkan oleh data.

`It’s tough to make predictions, especially about the future.`

<p align='right'>-Yogi Berra</p>

## 1. Pendahuluan

Tinjauan Umum tentang Pembelajaran Statistik

Pembelajaran statistik mengacu pada seperangkat alat yang sangat luas untuk memahami data. Alat-alat ini dapat diklasifikasikan sebagai alat yang diawasi(supervised) atau tidak diawasi (unsupervised). Secara garis besar, supervised statistical learning melibatkan pembuatan model statistik untuk memprediksi, atau memperkirakan, sebuah output berdasarkan satu atau lebih input. Masalah-masalah ini terjadi di berbagai bidang seperti bisnis, kedokteran, astrofisika, dan kebijakan publik. Dengan unsupervised statistical learning, ada input tetapi tidak ada output yang mengawasi; namun kita dapat mempelajari hubungan dan struktur dari data tersebut. Untuk memberikan gambaran tentang beberapa aplikasi pembelajaran statistik, kami secara singkat membahas tiga set data dunia nyata yang dibahas dalam buku ini.