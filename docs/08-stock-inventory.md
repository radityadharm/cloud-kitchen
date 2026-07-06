# 08 — Stock & Inventory Management

Sumber data: [`data/stock-par-level.csv`](../data/stock-par-level.csv).

## Konsep Par Level

**Par level** = jumlah stok minimum & maksimum yang harus dijaga untuk tiap bahan:
- **Par min** — batas bawah; begitu stok menyentuh ini, lakukan order ulang.
- **Par max** — batas atas; jangan stok berlebih (hindari basi & modal tertahan).

Par level dihitung dari: **rata-rata pemakaian harian × lead time + buffer**. Saat order
naik, par level dinaikkan. Contoh lengkap ada di CSV; ringkasan:

| Bahan | Par Min | Par Max | Simpan | Cek |
|-------|---------|---------|--------|-----|
| Ayam karkas | 15 kg | 30 kg | Freezer/Chiller | Harian |
| Ayam fillet | 12 kg | 25 kg | Freezer/Chiller | Harian |
| Beras | 50 kg | 100 kg | Kering | Mingguan |
| Minyak goreng | 36 L | 72 L | Kering | Mingguan |
| Cabai | 4 kg | 8 kg | Chiller | Harian |
| Susu UHT | 24 L | 48 L | Chiller | Mingguan |
| Biji kopi | 4 kg | 8 kg | Kedap udara | 2x/bulan |
| Packaging (box/bowl/cup) | 1.000 pcs | 3.000 pcs | Kering | Bulanan |

## Klasifikasi Bahan berdasarkan Frekuensi

- **Harian (bahan segar cepat rusak):** ayam, cabai, bawang, sayur — beli sesuai proyeksi
  order esok hari, minim stok agar segar.
- **Mingguan (semi-tahan lama):** beras, minyak, tepung, susu, saus olahan.
- **Bulanan (tahan lama):** packaging, bumbu kering, gula aren, cokelat/matcha bubuk.

## Sistem Penyimpanan (Storage)

1. **Freezer** — stok ayam beku cadangan.
2. **Chiller/Kulkas** — ayam siap masak (thawed), sayur, dairy, saus yang sudah dibuka.
3. **Rak kering** — beras, tepung, minyak, packaging, bumbu kering.
4. **Area bar** — biji kopi (kedap udara), susu (chiller bar), gula aren.
5. Pisahkan **bahan mentah** dan **bahan siap saji**; pisahkan area kopi dari area gorengan.

## FIFO (First In, First Out)

- Bahan yang **datang lebih dulu dipakai lebih dulu**.
- Beri **label tanggal terima** pada setiap batch.
- Tata stok lama di depan, stok baru di belakang.

## Kontrol Waste (Susut)

- **Prep sesuai proyeksi** order harian, jangan over-prep bahan cepat basi (sambal, nasi, saus fresh).
- **Pantau menu paling laku** vs lambat; kurangi prep menu lambat.
- **Manfaatkan bahan bersama** — sisa ayam fillet bisa dipakai lintas Gochu & Mangkok.
- **Catat waste harian** (berapa & kenapa) untuk perbaikan.
- Target **waste < 3–5%** dari nilai bahan.

## Alur Stok Opname

- **Harian:** cek cepat bahan segar & packaging (menjelang tutup) → tentukan order esok.
- **Mingguan:** hitung stok semi-tahan lama, cocokkan dengan pemakaian & penjualan.
- **Bulanan:** stok opname penuh + rekonsiliasi COGS aktual vs proyeksi (dari
  [11 — Keuangan](11-keuangan-unit-economics.md)).
- Gunakan **kartu stok sederhana / spreadsheet** (atau fitur inventory di POS) untuk mencatat
  masuk-keluar tiap bahan.
