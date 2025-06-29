# 🪴GREEN FINANCE-ANALISIS PROYEK BIOENERGI BERKELANJUTAN

**Hai,Sobat ETL!! 👋**

Semoga kabar kalian baik dan tetap semangat selalu dalam perjalanan belajarmu 💪📚. 

Selamat datang di "Studi Kasus Green Finance: Analisis Proyek Bioenergi Berkelanjutan"— repositori ini adalah bagian dari self-learning journey kita untuk mendalami green finance, atau sederhananya: menganalisis bagaimana keuangan dapat digunakan untuk membiayai proyek-proyek yang peduli terhadap lingkungan dan masyarakat 🏛️💸.

## 🎯 Tujuan
Tujuan dari proyek ini adalah:

1. **Memahami Konsep Green Finance dari Sisi Data:** Menjelajahi bagaimana data dapat mengungkapkan dampak finansial, lingkungan, dan sosial dari proyek-proyek hijau.

2. **Melihat Analisis Green Finance Berdampak Terhadap Lingkungan dan Sosial yang Terukur:** Mengidentifikasi metrik kunci untuk mengukur kontribusi nyata proyek terhadap keberlanjutan.

3. **Bagaimana Kita Dapat Menggunakan Data Historis untuk Memprediksi Keberhasilan dan Risiko Proyek Hijau:** Mempelajari pola dan tren dari data masa lalu untuk memitigasi risiko dan mengoptimalkan potensi proyek masa depan.

4. **Membedah Berbagai Variabel dalam Dataset yang Relevan:** Menganalisis beragam data, mulai dari aspek teknis proyek, dampak ekologis, hingga manfaat sosial-ekonomi.

## 1. Deskripsi Green Finance

*Green Finance* adalah sebuah strategi keuangan yang memprioritaskan investasi dan pembiayaan untuk inisiatif yang memberikan dampak positif pada lingkungan. Fokus utamanya adalah mendukung transisi menuju ekonomi sirkular dan regeneratif, termasuk pembiayaan untuk:

1. **Bioenergi Berkelanjutan** (seperti produksi biogas dari limbah organik dan biomassa)

2. **Pertanian Berkelanjutan** (penggunaan praktik pertanian ramah lingkungan)

3. **Konservasi Biodiversitas**

4. **Pengelolaan Air Terpadu**

5. **Inovasi Ramah Lingkungan**

Komponen Utama *Green Finance* adalah **Investasi Hijau** yang merupakan proyek dengan dampak lingkungan positif, seperti mengurangi limbah, merehabilitasi lahan, atau mendukung keanekaragaman hayati. Dan Instrumen Keuangan yang terdiri dari *Green Bond, Green Loan, dan ESG Fund (Environmental, Social, Governance).*

Sedangkan untuk manfaat Green Finance adalah:

1. Mendukung pencapaian target Tujuan Pembangunan Berkelanjutan (SDGs).

2. Meningkatkan resiliensi terhadap krisis lingkungan dan sosial.

3. Menciptakan nilai jangka panjang bagi pemangku kepentingan dan masyarakat.

4. Menarik modal dari investor yang berfokus pada keberlanjutan (misalnya **sustainability-linked financing** dengan insentif kinerja ESG).

### ⚖️ Regulasi Green Finance di Indonesia

**1. Taksonomi Hijau Indonesia (THI) – OJK 2022**

Merupakan sistem klasifikasi yang memandu kegiatan ekonomi mana yang dikategorikan sebagai **"HIJAU"**, menetapkan kriteria dan sektor prioritas.

**2. POJK No. 60/POJK.04/2017**

Mengatur penerbitan *Green Bond*, mencakup:

- **Kewajiban pelaporan dampak lingkungan dari proyek yang dibiayai.**

- **Penilaian kelayakan dan validasi proyek hijau oleh pihak ketiga.**

**3. POJK No. 51/POJK.03/2017**

Mewajibkan lembaga keuangan untuk:

- **Menyusun Rencana Aksi Keuangan Berkelanjutan (RAKB).**

- **Mengevaluasi portofolio berdasarkan prinsip keberlanjutan, termasuk analisis risiko dan peluang ESG.**

## 2. Analisis Field Dataset

**2.1 Technical & Operational Dataset**

Data ini memberikan gambaran mendalam tentang kinerja teknis dan operasional proyek bioenergi.

**📊 Struktur Dataset**

|Nama Field|Deskripsi Singkat|
|-|-
|Project_ID|Kode unik proyek (misal: BIO-GAS-001)|
|Capacity_MW|Kapasitas produksi energi (dalam Megawatt)|
|Operating_Hours_Annually|Jam operasi tahunan (dalam jam)|
|Maintenance_Cost_Ratio|Rasio biaya pemeliharaan terhadap pendapatan (%)|
|Biomass_Source_Reliability|Indeks keandalan pasokan biomassa (skala 0-100)|

