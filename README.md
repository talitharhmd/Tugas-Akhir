# Tugas Akhir — Analisis Topik dan Clustering Berbasis LDA & Word Embedding

## Deskripsi Penelitian
Repository ini berisi seluruh source code, notebook eksperimen, hasil clustering, dan file evaluasi yang digunakan dalam penelitian tugas akhir.

Penelitian ini berfokus pada analisis topik dan clustering dokumen teks menggunakan pendekatan:

- **Latent Dirichlet Allocation (LDA)**
- **Word Embedding**
  - Word2Vec
  - FastText
  - Fast2Vec
- **Dimensionality Reduction**
  - PCA
  - UMAP
- **Clustering**
  - K-Means

Penelitian membandingkan tiga skenario utama:

1. **LDA Only**  
   Clustering langsung menggunakan distribusi probabilitas topik dari LDA.

2. **Embedding Only**  
   Clustering menggunakan representasi word embedding.

3. **LDA + Embedding (Hybrid)**  
   Clustering menggunakan fitur gabungan LDA dan word embedding.

---

# Workflow Penelitian

1. Preprocessing data  
2. Pemodelan LDA  
3. Ekstraksi fitur embedding  
4. Reduksi dimensi (PCA / UMAP)  
5. Clustering menggunakan K-Means  
6. Evaluasi hasil clustering  
7. Analisis cluster dan interpretasi topik  

---

# Struktur Repository

```bash
Tugas-Akhir/
│
├── preprocessing/
│   └── preprocessing.ipynb
│
├── lda/
│   ├── lda_modeling.ipynb
│   └── lda_outputs/
│
├── clustering/
│   ├── lda_only/
│   ├── embedding_only/
│   └── lda_embedding/
│
├── hasil/
│   ├── lda_only/
│   ├── embedding_only/
│   └── lda_embedding/
│
├── dataset/
│
└── README.md
```

---

# Penjelasan Folder

## preprocessing/
Berisi notebook untuk preprocessing data, meliputi:

- cleaning
- case folding
- tokenizing
- slang replacement
- stopword removal
- stemming / lemmatization

---

## lda/
Berisi proses pembangunan model LDA:

- training model
- evaluasi coherence score
- pemilihan jumlah topik terbaik
- distribusi topik

---

## clustering/
Berisi notebook untuk seluruh eksperimen clustering.

### lda_only/
Clustering langsung dari distribusi topik LDA.

### embedding_only/
Clustering dari fitur word embedding.

### lda_embedding/
Clustering dari fitur gabungan LDA dan embedding.

---

## hasil/
Berisi seluruh hasil eksperimen.

Hasil dibagi berdasarkan skenario eksperimen:

- lda_only
- embedding_only
- lda_embedding

Setiap folder dapat berisi:

- cluster results
- visualisasi
- evaluasi clustering
- summary results

---

# Dimensi Embedding yang Digunakan

Eksperimen embedding dilakukan pada beberapa dimensi:

- 100 Dimensions
- 200 Dimensions
- 300 Dimensions

---

# Metode Evaluasi

Evaluasi clustering dilakukan menggunakan:

- Silhouette Score
- Davies-Bouldin Index (DBI)
- Elbow Method / Inertia
- Coherence Score
- c-TF-IDF Analysis

---

# Tools dan Library

Penelitian ini menggunakan:

- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- Gensim
- UMAP
- Matplotlib
- Seaborn
- Plotly

---

# Catatan

Repository ini disusun untuk dokumentasi penelitian tugas akhir secara terstruktur agar memudahkan proses evaluasi, revisi, dan reproduksi eksperimen.
