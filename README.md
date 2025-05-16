![imagegojo](https://github.com/user-attachments/assets/d368d16f-73cd-4449-812a-ea9892d50bbf)


Eksperimen dilakukan pada empat dataset dengan dua versi tiap data: versi asli yang masih mengandung outlier (D1), dan versi bersih hasil preprocessing (D2) menggunakan metode IQR. Total ada delapan data uji yang dibagi secara acak (train-test split 80:20). CatBoost langsung digunakan dengan pengaturan default, sementara Random Forest diuji dua kali: pertama dengan setting default, lalu dengan tuning intensif terhadap parameter utama (seperti n_estimators, max_depth, min_samples_split) dan eksplorasi random_state.

Hasilnya? CatBoost konsisten unggul di awal—efektif, cepat, dan minim repot. Namun, setelah melalui serangkaian tuning, Random Forest mulai menunjukkan taringnya, terutama ketika random_state ikut dioptimasi. Hal ini mengungkap fakta menarik: meski sering diabaikan, random_state bisa menjadi kunci performa model, terutama untuk algoritma seperti Random Forest yang sensitif terhadap inisialisasi acak.

Outlier juga menjadi medan uji ketangguhan. CatBoost terbukti lebih tangguh di data mentah, menunjukkan resiliensi terhadap noise. Sementara itu, Random Forest lebih rewel dan baru stabil setelah data dipoles dan hyperparameter diatur dengan cermat.
