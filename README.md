# Purwadhika_Final_Project
# Machine Learning Model for Predicting Used Car Price in UK
![alt text](https://github.com/PurwadhikaDev/DataRangersTeam_JC_DS_VL_05_FinalProject/blob/main/Picture/jpeg%20awal.jpg?raw=true)  
## BUSINESS UNDERSTANDING
### *CONTEXT*

Di tengah menurunnya pasokan mobil baru di Inggris Raya dikarenakan minimnya pasokan semikonduktor, banyak pelanggan mobil yang mulai beralih ke mobil bekas. Hal ini ditunjukkan dari data Society of Motor Manufacturers and Traders (SMMT) pertumbuhan penjualan mobil baru yang hanya 1% pada tahun 2021 dibandingkan dengan mobil bekas yang sebesar 11.5% (SMMT. https://www.smmt.co.uk/category/vehicle-data/used-car-sales-data/).
PT ABC adalah salah satu lembaga showroom mobil bekas yang berperan sebagai pihak yang membeli mobil bekas dari penjual mobil bekas, baik itu perorangan maupun lembaga dan menjual mobil bekas tersebut kepada calon pembeli. PT ABC akan melakukan penilaian harga mobil bekas yang akan dijual dan juga melakukan inspeksi dan kurasi untuk memeriksa keadaan mobil. PT ABC mengambil keuntungan 5% dari selisih harga beli dan harga jual mobil bekas.
Di tengah aktivitas pasar mobil bekas yang terus meningkat, PT ABC ingin dapat mendapat gambaran harga pasar mobil bekas yang akurat. Tim Data Analyst Rangers PT ABC bertugas untuk memprediksi harga mobil bekas sesuai dengan kebutuhan PT ABC.

### *PROBLEM STATEMENT*

Di tengah aktivitas pasar mobil bekas yang terus meningkat, kepercayaan konsumen menjadi sangat penting. Bila harga yang dinilai oleh PT ABC tidak akurat, maka konsumen mobil bekas akan beralih ke pesaing lainnya, sehingga PT ABC akan menderita kerugian.

### *GOALS*

Berdasarkan permasalahan tersebut, perusahaan ingin menilai harga mobil bekas dengan sebaik mungkin agar kepercayaan konsumen meningkat dan akhirnya PT ABC menjadi top of mind tempat jual beli mobil bekas.

### *METRIC EVALUATION*

Evaluasi metrik yang akan digunakan adalah MAPE, dimana MAPE adalah rataan persentase error yang dihasilkan oleh model regresi. Semakin kecil nilai MAPE yang dihasilkan, berarti model semakin akurat dalam memprediksi harga mobil bekas.

Selain itu, kita juga bisa menggunakan nilai R-squared (R2). Nilai R-squared digunakan untuk mengetahui seberapa baik model dapat merepresentasikan varians keseluruhan data. Semakin mendekati 1, maka semakin fit pula modelnya terhadap data observasi.

## DATA UNDERSTANDING
  
Dataset dapat diambil pada link: https://www.kaggle.com/datasets/adityadesai13/used-car-dataset-ford-and-mercedes?datasetId=750216&sortBy=voteCount
![alt text](https://github.com/PurwadhikaDev/DataRangersTeam_JC_DS_VL_05_FinalProject/blob/main/Picture/Data%20understanding12.png?raw=true)  

## EDA OVERVIEW

![alt text](https://github.com/risnandastrm/Purwadhika_Final_Project/blob/main/Picture/price%20dist.png?raw=true)    
Distribusi harga mobil cenderung berdistribusi right skewed. Artinya tidak banyak mobil yang memiliki harga yang tinggi dan mayoritas data berada pada harga €10000-21000.


![alt text](https://github.com/PurwadhikaDev/DataRangersTeam_JC_DS_VL_05_FinalProject/blob/main/Picture/Merk%20mobil.png?raw=true)    
Terlihat dari grafik di atas, mobil bekas yang paling banyak terjual di Inggris adalah merk **Ford** diikuti oleh merk **VW**.  
Dikarenakan tipe mobil yang banyak terjual adalah tipe city car yang praktis, maka PT ABC dapat menggencarkan promosi penjualan mobil- mobil sejenis dan juga memprioritaskan untuk membeli mobil bekas dari tipe- tipe tersebut.
  
    
    

![alt text](https://github.com/PurwadhikaDev/DataRangersTeam_JC_DS_VL_05_FinalProject/blob/main/Picture/Model%20mobil.png?raw=true)  
Berdasarkan grafik diatas, terlihat model **Ford Fiesta** menjadi model yang paling banyak terjual. Selain itu, hampir semua model yang paling banyak terjual masuk ke kategori mobil kecil dan juga city car, kecuali **Mercedes C-Class** yang termasuk ke dalam kategori mobil mewah.

## MODELLING
Kami melakukan modelling dengan algoritma Linear Regression, Decision Tree, Random Forest, dan XGBoost.  
![alt text](https://github.com/PurwadhikaDev/DataRangersTeam_JC_DS_VL_05_FinalProject/blob/main/Picture/Model-model.png?raw=true)  
Setelah dilihat, terlihat Random Forest merupakan algoritma dengan hasil terbaik.    
  
    
    

![alt text](https://github.com/PurwadhikaDev/DataRangersTeam_JC_DS_VL_05_FinalProject/blob/main/Picture/Before%20improvement.png?raw=true)  
Selanjutnya, setelah dilakukan hyperparameter tuning, terlihat bahwa model setelah dituning menunjukkan hasil yang lebih baik.  

### *MODEL IMPROVEMENT* 
Kami melakukan model improvement agar hasil prediksi model menjadi lebih baik.  
![alt text](https://github.com/PurwadhikaDev/DataRangersTeam_JC_DS_VL_05_FinalProject/blob/main/Picture/After%20improvement.png?raw=true)  
Setelah dilakukan modelling setelah improvement, terlihat performa model Random Forest membaik dari sisi MAPE maupun R-Squared.

## EVALUATION

### *FEATURE IMPORTANCE*
![alt text](https://github.com/PurwadhikaDev/DataRangersTeam_JC_DS_VL_05_FinalProject/blob/main/Picture/Feature%20importance.png?raw=true) 
Berdasarkan feature importance diatas setelah dilakukan improvement model, terdapat sedikit perbedaan dari feature importance sebelumnya dimana fitur yang paling berpengaruh kali ini terhadap harga adalah fitur enginesize (kapasitas mesin), mpg (miles per galon), year (tahun produksi mobil), transmisi kendaraan.  

## CONCLUSION


- Berdasarkan hasil EDA, terlihat mobil bekas yang paling banyak terjual adalah mobil merk Ford. Hal ini disebabkan oleh harga mobil Ford yang cenderung terjangkau (carblog.co.uk, "Why Is Ford The Most Popular Car Make In The UK?". https://www.carblog.co.uk/why-is-ford-the-most-popular-car-make-in-the-uk/).

- Berdasarkan hasil EDA, terlihat banyak mobil jenis city car dan mobil- mobil kecil seperti Ford Fiesta dan VW Golf laku terjual di Inggris Raya. Hal ini mengindikasikan preferensi konsumen Inggris Raya terhadap mobil- mobil jenis tersebut.

- Berdasarkan hasil data feature importance setelah model improvement, maka fitur yang paling berpengaruh terhadap perbedaan harga jual mobil bekas di UK adalah fitur kapasitas mesin dari mobil itu sendiri. Kemudian disusul oleh efisiensi mobil yang ditunjukkan oleh satuan mile per gallon. Hal ini cukup beralasan karena semakin tinggi kapasitas mesin mobil artinya semakin besar pula tenaga mobil tersebut yang menyebabkan harga mobil semakin mahal. Sementara untuk fitur mpg, efisiensi mobil banyak mempengaruhi harga dan juga fitur lainnya, seperti mileage dan tax. Mobil yang efisien juga berpengaruh pada biaya yang harus dikeluarkan untuk bahan bakar.

- Dilihat dari hasil score metric yang digunakan pada model setelah improvement. Model Random Forest Regressor menghasilkan nilai skor MAPE sebesar 0.070563 atau 7% error rate. Berdasarkan Lewis (1982), nilai skor MAPE yang berada di bawah 10% dapat dikategorikan bahwa hasil prediksi nya "Sangat Baik". Sebagai contoh, jika data aktual harga mobil sebesar 100000, maka harga prediksi akan berada di rentang minimal -7% hingga +7% dari harga aktual, jika ternyata berada di luar rentang tersebut artinya terjadi bias pada hasil prediksi.

- Sementara untuk R-Squared, model menghasilkan skor sebesar 0.962187 atau 96%, yang artinya model dapat menjelaskan variabel dependent (price) sebesar 96%, sementara yang sisanya 4% dijelaskan oleh variabel lain diluar variabel independent atau secara sederhana dapat dikatakan bahwa fitur-fitur input yang digunakan cukup berpengaruh terhadap perubahan harga yang menjadi target prediksi. Berdasarkan Hair et al (2011) nilai skor R-Squared yang berada di atas 0.75 / 75% termasuk kategori "Kuat"

- Dengan adanya model ini, diharapkan prediksi harga mobil untuk Showroom PT ABC dapat lebih objektif terhadap data, hemat waktu, dan dapat meningkatkan kepercayaan konsumen.


## RECOMMENDATION / NEXT SUGGESTION
Berikut adalah beberapa hal yang dapat dilakukan untuk pengembangan model dan bisnis agar bisa lebih baik lagi.

- Melihat kembali data predict, lalu menganalisa data-data yang memiliki error yang paling tinggi, dan membandingkan fitur-fitur mana saja yang menyebabkan model menghasilkan error tersebut.

- Jika memungkinkan, dilakukan penambahan fitur yang memiliki hubungan yang lebih korelatif dengan fitur harga. Untuk kasus ini, mungkin dapat ditambahkan fitur seperti kondisi fisik mobil, kelengkapan surat-surat, masa berlaku pajak, dll sehingga diharapkan dapat meningkatkan kemampuan model dalam memprediksi harga

- Menambah fitur kategori model mobil agar lebih detail. Contohnya BMW 2 Series, BMW 2 Series Tourer, dan BMW 2 Series Coupe.

- Melakukan data cleaning yang lebih mendalam pada fitur-fitur data yang masih bias pada dataset ini. Contohnya pada fitur fuelType masih terdapat tipe bahan bakar "other", hal ini sebaiknya diubah dan disesuaikan dengan jenis bahan bakar yang sebenarnya digunakan. Hal ini juga berlaku untuk fitur-fitur lainnya yang memiliki value yang berbeda dari yang data real sebenarnya. Dengan tujuan untuk mengurangi bias yang terjadi pada data-data tersebut. Karena data yang clean adalah kunci utama untuk bisa menghasilkan model yang terbaik

- Mencoba beberapa teknik feature engineering lainnya seperti binning pada data-data numerikal atau scaling menggunakan logaritmic scale pada data-data yang memiliki distribusi tidak normal.

- Menekankan prediksi yang underpriced dibandingkan overpriced.

- EDA yang bisa lebih difokuskan untuk target/label (harga mobil)
