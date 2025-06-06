# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding

Jaya Jaya Institut merupakan salah satu institusi pendidikan perguruan yang telah berdiri sejak tahun 2000. Hingga saat ini ia telah mencetak banyak lulusan dengan reputasi yang sangat baik.

### Permasalahan Bisnis

1. **Tingkat Dropout yang Tinggi** : Jumlah siswa yang meninggalkan sekolah atau meninggalkan Jaya Jaya Institut sangat besar. Ini dapat membahayakan reputasi institusi dan mengurangi pendapatan dari jumlah siswa yang lulus.

2. **Resiko Kehilangan Potensi** : Setiap siswa yang meninggalkan sekolah mewakili potensi yang hilang dalam hal kontribusi akademik, karir, dan sosial.

3. **Kebutuhan untuk Interenvensi Dini** : Institusi harus segera mengidentifikasi siswa dengan risiko dropout yang tinggi agar mereka dapat memberikan bimbingan khusus dan intervensi yang diperlukan untuk membantu siswa menyelesaikan pendidikannya.

4. **Kebutuhan Dashboard** : Diperlukan dashboard yang dapat memberikan informasi yang relevan dan mudah dipahami sehingga institusi pendidikan dapat mengambil tindakan proaktif untuk memantau prestasi siswa dan mengidentifikasi siswa yang berpotensi gagal.

5. **Penyelidikan Faktor Penyebab** : Penting untuk menyelidiki faktor-faktor yang mungkin menyebabkan tingginya tingkat dropout, seperti masalah akademik, masalah keuangan, masalah pribadi, atau kurangnya dukungan sosial.

### Cakupan Proyek

Berdasarkan permasalahan bisnis yang telah diidentifikasi, cakupan proyek dapat mencakup beberapa tahapan, antara lain :

1. Data Preparation:

- Pengumpulan dan pembersihan data: Memastikan data yang diperlukan tersedia dan dalam format yang sesuai untuk analisis.
- Pemrosesan data: Melakukan transformasi dan penyatuan data jika diperlukan untuk mempersiapkannya untuk analisis.

2. Analisis Eksploratif:

- Eksplorasi data: Menganalisis distribusi variabel, korelasi antar variabel, dan pola-pola yang mungkin terdapat dalam data.
- Identifikasi faktor-faktor potensial yang berkaitan dengan dropout: Mengidentifikasi variabel-variabel yang dapat menjadi prediktor atau indikator dropout siswa.

3. Model Prediksi Dropout:

- Pengembangan model prediksi: Membangun model statistik atau machine learning untuk memprediksi kemungkinan dropout siswa berdasarkan faktor-faktor yang telah diidentifikasi.
- Evaluasi model: Mengukur kinerja model untuk memastikan akurasi dan keandalannya.

4. Intervensi dan Bimbingan:

- Pengembangan strategi intervensi: Merancang program bimbingan dan intervensi yang sesuai untuk siswa yang berisiko tinggi dropout.
- Implementasi strategi: Melaksanakan program bimbingan dan intervensi kepada siswa yang telah diidentifikasi sebagai berisiko tinggi.

5. Monitoring dan Evaluasi:

- Pengembangan dashboard: Membangun dashboard atau laporan interaktif untuk memantau performa siswa secara kontinu dan mendeteksi perubahan dalam tingkat dropout.
- Evaluasi efektivitas: Mengevaluasi efektivitas strategi intervensi dan mengidentifikasi perubahan dalam tingkat dropout.

### Persiapan

Sumber data: https://raw.githubusercontent.com/dicodingacademy/dicoding_dataset/main/students_performance/data.csv

Setup environment:

#### Library Installation

1. Pastikan python sudah terinstall dalam device anda, untuk mengetahuinya dapat dengan membuka Command Prompt lalu ketik perintah seperti berikut

```
python --version
```

2. Jika sudah dipastikan bahwa python sudah terinstall dalam device anda, maka sekarang pastikan pip sudah terinstall dengan ketik perintah sebagai berikut di command prompt

```
pip --version
```

3. Jika sudah terinstall anda bisa melakukan install library-library yang dibutuhkan pada proyek ini dengan mengetik perintah berikut pada command prompt

```
pip install requirements.txt
```

#### Running Streamlit

1. Pastikan semua library dan model joblib semua siap, lalu jalankan perintah berikut untuk menjalankan aplikasi prediksi pada proyek ini

```
streamlit run app.py
```

#### looker studio (Dashboard)
https://lookerstudio.google.com/reporting/a6feb3af-a743-4a96-b98f-d94cbec0906e 


## Business Dashboard


Pada Jaya Jaya Institut terdapat total 4424 siswa, dimana 1421 siswa sudah dinyatakan dropout. Dimana rata-rata siswa dropout memiliki angka penggagurannya cukup besar yaitu 11.62%.

Adapun beberapa faktor yang mempengaruhi status siswa antara lain antara lain variabel tuition fees up to date, scholarship holder, debtor, nacionality dan seterusnya yang dapat dilihat pada bagian feature important pada dashboard.



## Menjalankan Sistem Machine Learning

