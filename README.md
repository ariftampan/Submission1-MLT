# Laporan Proyek Machine Learning - Yance Arifiyanto

## Domain Proyek

Harga rumah adalah faktor krusial dalam pasar perumahan, dan penentuan harga yang akurat memiliki dampak signifikan pada keputusan pembeli dan penjual. Menganalisis dan memprediksi harga rumah dengan tepat menjadi semakin penting karena kompleksitas pasar yang terus berkembang. Tantangan utama yang dihadapi dalam masalah harga rumah termasuk fluktuasi harga yang cepat, variasi nilai properti, dan dampak faktor eksternal seperti kondisi ekonomi dan sosial.
Saat ini, ketidakpastian harga properti dapat menciptakan kesulitan bagi calon pembeli dan penjual. Dalam keadaan seperti ini, penggunaan model machine learning untuk menganalisis dan memprediksi harga rumah dapat memberikan solusi konkret, yaitu diantaranya:

Keunggulan Prediksi Tepat
Model <i>machine learning</i>, seperti KNN, RF, dan Boosting Algorithms, memiliki kemampuan untuk memahami pola dan tren yang rumit dalam data harga rumah. Dengan demikian, penggunaan model ini dapat meningkatkan ketepatan dan akurasi dalam memprediksi harga rumah, memberikan keunggulan dalam pengambilan keputusan.

Optimasi Harga
Melalui analisis yang mendalam, model machine learning dapat membantu dalam mengoptimalkan penetapan harga rumah berdasarkan berbagai fitur dan faktor yang mempengaruhi harga. Ini dapat memungkinkan penjual untuk menentukan harga yang kompetitif dan pembeli untuk mendapatkan nilai terbaik.

Adaptasi Terhadap Perubahan Pasar
Dengan memanfaatkan teknik-teknik machine learning, model dapat beradaptasi dengan perubahan pasar secara real-time, memperhitungkan variabilitas yang mungkin terjadi. Hal ini memungkinkan pemangku kepentingan untuk mengambil keputusan yang lebih baik dan lebih cepat.

## Business Understanding

Permasalahan utama yang ingin diselesaikan adalah ketidakpastian dalam penentuan harga rumah, yang saat ini dapat menciptakan kesulitan bagi calon pembeli dan penjual. Tantangan tersebut mencakup fluktuasi harga yang cepat, variasi nilai properti, dan dampak faktor eksternal seperti kondisi ekonomi dan sosial. Harga rumah yang tidak akurat dapat menyebabkan ketidaksetaraan dalam transaksi, membuat calon pembeli dan penjual mengalami kesulitan dalam pengambilan keputusan yang tepat.

Beberapa pertanyaan bisnis yang perlu dijawab antara lain

- Faktor faktor yang paling mempengaruhi harga properti seperti jumlah kamar tidur, luas tanah, kondisi properti dan sebagainya.
- Bagaimana model dapat meningkatkan kualitas estimasi harga bagi pihak yang terlibat dalam transaksi properti.

Dengan analisis menggunakan Machine Learning maka diharapkan pertanyaan pertanyaan diatas dapat terjawab, sehingga tujuan dapat tercapai yang diantaranya:

- Mengetahui variabel yang paling berperan dalam penentuan harga
- Dapat menetapkan Harga pada waktu yang dikehendaki. Dengan machine learning, dapat diprediksi harga pada waktu yang dikehendaki, misal prediksi harga bulan depan, di mana model machine learning dapat memberikan prediksi harga dengan tingkat akurasi tertentu.

Solusi untuk permasalahan ini melibatkan pengembangan model machine learning, termasuk tetapi tidak terbatas pada algoritma K-Nearest Neighbors (KNN), Random Forest (RF), dan Boosting Algorithms. Model ini akan memanfaatkan dataset historis harga rumah dan fitur-fitur yang relevan untuk menghasilkan prediksi harga yang lebih tepat pada "waktu tertentu." Dengan mengoptimalkan keakuratan prediksi, model ini diharapkan dapat memberikan panduan yang lebih baik bagi para pemangku kepentingan dalam membuat keputusan pembelian atau penjualan properti.

Kriteria Kesuksesan:
Keberhasilan proyek ini akan diukur berdasarkan:

- Mengetahui variabel yang paling berpengaruh terhadap harga
- Akurasi prediksi harga rumah pada rentang waktu yang telah ditentukan.
  Dengan demikian, proyek dapat dianggap berhasil jika mampu mencapai kriteria diatas.

## Data Understanding

### Informasi Data:

