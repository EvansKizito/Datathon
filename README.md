## Competition & Project Overview

### Datathon 2025 @ Fasilkom UI
- **Tema:** AI-Powered Business Insight & Action  
- **Penyelenggara:** RISTEK FASILKOM Universitas Indonesia  
- **Kolaborasi:** Investor Daily, BeritaSatu, JakartaGlobe.id, BTV, B Universe  

**Highlight Kompetisi**  
1. **Goal:** Ubah data mentah jadi insight bisnis yang **actionable**.  
2. **Pendekatan:** Pipeline end-to-end berbasis CRISP-DM (Business Understanding → Data Understanding → Data Preparation → Modeling → Evaluation → Deployment).  
3. **Output:**  
   - Prototype (notebook/app) dengan demo Isolation Forest, Chain Ladder & Bornhuetter–Ferguson.  
   - Laporan riset format NeurIPS (≤ 12 halaman).  
   - Pitch deck 10–12 slide.

---

### Project: “Penerapan Isolation Forest untuk Verifikasi Cadangan Klaim”  
**Judul Lengkap:**  
> *Penerapan Isolation Forest untuk Verifikasi Cadangan Klaim: Studi Banding terhadap Chain Ladder dan Bornhuetter–Ferguson*

**Metodologi & Struktur Laporan**  
1. **Abstrak**  
   - Ringkas tujuan riset, metodologi, hasil utama (penurunan error cadangan).  
2. **Pendahuluan**  
   - Latar: rendahnya literasi asuransi & risiko anomali reserve.  
   - Tujuan: verifikasi cadangan klaim via ML (IF) vs metode tradisional.  
3. **Kajian Teori & Data**  
   - Chain Ladder & Bornhuetter–Ferguson (CL/BF).  
   - Prinsip Isolation Forest (unsupervised anomaly detection).  
   - Deskripsi dataset synthetic: paid & incurred triangle, reported year, exposure, LOB, anomali 2%.  
4. **Solusi Usulan**  
   - **Data Preparation:** normalisasi, feature engineering, reported year.  
   - **Modeling:**  
     - Chain Ladder (faktor development & proyeksi ultimate).  
     - Bornhuetter–Ferguson (expected loss ratio + pattern development).  
     - Isolation Forest (flag & filter anomali).  
   - **Integrasi:**  
     - Skenario 0: CL/BF baseline.  
     - Skenario 1: Drop titik anomali—hitung ulang CL/BF.  
     - Skenario 2: Down-weight anomali dalam CL/BF.  
5. **Hasil Eksperimen & Pengujian**  
   - Metrik: MAPE, RMSE, MARE, over/under-reserving ratio.  
   - Heatmap segitiga sebelum/sesudah filter anomali.  
   - Grafik perbandingan estimasi ultimate.  
6. **Analisis Hasil**  
   - Dampak filter anomali pada akurasi cadangan.  
   - Business insight: early warning, optimasi capital charge, compliance audit.  
7. **Kesimpulan & Saran**  
   - Rangkuman temuan & rekomendasi implementasi real-time dashboard.  
   - Saran robustness check (Mack, Bootstrap CL) dan perluasan dataset.

---

### Ringkasan Metode Utama

| Metode                             | Fungsi                                                                                     |
|------------------------------------|--------------------------------------------------------------------------------------------|
| **Isolation Forest**               | Deteksi anomali pada incremental paid & incurred, flag data kacau → verifikasi reserve.    |
| **Chain Ladder**                   | Proyeksi ultimate reserve berdasarkan faktor development segitiga klaim kumulatif.         |
| **Bornhuetter–Ferguson**           | Kombinasi expected loss ratio & development pattern untuk estimasi reserve yang stabil.    |
| **CRISP-DM**                       | Kerangka sistematis: dari business understanding hingga deployment insight.               |
