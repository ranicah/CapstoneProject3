# CapstoneProject3

Customer Life Value atau CLV, adalah ukuran seberapa berharganya seorang pelanggan bagi perusahaan. Dari nilai ini, perusahaan dapat menentukan berapa banyak keuntungan yang diperoleh dari satu penumpang dan biaya yang dikeluarkan untuk mendapatkan atau mempertahankan pelanggan baru. Angka ini cukup penting bagi perusahaan untuk mengetahui apakah perusahaan ingin menargetkan pemasaran kepada pelanggan berharga secara efektif dan bagaimana pelanggan perusahaan akan berubah di masa mendatang.

Pada capstone ini, diambil contoh pada perusahaan Elektronik EL, dimana perusahaan ingin mengoptimalkan layanan jasa mereka terhadap pelanggan dengan marketing yang belum fokus ditujukan untuk siapa sehingga biaya marketing membludak dan harus menekan biaya operasional lainnya, sehingga perusahaan ingin melihat seberapa tepat nilai prediksi dari pelanggan untuk menentukan pelanggan VIP (CLV tinggi) yang bertujuan untuk alokasi anggaran marketing dapat digunakan secara optimal.

Sebagai data analis, langkah-langkah yang dilakukan dalam prediksi CLV perusahaan Elektronik EL adalah sebagai berikut:
## 1. Data Understanding
  Memahami dataset termasuk baris dan kolom didalamnya menjadi pondasi awal sebagai data analis memahami data yang akan diproses ke langkah selanjutnya. Dalam dataset CLV, terdapat 11 kolom dan 5669 baris. 
  
## 2. Data Cleaning
  Data Cleaning dalam proses ini difokuskan menghapus nilai kosong dan data duplikat. Dalam dataset terdapat 618 duplikat yang langsung didrop. 
  
## 3. Pemilihan model dan evaluasi matrix
  Dataset yang dimiliki merupakan regresi sehingga model yang digunakan dalam prediksi CLV diantaranya adalah:
  - Linear Regression (efisien untuk mendeteksi pola linear dalam data)
  - Random Forest (memiliki resistensi tinggi terhadap struktur yang unik)
  - Elastic Net (kombinasi lasso dan ridge, memiliki kapabilitas dalam meng-handle model yang kompleks dengan korelasi yang tinggi)
  - Stacking (meningkatkan akurasi prediksi)
  - XGBoost (banyak digunakan karena cepat, akurat, dan efisiensi tinggi untuk permodelan)
  - Lasso dan Ridge (Pengujian Lasso dan Ridge untuk melihat apakah lebih baik dilakukan independen atau digabungkan)
    
  Evaluasi matrix yang digunakan adalah sebagai berikut:
  - MAE (mudah diinterpretasikan)
  - MAPE (mudah dimengerti bisnis, selain MAE)
  - RMSE (mengurangi pengaruh outlier skala besar)
  - R^2 (skor relatif terhadap model baseline (mean))
    Pada pengaplikasikaannya, MAE digunakan dalam penentuan model terbaik dikarenakan mudah diinterpretasikan ke dalam bisnis dan mudah dipahami oleh stakeholder.

  Algoritma model dan evaluasi matrix diaplikasikan dalam 3 eksperimen yaitu model sederhana, based model, dan tanpa outlier (outlier dihapus terlebih dahulu dalam eksperimen ini) untuk dapat hasil terbaik. 
    
## 4. Hyperparameter tuning
  Tuning ditujukan untuk membantu nilai model terbaik semakin baik nilainya. Dari ketiga eksperimen, model terbaik adalah XGBoost Tanpa Outlier. Tuning yang dilakukan dilakukan dengan dua cara yaitu random search dan grid search.

## 5. Evaluasi model terbaik
  Hasil akhir model terbaik yaitu XGBoost Tanpa Outlier sebelum dituning. Setelahnya dapat dilakukan plotting untuk melihat ketepatan prediksi CLV terhadap nilai aktualnya, sehingga dapat dilakukan rekomendasi bisnis dan model yang        telah digunakan. 

  Secara lengkapnya dapat dilihat dalam colab dan slideshow yang telah terlampir. 

  
