# 06 — Resep & Bill of Materials (BOM)

Dokumen ini berisi resep operasional tiap menu + rincian bahan per porsi. Rincian bahan
(BOM) contoh menu hero ada di [`data/bom-resep.csv`](../data/bom-resep.csv); COGS setiap
menu dirangkum di [`data/menu-pricing.csv`](../data/menu-pricing.csv).

> **Cara hitung COGS:** jumlahkan (qty bahan × harga per satuan) + biaya packaging.
> Harga bahan acuan ada di [07 — Supply](07-supply-sourcing.md). Semua estimasi — sesuaikan
> dengan harga beli riil.

---

## Bahan Dasar Bersama (Base Prep)

Disiapkan sekali, dipakai lintas menu/brand:

- **Nasi:** beras dicuci, dimasak di rice cooker besar. ±130 g beras → 1 porsi nasi (±Rp2.000).
- **Ayam ungkep rempah (Joglo):** karkas diungkep bumbu halus (bawang putih, bawang merah,
  ketumbar, kunyit, lengkuas, kemiri, garam) 20–30 menit, tiriskan, siap goreng.
- **Ayam fillet marinasi (Gochu & Mangkok):** fillet dipotong, dibumbui dasar (garam,
  bawang putih, lada), disimpan chiller.
- **Adonan kremes:** tepung + air + bumbu, disendokkan ke minyak panas → renyah.
- **Batter & breadcrumb:** untuk boneless Gochu & katsu Mangkok.
- **Saus-saus:** gochujang, soy garlic, cheese, honey butter, teriyaki, blackpepper, katsu,
  salted egg — sebagian premix/jadi, sebagian diracik (lihat catatan tiap resep).
- **Gula aren cair & espresso base:** untuk Kopi Sore.

---

## Ayam Rempah Joglo

### AR-01 — Paket Ayam Rempah Kremes (hero) · COGS Rp9.800 · Jual Rp23.000
**Resep:** Ambil 1 potong ayam ungkep rempah → goreng hingga matang keemasan → tiriskan.
Siram/taburi kremes. Sajikan dengan nasi, sambal (pilihan), dan lalapan.
**BOM per porsi** (lihat CSV): ayam karkas 97 g, bumbu rempah, tepung bumbu, minyak, kremes,
nasi, sambal, lalapan + packaging.

### AR-02 — Paket Komplit (2 pc) · COGS Rp13.100 · Rp33.000
Sama seperti AR-01, porsi ayam 2 potong. Bahan ayam & kremes ×2, nasi & sambal tetap 1 porsi besar.

### AR-03 — Ayam Rempah + Nasi + Es Teh · COGS Rp10.600 · Rp26.000
AR-01 tanpa lalapan + tambahan es teh manis (COGS es teh ±Rp1.500 termasuk cup).

### AR-04 — Nasi Ayam Rempah Sambal Ijo · COGS Rp10.100 · Rp24.000
AR-01 dengan sambal ijo (cabai hijau, bawang, tomat hijau) menggantikan sambal bawang.

### AR-05 — Ala Carte (1 pc, tanpa nasi) · COGS Rp5.300 · Rp15.000
Hanya ayam rempah + kremes + sambal kecil, tanpa nasi.

### AR-06 — Tahu Tempe Rempah · COGS Rp4.000 · Rp10.000
Tahu & tempe diungkep bumbu rempah lalu digoreng; side dish/hemat.

---

## Gochu Korean Chicken

### GC-01 — Rice Box Gochujang (hero) · COGS Rp12.800 · Rp30.000
**Resep:** Fillet dipotong dadu → celup batter → balur breadcrumb → *double fry* renyah →
lumuri saus gochujang (gochujang, bawang putih, madu, wijen) → letakkan di atas nasi,
taburi wijen & nori. **BOM per porsi** (lihat CSV): fillet 100 g, batter+breadcrumb, minyak,
saus gochujang, nasi, garnish + packaging.