- Jumlah Data: 4.601 entri properti.
- Kondisi Data: Dataset terdiri dari properti-properti yang bervariasi, mencakup berbagai fitur seperti lokasi, luas tanah, jumlah kamar tidur, tahun pembangunan, dan lainnya.
- Sumber Data: Data diperoleh dari kaggle [House price prediction](https://www.kaggle.com/datasets/shree1992/housedata?select=data.csv)

### Variabel-variabel pada Prediksi Harga Rumah adalah sebagai berikut:

- bedrooms : jumlah kamar tidur
- bathroom : jumlah kamar mandi
- sqft_living : Luas ruang hidup dalam feet persegi
- sqft_lot : Luas lahan dalam feet persegi
- floors : jumlah lantai
- waterfront : merujuk pada lokasi properti yang terletak di sepanjang garis pantai atau tepi air, seperti sungai, danau, atau laut
- view : mengacu pada apa yang dapat dilihat atau diperhatikan dari properti tersebut, terutama dari bagian dalam atau sekitar bangunan
- condition : merujuk pada keadaan atau status fisik umum dari properti tersebut
- sqft_above : luas lantai di atas permukaan tanah dalam feet persegi
- sqft_basement : luas lantai ruang bawah tanah dalam feet persegi
- yr_built : tahun dibangun
- yr_renovated : tahun renovasi dilakukan pada properti.
- street : alamat jalan properti
- city : alamat kota dari properti
<br>
Univariate Analisis<br>
variabel street
Dari gambar dapat disimpulkan bahwa, hampir semua lokasi berbeda beda. terdapat 3604 rumah yang tersebar di 3596 jalan.

![univariate_street](https://github.com/ariftampan/Submission1-MLT/assets/138217930/9236ce59-8c74-41b0-9d7c-53ee6075c4cd)


variabel city
<img width="226" alt="Screenshot 2024-02-13 175917" src="https://github.com/ariftampan/Submission1-MLT/assets/138217930/80407583-5d0a-4d04-9a50-c3c6eaeb23db">

![city](https://github.com/ariftampan/Submission1-MLT/assets/138217930/1888e8f7-b7eb-4eee-bbfa-8ab512a31773)

dari gambar disimpulkan bahwa rumah di seattle., renton dan bellevue menempati 50% dari jumlah rumah yang dijual.
<p>Numerical Analisis</p>

![download (3)](https://github.com/ariftampan/Submission1-MLT/assets/138217930/a11fb6f1-96a6-485c-af1f-6ad9ac7fcef9)
Apabila dicermati, dari histogram di atas, khususnya histogram untuk variabel price yang merupakan fitur target (label) pada data. Dari histogram price, dapat diperoleh beberapa informasi, antara lain:<br>
- Rentang harga rumah cukup tinggi yaitu dari skala seratusan ribu dolar Amerika hingga sekitar 1.100.000 an dollar Amerika. dengan lebih dari 50% berada dibawah 600 rb usd. <br>
- Distribusi harga miring ke kanan (right-skewed). Hal ini akan berimplikasi pada model.<br>

Multivariate Analisis<br>
Categorical Features<br>

![Multivariate-street](https://github.com/ariftampan/Submission1-MLT/assets/138217930/9b5bc4e2-8153-41c0-9cd7-f665b5788a9f)

![Multivariate-city](https://github.com/ariftampan/Submission1-MLT/assets/138217930/aae92dac-84a1-4094-9050-86cce0312b29)


Dari gambar diatas, korelasi antara categorical features dengan price, dapat diperoleh kesimpulan bahwa:
- pada fitur street, hampir setiap properties rumah menempati alamat yang berbeda beda. jadi tidak dapat diambil korelasi dari variabel street
- pada fitur city , yang menempati harga tertinggi di belevue dan kirkland seharga 1.15M USD
dari data diatas, dapat diambil kesimpulan kalau categorical fitur tidak korelasi secara langsung dnegan harga

Numerical Feature<br>
dari data, dapat diperoleh grafik sebagai berikut:

![multivariate-numerical](https://github.com/ariftampan/Submission1-MLT/assets/138217930/01c6075e-4801-4de5-b62e-f63402601cec)

Terlihat dari grafik diatas, relasi antara fitur numerik dengan fitur target yaitu price. sebaran data yang terpola terdapat pada grafik relasi antara sqft_living vs price dan sqft_above vs price.
dapat disimpulkan bahwa sqft_living dan sqft_above adalah yang memiliki relasi dominan terhadap price , terlebih bisa dilihat dengan tabel dibawah, dimana utk sqft_lving dan sqft_above memiliki nilai yang mendekati 1.

![tabel](https://github.com/ariftampan/Submission1-MLT/assets/138217930/634ab513-050b-4742-874a-d78a24f71f2c)


Kesimpulan Data Understanding:
Data yang digunakan untuk prediksi harga rumah mencakup berbagai fitur dan karakteristik properti. EDA telah membantu mendapatkan wawasan mendalam terhadap variabel-variabel tersebut dan hubungannya dengan harga. Data ini siap digunakan dalam pengembangan model machine learning untuk memprediksi harga rumah dengan lebih akurat, dengan fokus pada fitur-fitur yang signifikan yaitu <b>sqft_living</b>, dan <b>sqft_above</b> dalam menentukan nilai properti.

## Data Preparation

Pada tahap persiapan data (data preparation) proyek prediksi harga rumah, berbagai teknik telah diterapkan untuk memastikan bahwa dataset siap untuk digunakan dalam pengembangan model machine learning. Berikut adalah teknik-teknik yang diterapkan berurutan dalam notebook:

- Principal Component Analysis (PCA):
  Teknik PCA digunakan untuk mengurangi dimensi dari variabel-variabel yang berkorelasi tinggi.
  Komponen utama yang dihasilkan dari PCA digunakan sebagai fitur input alternatif dalam pengembangan model.
  Alasan Penggunaan: Pengurangan dimensi dengan PCA membantu mengatasi masalah multicollinearity dan dapat mempercepat proses pelatihan model. Ini juga dapat meningkatkan interpretabilitas model.

- Data Splitting:
  Dataset dibagi menjadi dua bagian: data latih (training set) dan data uji (test set). Proporsi pembagian, misalnya 90-10, disesuaikan dengan ukuran dataset.
  Alasan Penggunaan: Data splitting memungkinkan evaluasi yang objektif terhadap performa model pada data yang tidak digunakan selama pelatihan. Ini membantu menghindari overfitting dan menguji kemampuan generalisasi model.
  untuk mengurangi jumlah fitur atau variabel dalam dataset sambil mempertahankan sebanyak mungkin informasi maka dipakai teknik PCA (Principal Component Analysis)

- Standarisasi:
  Standarisasi dilakukan untuk mentransformasi variabel numerik yaitu sqft_living, dan sqft_above ke dalam distribusi dimension.
  Standarisasi menggunakan mean dan deviasi standar dari data latih untuk diterapkan pada data uji.
  Alasan Penggunaan: Standarisasi membantu model mengatasi perbedaan skala dan memastikan bahwa variabel-variabel memiliki rentang nilai yang seragam, mendukung performa model yang stabil.

Dampak Terhadap Model:

- PCA: Mengurangi dimensi dataset, menghilangkan korelasi tinggi antar-variabel, dan meningkatkan efisiensi pelatihan model.
- Data Splitting: Menghindari overfitting, mengevaluasi performa model secara objektif, dan menguji kemampuan generalisasi model.
- Standarisasi: Memastikan model dapat mengatasi perbedaan skala variabel dan meningkatkan stabilitas performa model.

Dengan menerapkan teknik-teknik data preparation ini, diharapkan dataset yang dihasilkan akan mendukung pengembangan model machine learning yang akurat, efisien, dan memiliki kemampuan generalisasi yang baik.

## Modeling

Dalam tahap pemodelan untuk proyek prediksi harga rumah, tiga model machine learning telah diterapkan: K-Nearest Neighbors (KNN), Random Forest (RF), dan Boosting Algoritm. Berikut adalah rincian mengenai setiap model:

K-Nearest Neighbors (KNN):
KNN adalah algoritma berbasis instan yang melakukan prediksi berdasarkan mayoritas label dari k-neighbors terdekat.
Tahapan Pemodelan:

- Menentukan jumlah tetangga (n_neighbors) yang optimal yaitu 10
- Menyesuaikan model dengan data latih.
- Melakukan prediksi pada data uji.
  Parameter yang Digunakan:
- Jumlah Tetangga (n_neighbors).
  Kelebihan:
  Sederhana, mudah diimplementasikan, cocok untuk data dengan distribusi yang kompleks.

Random Forest (RF):
RF adalah algoritma ensemble yang membangun beberapa pohon keputusan dan menggabungkan hasil prediksi mereka.
Tahapan Pemodelan:

- n_estimators: Jumlah pohon keputusan dalam ensemble. Dalam kasus ini, kita memilih 75 pohon.
- max_depth: Kedalaman maksimum dari setiap pohon keputusan. Diatur menjadi 20.
- random_state: Seed untuk mengontrol randomness agar hasilnya dapat direproduksi. Diatur menjadi 40.
- n_jobs: Menentukan jumlah pekerjaan paralel yang akan dijalankan selama pelatihan. Nilai -1 berarti menggunakan semua core yang tersedia.

Selanjutnya, hasil Mean Squared Error (MSE) dari prediksi model terhadap data latih disimpan dalam DataFrame 'models' pada baris 'train_mse' dan kolom 'RandomForest'. MSE merupakan metrik evaluasi yang umum digunakan untuk mengevaluasi performa model regresi, di mana nilai MSE yang lebih rendah menunjukkan performa model yang lebih baik.

Kelebihan: Stabil, tahan terhadap overfitting, mampu menangani data dengan banyak fitur.

K-Nearest Neighbor:
Algoritma boosting, seperti Gradient Boosting atau AdaBoost, membangun model secara berurutan dan memperbaiki kesalahan prediksi sebelumnya.
Tahapan Pemodelan:

- learning_rate: Tingkat kontribusi dari setiap model base. Nilai ini akan mengontrol seberapa besar bobot dari setiap model dalam ensemble. Pada contoh ini, diatur menjadi 0.05.
- random_state: Seed untuk mengontrol randomness agar hasilnya dapat direproduksi.
  Kelebihan: Meningkatkan akurasi model secara berangsur, tahan terhadap overfitting.

Perbandingan Kinerja:
Dari ketiga model, Random Forest (RF) dipilih sebagai model terbaik untuk prediksi harga rumah. Berikut adalah perbandingan kinerja RF dengan KNN dan Boosting:

KNN vs. RF vs. Boosting Algoritm:

- RF menunjukkan kinerja yang lebih baik dibandingkan KNN dan Boosting pada sebagian besar metrik evaluasi.
- Kelebihan RF: Mampu menangani ketergantungan dan interaksi yang kompleks antar fitur.
- Tahan terhadap overfitting.
- Stabil dan konsisten dalam berbagai kondisi.

Detail Perbandingan Kinerja:

- Akurasi: RF memiliki akurasi yang lebih tinggi dibandingkan KNN dan Boosting pada data uji.
- Mean Squared Error (MSE): RF memberikan MSE yang lebih rendah, menunjukkan keakuratan prediksi yang lebih baik.
- Waktu Pelatihan: Meskipun RF mungkin memerlukan waktu pelatihan lebih lama, hasilnya memberikan keseimbangan yang baik antara waktu pelatihan dan kinerja model.

Kesimpulan:
Berdasarkan perbandingan kinerja, Random Forest (RF) terbukti menjadi model yang unggul dalam prediksi harga rumah. Keakuratan dan kestabilan RF menjadikannya pilihan yang efektif dan dapat diandalkan untuk menangani kompleksitas dalam dataset ini. Dengan demikian, RF dianggap sebagai model terbaik untuk tugas prediksi harga rumah dalam konteks proyek ini.

## Evaluation

Metrik Evaluasi: Mean Squared Error (MSE)

Formula Metrik:
MSE merupakan metrik evaluasi yang mengukur rata-rata dari kuadrat selisih antara nilai sebenarnya dan nilai prediksi. Formula MSE dapat dihitung dengan rumus berikut:

Dimana:
N: jumlah observasi.
yi: nilai sebenarnya.
y_pred: nilai prediksi

Cara Kerja Metrik:
MSE mengukur seberapa besar kesalahan prediksi model dengan cara mengevaluasi seberapa besar deviasi antara nilai sebenarnya dan nilai prediksi, kemudian menghitung rata-rata kuadrat dari deviasi tersebut. MSE memberikan bobot lebih besar pada kesalahan yang lebih besar, sehingga mengindikasikan seberapa buruk performa model dalam memprediksi data.

Interpretasi Nilai MSE:
Nilai MSE yang lebih rendah menunjukkan bahwa model memiliki tingkat kesalahan yang lebih kecil.
Nilai MSE yang lebih tinggi mengindikasikan bahwa model memiliki tingkat kesalahan yang lebih besar.

Dampak Praktis:
Dalam konteks prediksi harga rumah, nilai MSE yang rendah menunjukkan bahwa model memberikan prediksi harga yang akurat dan mendekati nilai sebenarnya.
Sebaliknya, nilai MSE yang tinggi menunjukkan bahwa model memiliki tingkat kesalahan yang besar dalam memprediksi harga rumah.

Hasil Metrik Evaluasi:
Dari hasil evaluasi menggunakan MSE pada data latih dan data uji, kita dapat:
Membandingkan performa relatif dari model KNN, Random Forest (RF), dan Boosting.
Menilai seberapa baik model-model tersebut dalam menghasilkan prediksi harga rumah yang akurat.
Menyesuaikan model atau parameter jika diperlukan untuk meningkatkan performa.

Kesimpulan:
Model dengan nilai MSE yang lebih rendah dianggap lebih baik dalam konteks ini.
Evaluasi ini membantu memahami seberapa efektif model dalam memenuhi goals proyek, yaitu memberikan prediksi harga rumah yang akurat dan relevan.