Untuk menjalankan sistem prediksi yang dibangun, pengguna harus memastikan sudah memasukan data sebenarnya. Dimana data yang perlu dimasukan dibagi menjadi beberapa section yaitu :

1. Personal Information, antara lain : Gender, Marital Status, Nacionality, Father Occupation, Father Qualification, Mother Occupation, Mother Qualification
2. Application Information, antara lain : DayTime Evening Attendance, Previous Qualification, International Student, Application Mode, Course, Admission Grade, Previous Qualification Grade, Displaced, Education Special Needs
3. Financial Information, antara lain : Debtor, Scholarship Holder, Tuition Fees Up To Date
4. Student Progress, antara lain : Curricular Units 1st Sem & 2nd Sem Enrolled, Curricular Units 1st & 2nd Sem Evaluations, Curricular Units 1st Sem & 2nd Approved, Curricular Units 1st & 2nd Sem Grade, Applciation Order, Age at Enrollment, Unemployment Rate, Inflation Rate, GDP

Lalu setelah keseluruhan data yang sudah diisi, pengguna dapat melihat data yang dimasukan pada table dengan menekan bagian _View the Raw Data_ menekan Tombol _Predict_ untuk melakukan prediksi menurut data yang sudah dimasukan.

Perlu diketahui sitem prediksi yang dibangun menggunakan Gradient Boosting model.

Dimana jika sistem berhasil melakukan prediksi, maka akan mengeluarkan status seperti berikut :

1. Graduate : Siswa memiliki status lulus
2. Enrolled : Siswa yang masih aktif menjalani akademik
3. Dropout : Siswa yang sudah keluar dari kegiatan akademisi


Sistem prediksi ini dapat dilihat pada link berikut :
https://proyek-akhir-course-bpds-diazdarsya.streamlit.app/ 

## Conclusion

Terdapat berbagai faktor yang dapat mengakibatkan siswa mengalami dropout :

1. Finansial : siswa yang memiliki finansial yang buruk lebih rentan mengalami dropout. Keterlambatan dalam membayar juga dapat mengakibatkannya. Data ini dapat juga terlihat melalui nilai rata-rata keseluruhan GDP siswa yang dropout.
2. Program studi : program studi dengan jumlah siswa terbanyak lebih banyak mengalami dropout.
3. Beasiswa : walau tidak banyak berpengaruh, namun perlu diperhatikan kembali oleh instansi bahwa sasaran siswa yang mendapatkan beasiswa itu harus tepat.
4. Usia : usia muda lebih rentan mengalami dropout
5. Jumlah kurikulum : Siswa dengan jumlah kurikulum yang diambil lebih rentan mengalami dropout

Untuk mendalami dan memprediksi siswa yang rentan mengalami dropout, penulis membangun sebuah model machine learning menggunakan beberapa model dan beberapa feature data numerik yang dipakai diantaranya :

- Curricular_units_1st_sem_enrolled
- Curricular_units_1st_sem_evaluations
- Curricular_units_1st_sem_approved
- Curricular_units_1st_sem_grade
- Curricular_units_2nd_sem_enrolled
- Curricular_units_2nd_sem_evaluations
- Curricular_units_2nd_sem_approved
- Curricular_units_2nd_sem_grade
- Application_order
- Age_at_enrollment
- Unemployment_rate
- Inflation_rate
- GDP

1. Logistic Regression (accuracy : 62%)
2. Decision Tree (accuracy : 65%)
3. Random Forest (accuracy : 76%)
4. Gradient Boosting (accuracy : 91%)
5. XGBClassifier (accuracy : 90%)

Jadi, kami menemukan bahwa Gradient Boosting adalah model yang tepat untuk prediksi proyek ini, dan model ini menggunakan pc1_1 sebagai fitur utama untuk membuat prediksi.



### Rekomendasi Action Items

Berdasarkan data yang sudah dianalisis, didapatkan bahwa Jaya Jaya institusi dapat melakukan beberapa aksi untuk mencegah siswa mengalami dropout : </br>

1. Analisis Kinerja Akademik: Untuk mengevaluasi kinerja akademik siswa dan menemukan area perbaikan, tinjau data tentang mata kuliah yang diambil, kehadiran di kelas, kualifikasi sebelumnya, dan nilai.
2. Melakukan Pengembangan Program Dukungan: Institusi dapat membuat inisiatif untuk meningkatkan kesehatan dan kinerja siswa dengan mengumpulkan data tentang kebutuhan pendidikan khusus, status keuangan, dan kemampuan orang tua.
3. Melakukan Pemantauan Pembayaran Uang Kuliah: Tinjau data tentang utang siswa dan keterlambatan pembayaran uang kuliah untuk memastikan bahwa siswa memiliki sumber daya keuangan yang memadai dan untuk mengatasi masalah keuangan yang mungkin mengganggu pendidikan mereka.
4. Analisis Dampak Faktor Ekonomi: Untuk memahami dampak faktor ekonomi terhadap pendidikan dan kesejahteraan siswa, tinjau data tentang tingkat pengangguran, tingkat inflasi, dan PDB.
5. Pengembangan Program Beasiswa: Institusi dapat membuat program beasiswa yang tepat untuk membantu siswa yang berprestasi dan berkebutuhan keuangan berdasarkan data penerima beasiswa.
