# CUSTOMER CHURN PREDICTION MODEL FOR TELCO COMPANY

📌 **Background:**
Telco Company menghadapi tantangan dalam mempertahankan pelanggan akibat tingginya angka *customer churn*, yang berdampak langsung pada penurunan pendapatan dan peningkatan biaya akuisisi pelanggan baru. Sistem prediksi churn sebelumnya masih berbasis *rule-based*, yang tidak mampu menangkap pola kompleks dari perilaku pelanggan yang berhenti berlangganan.

Melalui proyek ini, perusahaan berupaya membangun model prediktif berbasis *machine learning* untuk mengidentifikasi pelanggan yang berpotensi churn secara lebih akurat. Dengan menggunakan data historis pelanggan yang mencakup informasi demografi, perilaku langganan, jenis kontrak, dan biaya bulanan, model ini diharapkan dapat mengurangi churn dan meningkatkan efisiensi strategi retensi.

Untuk meminimalisir kerugian dari kesalahan klasifikasi (khususnya false negative), model ini difokuskan untuk memaksimalkan **recall**, sehingga pelanggan yang sebenarnya berisiko churn dapat ditangani lebih awal melalui intervensi bisnis.

---

❓ **Problem Statement:**
- Bagaimana membangun model machine learning yang mampu memprediksi pelanggan berisiko churn secara akurat ?
- Fitur-fitur apa saja yang paling berkontribusi dalam menentukan risiko churn dan bagaimana fitur tersebut dapat dimanfaatkan oleh tim bisnis untuk strategi retensi?

---

🎯 **Goals:**
1. Mengembangkan model prediktif churn dengan akurasi tinggi dan ketahanan terhadap ketidakseimbangan data.
2. Menemukan fitur-fitur paling penting yang menjadi indikator utama terjadinya churn.
3. Menyediakan hasil interpretasi dan threshold optimal untuk membantu pengambilan keputusan yang tepat sasaran.

---

⚙️ **Analytic Approach:**
- Menggunakan berbagai algoritma klasifikasi seperti **GradientBoostingClassifier**, serta pembandingan awal dengan model lain seperti XGBoost, CatBoost, dan LightGBM.
- Penanganan ketidakseimbangan data melalui teknik **SMOTEENN**.
- Penyesuaian threshold menggunakan **optimasi F2-Score** untuk meningkatkan kemampuan deteksi churn.
- Feature selection dan interpretabilitas melalui **SHAP analysis** dan korelasi.
- Validasi performa model menggunakan **Cross Validation**, **Learning Curve**, dan **ROC Curve**.

---

📏 **Metric Evaluation:**
- **F2-Score (Utama)**  
  F2 dipilih sebagai metrik utama karena lebih mengutamakan **recall**, yang penting dalam konteks churn untuk mendeteksi sebanyak mungkin pelanggan yang akan berhenti. Ini memungkinkan intervensi lebih awal dan mengurangi risiko kehilangan pelanggan bernilai tinggi.

- **F1-Score (Pelengkap)**  
  Digunakan untuk memastikan bahwa recall yang tinggi tidak diperoleh dengan mengorbankan precision secara drastis.

- **ROC-AUC (Pendukung)**  
  Digunakan sebagai metrik tambahan untuk mengevaluasi kualitas klasifikasi secara menyeluruh dalam membedakan kelas churn dan non-churn.

---

Dengan pendekatan ini, diharapkan Telco Company dapat lebih efektif dalam mempertahankan pelanggan melalui model prediktif yang tidak hanya akurat, tetapi juga **interpretable** dan **actionable** bagi unit bisnis terkait.