**📏 Rumus Lifecycle Carbon Footprint (LCF)**

$$LCF = \sum_{t=1}^{N} (E_{t,produksi} + E_{t,transport} + E_{t,pengelolaan}) - E_{t,penghindaran}$$
 
**Keterangan:**
* ($ LCF $): **Lifecycle Carbon Footprint** (total jejak karbon siklus hidup proyek dalam ton CO₂e).
* ($E_{t,produksi}$): Emisi karbon dari produksi biomassa pada tahun ke-($t$).
* ($E_{t,transport}$): Emisi karbon dari transportasi biomassa pada tahun ke-($t$).
* ($E_{t,pengelolaan}$): Emisi karbon dari pengelolaan limbah/residu pada tahun ke-($t$).
* ($E_{t,penghindaran}$): Emisi karbon yang berhasil dihindari (misalnya dari metana yang tidak lepas ke atmosfer) pada tahun ke-($t$).
* ($N$): Umur proyek (dalam tahun).

**✅ LCF yang lebih rendah menunjukkan proyek lebih efisien dalam mengurangi emisi gas rumah kaca secara keseluruhan.**

Analisis **LCF** dari data `Technical_Operational_Dataset` menunjukkan hasil sebagai berikut:

![statistik_LCF_proyek](https://github.com/user-attachments/assets/607781a2-f598-438c-b131-0d524c20d83d)


**Kesimpulan Hasil:**

- Proyek dengan LCF rendah secara konsisten adalah proyek-proyek yang mengoptimalkan penggunaan biomassa lokal dan memiliki rantai pasok yang efisien.
  
- Dalam visualisasi, mayoritas proyek biogas seperti BIO-GAS-KALTENG-001 dan BIO-GAS-SUMUT-001 menunjukkan LCF yang sangat rendah, menandakan keberhasilan dalam mengelola emisi dari hulu ke hilir.
  
- Beberapa proyek biomassa berskala besar juga menunjukkan kinerja yang baik, namun penting untuk memantau sumber biomassa dan praktik berkelanjutan.

**2.2 Environmental Impact Dataset**

Dataset ini merekam dampak lingkungan yang lebih luas dari proyek bioenergi, melampaui emisi karbon.

**📊 Struktur Dataset**

|Nama Kolom|Deskripsi Singkat|
|-|-
|`Project_ID`|Kode unik proyek|
|`Water_Footprint_Reduction`|Estimasi pengurangan jejak air tahunan (dalam m³)|
|`Waste_Diversion_Rate`|Persentase limbah yang berhasil dialihkan dari TPA (%)|
|`Biodiversity_Impact_Score`|Skor dampak terhadap keanekaragaman hayati (skala -100 hingga 100)|
|`Soil_Health_Improvement`|Indeks peningkatan kesehatan tanah (skala 0-100)|

**📏Rumus Environmental Value Index (EVI)**

$$EVI = w_1 \cdot W + w_2 \cdot D + w_3 \cdot B$$

**Keterangan:**
* ($ EVI $): **Environmental Value Index** (skor nilai lingkungan proyek, 0-100).
* ($W$): Skor normalisasi dari pengurangan jejak air (`Water_Footprint_Reduction`).
* ($D$): Skor normalisasi dari tingkat pengalihan limbah (`Waste_Diversion_Rate`).
* ($B$): Skor normalisasi dari dampak keanekaragaman hayati (`Biodiversity_Impact_Score`).
* ($w_1, w_2, w_3$): Bobot faktor dampak lingkungan (jumlahnya = 1), ditentukan melalui metode pakar.

✅ Nilai EVI yang lebih tinggi menunjukkan kontribusi lingkungan yang lebih signifikan dan holistik per unit proyek.

Analisis EVI dari data `Environmental_Impact_Dataset` menunjukkan hasil sebagai berikut:

![fc2da5d9-b9a3-4511-a1b0-58e2ce862936](https://github.com/user-attachments/assets/ece2d77d-5a09-401b-aa9c-4502c826859a)

**Kesimpulan Hasil:**

Proyek dengan EVI tinggi menunjukkan praktik pengelolaan lingkungan yang komprehensif, tidak hanya berfokus pada emisi tetapi juga air, limbah, dan keanekaragaman hayati.
Proyek yang memanfaatkan limbah pertanian sebagai bahan baku biomassa cenderung memiliki EVI yang sangat baik karena berkontribusi pada pengurangan limbah dan peningkatan kualitas tanah.
Penting untuk memonitor proyek dengan EVI rendah dan mengidentifikasi area yang perlu perbaikan, seperti pengelolaan limbah cair atau dampak terhadap ekosistem lokal.

**2.3 Social Development Dataset**

Dataset ini mengukur dampak proyek terhadap kesejahteraan dan pengembangan masyarakat lokal.

**📊 Struktur Dataset**

|Nama Field|Deskripsi Singkat|
|-|-
|`Local_Employment_Rate_Increase`|Persentase peningkatan lapangan kerja lokal (%)|
|`Community_Income_Impact`|Dampak terhadap pendapatan rumah tangga lokal (dalam Rupiah per tahun)|
|`Skills_Transfer_Index`|Indeks transfer pengetahuan dan keterampilan kepada masyarakat (skala 0-100)|
|`Gender_Equality_Inclusion`|Tingkat inklusi gender dalam proyek dan manfaatnya (skala 0-100)|


**🤝 Rumus Community Well-being Impact (CWI)**

$$CWI = w_1 \cdot E + w_2 \cdot I + w_3 \cdot S + w_4 \cdot G$$

**Keterangan:**
* ($ CWI $): **Community Well-being Impact** (skor dampak kesejahteraan masyarakat, 0-100).
* ($E$): Skor normalisasi dari peningkatan lapangan kerja lokal (`Local_Employment_Rate_Increase`).
* ($I$): Skor normalisasi dari dampak pendapatan komunitas (`Community_Income_Impact`).
* ($S$): Skor normalisasi dari indeks transfer keterampilan (`Skills_Transfer_Index`).
* ($G$): Skor normalisasi dari inklusi gender (`Gender_Equality_Inclusion`).
* ($w_1, w_2, w_3, w_4$): Bobot faktor dampak sosial (jumlahnya = 1), ditentukan melalui survei partisipatif.

**✅ CWI yang lebih tinggi menunjukkan proyek memberikan manfaat sosial yang lebih substansial dan inklusif bagi masyarakat lokal.**

Hasil analisis dari data Social_Development_Dataset menunjukkan hasil sebagai berikut:

![statistik_CWI](https://github.com/user-attachments/assets/e984c5c3-c39c-4543-b870-92f9e7be5b98)

**Kesimpulan Hasil:**

Proyek dengan CWI positif menunjukkan komitmen kuat terhadap pengembangan masyarakat, melampaui sekadar penciptaan lapangan kerja.
Proyek yang melibatkan pelatihan masyarakat dan memberdayakan perempuan dalam operasionalnya cenderung memiliki CWI yang sangat tinggi.
Penting untuk mengidentifikasi proyek dengan CWI rendah dan menyelidiki apakah ada kesenjangan dalam distribusi manfaat atau partisipasi masyarakat.

**2.4 Economic Feasibility Dataset**

Dataset ini memberikan gambaran tentang kelayakan ekonomi makro dan mikro proyek dari sisi finansial.

**📊 Struktur Dataset**

|Nama Field`|Deskripsi Singkat|
|-|-
|`Net_Revenue_Projection`|Proyeksi pendapatan bersih tahunan (dalam Rupiah)|
|`Operational_Cost_Efficiency`|Rasio biaya operasional terhadap pendapatan (%), makin rendah makin baik|
|`Internal_Rate_of_Return_IRR`|Tingkat pengembalian internal proyek (%)|
|`Payback_Period_Years`|Waktu pengembalian modal awal (dalam tahun)|

**📉 Rumus Green Return on Investment (GROI)**

$$GROI = \frac{NPV_{finansial} + NPV_{lingkungan} + NPV_{sosial}}{I_0}$$
​ 

**Keterangan:**
* ($ GROI $): **Green Return on Investment** (rasio pengembalian hijau, tanpa satuan).
* ($NPV_{finansial}$): Net Present Value dari arus kas finansial proyek.
* ($NPV_{lingkungan}$): Net Present Value dari nilai dampak lingkungan yang dimonetisasi.
* ($NPV_{sosial}$): Net Present Value dari nilai dampak sosial yang dimonetisasi.
* ($I_0$): Investasi awal proyek (dalam Rupiah).

**✅ GROI yang lebih tinggi menunjukkan proyek tidak hanya menguntungkan secara finansial, tetapi juga memberikan pengembalian yang signifikan dari dampak lingkungan dan sosial yang dimonetisasi.**

Dari analisis Economic_Feasibility_Dataset menunjukkan hasil sebagai berikut:

![824f1ed4-ede7-4ab2-9adf-514e854db10f](https://github.com/user-attachments/assets/95db57de-6d26-4369-afbe-39d835c69561)


**Kesimpulan Hasil:**

Proyek dengan GROI positif secara konsisten dianggap layak secara finansial, lingkungan, dan sosial.
Proyek bioenergi yang memiliki akses stabil ke bahan baku lokal dan pasar energi bersih cenderung menunjukkan GROI yang tinggi.
Analisis ini membantu mengidentifikasi proyek yang mungkin memerlukan penyesuaian strategi untuk meningkatkan dampak holistiknya.

**2.5 Policy & Regulatory Dataset**

Dataset ini menyajikan data mengenai dukungan kebijakan dan lingkungan regulasi yang relevan dengan proyek bioenergi.

**📊 Struktur Dataset**

|Nama Field|Deskripsi Singkat|
|-|-
|`Policy_Support_Index`|Skor dukungan kebijakan pemerintah (0-100), mencakup insentif dan regulasi.|
|`Regulatory_Compliance_Rate`|Tingkat kepatuhan proyek terhadap regulasi lingkungan dan sosial (%)|
|`Community_Acceptance_Score`|Skor penerimaan masyarakat terhadap proyek (0-100), dari survei publik.|
|`Investment_Incentive_Value`|Estimasi nilai insentif investasi yang diterima proyek (dalam Rupiah).|

📜 Rumus Regulatory and Social Acceptance Index (RSAI)

$$RSAI = w_1 \cdot P + w_2 \cdot C + w_3 \cdot A$$

**Keterangan:**
* ($ RSAI $): **Regulatory and Social Acceptance Index** (skor penerimaan regulasi dan sosial, 0-1).
* ($P$): Skor normalisasi dari dukungan kebijakan (`Policy_Support_Index`).
* ($C$): Skor normalisasi dari tingkat kepatuhan regulasi (`Regulatory_Compliance_Rate`).
* ($A$): Skor normalisasi dari penerimaan masyarakat (`Community_Acceptance_Score`).
* ($w_1, w_2, w_3$): Bobot faktor (jumlahnya = 1), ditentukan berdasarkan prioritas strategis.

**✅ RSAI mendekati 1 → Proyek memiliki dukungan kebijakan dan penerimaan sosial yang kuat → Mengurangi risiko non-finansial.**

Dari analisis data Policy_Regulatory_Dataset menunjukkan hasil sebagai berikut:

![b9177f33-e1db-4129-b5b2-1c12bb7997cd](https://github.com/user-attachments/assets/d04ad35a-3398-4b8f-bb11-c3b2e2d5f733)


**Kesimpulan Hasil:**

Proyek dengan RSAI tinggi menunjukkan lingkungan yang kondusif untuk pengembangan dan keberlanjutan.
Proyek yang secara aktif melibatkan pemangku kepentingan lokal dan selaras dengan kebijakan energi nasional cenderung memiliki RSAI yang optimal.
Analisis ini membantu mengidentifikasi potensi hambatan non-finansial yang dapat mempengaruhi proyek.

# 📌 Kesimpulan

Analisis proyek Green Finance ini menegaskan bahwa keberhasilan proyek bioenergi berkelanjutan merupakan konvergensi dari berbagai dimensi: teknis-operasional, dampak lingkungan, pengembangan sosial, kelayakan ekonomi, serta dukungan kebijakan dan sosial.

**💰 Technical & Operational Dataset menunjukkan bahwa efisiensi operasional dan keandalan pasokan bahan baku sangat krusial untuk kinerja proyek.**

**🌱 Environmental Impact Dataset menekankan pentingnya tidak hanya mitigasi emisi, tetapi juga pengurangan jejak air, pengelolaan limbah, dan konservasi keanekaragaman hayati.**

**🧑‍🤝‍🧑 Social Development Dataset menyoroti dampak transformatif proyek terhadap penciptaan lapangan kerja lokal, peningkatan pendapatan, transfer keterampilan, dan inklusi gender.**

**📈 Economic Feasibility Dataset memberi pandangan penting tentang bagaimana proyek bioenergi dapat menghasilkan pengembalian yang komprehensif, melampaui metrik finansial tradisional.**

**📜 Policy & Regulatory Dataset membantu mengidentifikasi lingkungan yang mendukung atau menghambat proyek, termasuk insentif dan penerimaan masyarakat.**

Dengan mengintegrasikan kelima dimensi ini—teknis-operasional, dampak lingkungan, pengembangan sosial, kelayakan ekonomi, serta kebijakan dan penerimaan publik—pendekatan Green Finance memberikan gambaran yang lebih komprehensif. Ini membantu kita menilai proyek energi berkelanjutan secara lebih adil dan akurat, baik dari segi dampak positif yang dihasilkan maupun risiko yang mungkin dihadapi.

Terima kasih telah menjelajahi repositori ini! Semoga analisis ini menginspirasi kita semua untuk mengambil keputusan yang lebih hijau dan berkeadilan berbasis data. Sampai jumpa di proyek berikutnya, dan tetap semangat, Teman-Teman ETL! 🌿💡
