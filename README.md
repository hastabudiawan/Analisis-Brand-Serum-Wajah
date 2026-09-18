---
title: "Analisis Brand Serum Wajah"
slug: "analisis-serum-wajah"
tech: ["Python", "Pandas", "Matplotlib", "Power BI"]
image: "/images/projects/serum.png"
demoUrl: ""
repoUrl: ""
date: "2025-09"
overview: "Memetakan lanskap kompetisi kategori Serum Wajah di Shopee untuk brand skincare lokal yang berencana ekspansi lini produk."
---

## Business Understanding

**Tujuan:** Analisis ini disusun dari sudut pandang *growth strategy consultant* yang diminta oleh sebuah brand skincare lokal (sudah punya lini produk, berencana ekspansi ke lini serum) untuk memetakan lanskap kompetisi kategori **Serum Wajah**.

**Permasalahan:** Sebelum menyusun strategi masuk/ekspansi, brand butuh pemahaman soal siapa pemain dominan saat ini, bagaimana pola distribusi penjualan mereka (official store vs reseller), positioning harga, serta wilayah dengan permintaan tertinggi.

**Key Questions:**
1. Siapa brand dominan di kategori Serum Wajah dan seberapa besar kontribusi penjualannya?
2. Apakah dominasi penjualan brand-brand tersebut berasal dari *official store* atau *reseller/toko pihak ketiga*?
3. Produk apa yang jadi *hero product* kontributor utama volume maupun revenue?
4. Bagaimana positioning harga rata-rata (*average selling price*) brand-brand top main di segmen value atau premium?
5. Wilayah mana yang jadi pusat permintaan tertinggi?
6. Rekomendasi strategi apa yang relevan untuk brand yang mau bersaing di kategori ini?

## What Happened (Descriptive Analytics)

Dataset berisi **3.692 listing produk** dari **529 brand unik** kategori Serum Wajah di Shopee, dengan total **623.000 unit terjual** senilai **Rp91 miliar** revenue.

![Dashboard Analisis Serum Wajah](/images/projects/serum-dashboard.png)

**Top 5 brand berdasarkan volume penjualan:**
| Brand | Total Unit Terjual |
|---|---|
| Scarlett | 124.000 |
| Somethinc | 65.000 |
| Bening'S | 46.000 |
| Garnier | 38.000 |
| Wardah | 28.000 |

Top 3 brand (Scarlett, Somethinc, Bening'S) menguasai **38% dari total volume penjualan** kategori pasar cukup terkonsentrasi di segelintir pemain besar, meski ada 529 brand yang bersaing.

**Hero product** (kontributor volume tertinggi per SKU):
1. Bening's Diamond Serum / Super Whitening 20.805 unit
2. Scarlett Whitening Acne Serum 20.307 unit
3. Bening's Skin Regeneration Serum (Scar/Bopeng) 20.231 unit

**Pusat permintaan** terkonsentrasi di Jakarta: Jakarta Barat (200K unit) dan Jakarta Utara (136K unit) jadi dua wilayah teratas, jauh di atas Jakarta Selatan, Jambi, dan Tangerang.

**100% listing di dataset ini berasal dari Official Store** tidak ada satu pun data reseller/toko pihak ketiga yang ter-capture selama proses pengumpulan data.

## Why Did It Happen (Diagnostic Analytics)

**Price positioning** brand-brand top menunjukkan dua strategi harga yang berbeda (dilihat dari sebaran *Avg Selling Price* vs volume di scatter plot):

Scarlett bermain di **harga rata-rata jauh lebih tinggi** dibanding brand lain, namun tetap unggul telak di volume penjualan mengindikasikan kekuatan *brand equity* yang kuat, bukan bersaing lewat harga murah. Sebaliknya, sebagian besar brand lain (termasuk yang volume-nya lebih rendah) justru bermain di rentang harga jauh lebih terjangkau.

> **Insight utama:** Volume penjualan tinggi tidak selalu berasal dari harga rendah Scarlett membuktikan brand dengan positioning premium tetap bisa dominan di volume kalau brand equity-nya kuat.

**Soal komposisi official store vs reseller** yang jadi salah satu Key Question di awal: pertanyaan ini **tidak bisa divalidasi** dengan data yang tersedia, karena kolom Seller Type di dataset cuma punya satu nilai (`Official Store`) di seluruh 3.692 baris gak ada listing reseller yang tercapture sama sekali. Ini dicatat sebagai limitasi data, bukan diabaikan.

## What's Next (Prescriptive Analytics)

Rekomendasi untuk brand yang mau ekspansi ke kategori ini:

1. **Tentukan positioning harga secara sadar** - bersaing di segmen volume/harga terjangkau atau di segmen premium dengan brand equity kuat (mengikuti pola Scarlett)  bukan di tengah-tengah tanpa arah jelas.
2. **Fokuskan alokasi budget marketing awal ke Jakarta** (Barat dan Utara khususnya) sebagai wilayah dengan permintaan tertinggi, sebelum ekspansi ke wilayah sekunder.
3. **Pelajari karakteristik hero product** dari brand top (klaim manfaat, format kemasan) sebagai referensi pengembangan produk unggulan sendiri, karena 1-2 SKU sering jadi kontributor mayoritas volume sebuah brand.
4. **Untuk riset lanjutan**, lengkapi metode pengumpulan data agar mencakup listing reseller/toko pihak ketiga, supaya perbandingan pola distribusi official store vs reseller bisa benar-benar dijawab.

## Resources
- [Notebook (Google Colab)](https://colab.research.google.com/drive/1VIPNq5pLVpSOLwBK-_MTzUA4-hldE2i4?usp=sharing)
- [Data bersih hasil ekspor (Google Sheets)](https://docs.google.com/spreadsheets/d/1GB6l7ucp380zIryphEdLFaHzkyIqvzNJDtgrEBa6zvI/edit?usp=sharing)
- [Download Dashboard Power BI](https://drive.google.com/file/d/1Fn2Jq_u55H0RkacGTHyttxQTP7ncCm_M/view?usp=drive_link)