### GC-02 — Rice Box Soy Garlic · COGS Rp12.500 · Rp30.000
Sama, saus soy garlic (kecap asin, bawang putih, madu, mentega).

### GC-03 — Rice Box Cheese · COGS Rp13.500 · Rp32.000
Sama, saus/bubuk keju leleh (biaya keju lebih tinggi).

### GC-04 — Rice Box Honey Butter · COGS Rp13.000 · Rp31.000
Sama, saus honey butter (madu + mentega).

### GC-05 — Chicken Only Boneless 150g · COGS Rp12.000 · Rp28.000
Boneless goreng 150 g + saus pilihan, tanpa nasi (porsi ayam lebih banyak).

### GC-06 — Korean Wings 5pc · COGS Rp13.200 · Rp30.000
5 sayap ayam (bagian sayap) digoreng + saus pilihan.

---

## Mangkok Rice Bowl

### MB-01 — Chicken Katsu Rice Bowl (hero) · COGS Rp11.900 · Rp26.000
**Resep:** Fillet dipipihkan → celup telur → balur breadcrumb → goreng → iris → tata di atas
nasi → siram saus katsu → beri sayur pelengkap. **BOM per porsi** (lihat CSV): fillet 85 g,
tepung+breadcrumb, telur, minyak, nasi, saus katsu, sayur + packaging.

### MB-02 — Chicken Teriyaki · COGS Rp11.500 · Rp25.000
Ayam dipotong, ditumis/goreng, disiram saus teriyaki, di atas nasi.

### MB-03 — Chicken Blackpepper · COGS Rp11.600 · Rp25.000
Ayam + saus blackpepper (lada hitam, bawang bombay, saus tiram).

### MB-04 — Chicken Salted Egg · COGS Rp12.800 · Rp28.000
Ayam popcorn/katsu disiram saus salted egg (telur asin, mentega, daun kari) — premium.

### MB-05 — Chicken Katsu Curry · COGS Rp12.500 · Rp28.000
Katsu (MB-01) disiram saus kari Jepang.

### MB-06 — Chicken Popcorn · COGS Rp10.600 · Rp23.000
Potongan ayam kecil (popcorn) digoreng + saus pilihan; paling hemat.

---

## Kopi Sore

### KS-01 — Es Kopi Susu Gula Aren (hero) · COGS Rp7.000 · Rp18.000
**Resep:** Tarik 1 shot espresso (±16 g biji) → tuang gula aren cair → susu full cream →
es batu → sajikan di cup 16 oz. **BOM per porsi** (lihat CSV): biji kopi 16 g, susu 100 ml,
gula aren 25 ml, es + cup set.

### KS-02 — Americano · COGS Rp5.000 · Rp15.000
Espresso + air (panas/es). COGS terendah, margin tertinggi.

### KS-03 — Kopi Susu Reguler · COGS Rp6.200 · Rp16.000
Espresso + susu + sedikit gula, tanpa gula aren premium.

### KS-04 — Es Kopi Susu Cokelat · COGS Rp7.800 · Rp20.000
KS-01 + bubuk/sirup cokelat.

### KS-05 — Cokelat / Matcha Latte (non-kopi) · COGS Rp8.500 · Rp21.000
Bubuk cokelat atau matcha + susu, tanpa espresso.

### KS-06 — Kopi Susu Botol 250ml · COGS Rp10.000 · Rp25.000
Versi botol *grab & go*, porsi lebih besar + botol.

---

## Kontrol Kualitas Resep

- **Timbang bahan** (gunakan timbangan digital) agar porsi & COGS konsisten.
- **Standar resep tertulis** ditempel di tiap stasiun.
- **Uji rasa harian** untuk sambal, saus, dan kopi (batch baru).
- **Tinjau COGS bulanan** saat harga bahan berubah; sesuaikan porsi/harga bila perlu.
