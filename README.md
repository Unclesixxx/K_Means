# Simpan laporan sebagai file README.md untuk GitHub

laporan_md = """
# 🧠 Tugas Data Mining: K-Means Clustering  
## Studi Kasus: Ekstrovert vs Introvert Personality Traits  

**Nama:** Qomar Tokan  
**NIM:** 23260008  
**Mata Kuliah:** Data Mining  
**Algoritma:** K-Means Clustering  

---

## 1. Latar Belakang  
Dalam dunia psikologi, klasifikasi kepribadian seperti ekstrovert dan introvert penting untuk berbagai keperluan, mulai dari rekrutmen kerja hingga pengembangan diri. Dengan menggunakan algoritma *K-Means Clustering*, kita dapat mengelompokkan individu ke dalam dua kategori tersebut berdasarkan perilaku dan kebiasaan sehari-hari tanpa label awal (*unsupervised learning*).

---

## 2. Dataset  
Dataset yang digunakan berjudul **"Extrovert vs. Introvert Personality Traits Dataset"**, yang merupakan data sintetis dari platform SyncoraAI.  

**Jumlah data:** ±5000 baris  
**Fitur-fitur:**
- `Time_spent_Alone`
- `Stage_fear`
- `Social_event_attendance`
- `Going_outside`
- `Drained_after_socializing`
- `Friends_circle_size`
- `Post_frequency`

Label (hanya untuk evaluasi, tidak dilatih): `Personality`  
> 0 = Extrovert, 1 = Introvert

---

## 3. Metode  
1. **Preprocessing**:  
   - Menghapus kolom label saat training.  
   - Melakukan normalisasi data dengan `StandardScaler`.

2. **Clustering**:  
   - Menggunakan `KMeans(n_clusters=2)` untuk memisahkan data ke dalam dua kelompok.

3. **Evaluasi**:  
   - Hasil clustering dibandingkan dengan label asli untuk mengetahui akurasi.

---

## 4. Hasil

### Confusion Matrix
|                    | Cluster 0 | Cluster 1 |
|--------------------|-----------|-----------|
| **Extrovert**      |   2404    |    193    |
| **Introvert**      |   125     |   2276    |

**Akurasi: 93.64%**

> Clustering berhasil mengelompokkan data dengan sangat baik. Hal ini menunjukkan bahwa fitur-fitur yang digunakan cukup representatif dalam membedakan ekstrovert dan introvert.

---

## 5. Visualisasi  
Ditampilkan dalam bentuk heatmap confusion matrix menggunakan pustaka `seaborn`.

![Confusion Matrix](confusion_matrix.png)

---

## 6. Kesimpulan  
- Algoritma K-Means dapat digunakan untuk mengelompokkan data kepribadian dengan akurasi tinggi.  
- Fitur perilaku sosial sangat relevan untuk mengidentifikasi kecenderungan kepribadian seseorang.  
- Meskipun tanpa label, metode *unsupervised learning* tetap bisa menghasilkan insight yang akurat.

---

## 7. File Terkait
- `Extrovert vs. Introvert Personality Traits Dataset.csv`
- [`hasil_kmeans_personality.csv`](hasil_kmeans_personality.csv)
- `main.ipynb` (notebook Python)
"""

# Simpan sebagai README.md
readme_path = "/mnt/data/README.md"
with open(readme_path, "w", encoding="utf-8") as f:
    f.write(laporan_md)

readme_path
