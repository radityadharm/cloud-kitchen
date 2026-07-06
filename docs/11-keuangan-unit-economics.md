# 11 — Keuangan & Unit Economics

Sumber data: [`data/proyeksi-keuangan.csv`](../data/proyeksi-keuangan.csv),
[`data/capex-peralatan.csv`](../data/capex-peralatan.csv).

> Semua angka **estimasi** untuk perencanaan. Validasi dengan biaya riil sebelum eksekusi.

## 1. Modal Awal (CAPEX)

| Komponen | Nilai |
|----------|-------|
| Peralatan | Rp69.600.000 |
| Renovasi & instalasi | Rp40.000.000 |
| Deposit + sewa dimuka | Rp15.000.000 |
| Perizinan | Rp8.000.000 |
| Branding + fotografi | Rp10.000.000 |
| Onboarding + marketing awal | Rp10.000.000 |
| Modal kerja awal | Rp40.000.000 |
| Kontingensi | Rp20.000.000 |
| **TOTAL CAPEX** | **±Rp212.600.000** |

Rincian: [09 — Peralatan & CAPEX](09-peralatan-capex.md).

## 2. Biaya Tetap Bulanan (OPEX)

| Komponen | Nilai/bulan |
|----------|-------------|
| Sewa ruko/kios | Rp3.500.000 |
| Gaji tim (6 orang) | Rp15.000.000 |
| Listrik + gas + air | Rp4.000.000 |
| Internet | Rp500.000 |
| Marketing / iklan platform | Rp3.000.000 |
| Maintenance & lain-lain | Rp1.500.000 |
| Fee software/POS | Rp500.000 |
| **TOTAL OPEX TETAP** | **Rp28.000.000/bulan** |

> **Di luar** OPEX tetap ada 2 biaya **variabel** (mengikuti penjualan): **COGS bahan ±40%**
> dan **komisi platform ±22%** dari penjualan.

## 3. Unit Economics (per Order)

Asumsi **AOV (nilai rata-rata order) = Rp35.000** (karena order sering multi-item + minuman):

| Komponen | % | Nilai per order |
|----------|---|-----------------|
| Penjualan (AOV) | 100% | Rp35.000 |
| (–) COGS bahan | 40% | Rp14.000 |
| (–) Komisi platform | 22% | Rp7.700 |
| **= Kontribusi per order** | **38%** | **Rp13.300** |

Rp13.300 inilah yang tersedia menutup OPEX tetap & jadi laba.

## 4. Titik Impas (BEP)

$$\text{BEP order/bulan} = \frac{\text{OPEX tetap}}{\text{kontribusi per order}} = \frac{28.000.000}{13.300} \approx 2.105 \text{ order/bulan}$$

**≈ 70 order/hari** (2.105 ÷ 30). Di bawah ini rugi operasional; di atas ini mulai untung.

## 5. Proyeksi Laba-Rugi 12 Bulan (Skenario Lean)

Asumsi: order/hari naik bertahap (ramp-up), AOV Rp35.000, COGS 40%, komisi 22%, OPEX tetap
Rp28 juta. Angka penuh di [`data/proyeksi-keuangan.csv`](../data/proyeksi-keuangan.csv).

| Bulan | Order/hari | Revenue | Laba Bersih | Laba Kumulatif |
|-------|-----------|---------|-------------|----------------|
| 1 | 40 | Rp42,0 jt | **–Rp12,0 jt** | –Rp12,0 jt |
| 2 | 55 | Rp57,8 jt | –Rp6,1 jt | –Rp18,1 jt |
| 3 | 70 | Rp73,5 jt | ±Rp0 (BEP) | –Rp18,2 jt |
| 4 | 85 | Rp89,3 jt | +Rp5,9 jt | –Rp12,3 jt |
| 5 | 95 | Rp99,8 jt | +Rp9,9 jt | –Rp2,3 jt |
| 6 | 105 | Rp110,3 jt | +Rp13,9 jt | +Rp11,6 jt |
| 7 | 110 | Rp115,5 jt | +Rp15,9 jt | +Rp27,4 jt |
| 8 | 115 | Rp120,8 jt | +Rp17,9 jt | +Rp45,3 jt |
| 9 | 120 | Rp126,0 jt | +Rp19,9 jt | +Rp65,2 jt |
| 10 | 125 | Rp131,3 jt | +Rp21,9 jt | +Rp87,1 jt |
| 11 | 130 | Rp136,5 jt | +Rp23,9 jt | +Rp111,0 jt |
| 12 | 130 | Rp136,5 jt | +Rp23,9 jt | +Rp134,8 jt |

**Catatan pembacaan:**
- **BEP operasional** tercapai sekitar **bulan ke-3** (±70 order/hari).
- **Laba kumulatif operasional** jadi positif sekitar **bulan ke-6**.
- **Balik modal (payback CAPEX Rp212,6 jt):** laba operasi tahun 1 ≈ Rp134,8 juta; sisa
  ±Rp77,8 juta tertutup di tahun ke-2 (laba ±Rp23,9 jt/bln) → **payback ±16 bulan**. Wajar untuk F&B.

## 6. Skenario Sensitivitas

| Skenario | Perubahan | Dampak |
|----------|-----------|--------|
| Konservatif | Ramp lebih lambat / AOV Rp30rb | BEP mundur ke bulan 4–5, payback ±24 bln |
| Optimis | Dorong order langsung (komisi turun) & AOV Rp40rb | Kontribusi/order naik ke ±Rp16–18rb, payback ±12–14 bln |
| Biaya bahan naik | Cabai/ayam naik → COGS 45% | Kontribusi turun; sesuaikan porsi/harga |

## 7. Pengungkit Keuntungan (Levers)

1. **Naikkan AOV** — bundling makanan + Kopi Sore (minuman margin 60%+).
2. **Kurangi komisi** — arahkan pelanggan ke order langsung (WhatsApp) via stiker & loyalti.
3. **Jaga COGS** — timbang porsi, kontrol waste (<5%), negosiasi supplier.
4. **Optimalkan volume** — rating tinggi + foto bagus + kecepatan → peringkat aplikasi naik.
5. **Efisiensi SDM** — owner merangkap admin di fase awal menghemat ±Rp2,5 jt/bulan.
