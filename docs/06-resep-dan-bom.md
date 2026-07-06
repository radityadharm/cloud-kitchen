# 06 — Resep & Bill of Materials (BOM)

Dokumen ini adalah **ringkasan COGS/BOM**. **Resep lengkap berstandar restoran** (gramasi tepat,
sub-resep batch, teknik, suhu & waktu, plating, catatan chef) ada di binder terpisah:

## 📖 Binder Resep Detail → [`docs/resep/`](resep/00-standar-dan-teknik.md)

| File | Isi |
|------|-----|
| [00 — Standar & Teknik](resep/00-standar-dan-teknik.md) | Standar dapur, teknik inti (double-fry, sangrai rempah, dial-in espresso), food safety |
| [01 — Sub-Resep Dasar](resep/01-sub-resep-dasar.md) | Bumbu, batter, breading, sambal, semua saus, nasi, gula aren, base kopi (skala batch) |
| [02 — Ayam Rempah Joglo](resep/02-ayam-rempah-joglo.md) | Kartu resep AR-01…AR-06 |
| [03 — Gochu Korean Chicken](resep/03-gochu-korean-chicken.md) | Kartu resep GC-01…GC-06 |
| [04 — Mangkok Rice Bowl](resep/04-mangkok-rice-bowl.md) | Kartu resep MB-01…MB-06 |
| [05 — Kopi Sore](resep/05-kopi-sore.md) | Kartu resep KS-01…KS-06 + dial-in espresso |

---

## Hubungan Resep ↔ COGS ↔ Harga

```
Sub-resep & kartu resep (docs/resep/)  →  gramasi per porsi
        │
        ▼
data/bom-resep.csv  →  biaya bahan per porsi (menu hero)
        │
        ▼
data/menu-pricing.csv  →  COGS total + harga jual + margin  →  docs/05-menu-dan-pricing.md
```

> **Cara hitung COGS:** jumlahkan (qty bahan × harga per satuan) + biaya packaging. Harga bahan
> acuan ada di [07 — Supply](07-supply-sourcing.md). Semua estimasi — sesuaikan dengan harga riil.

## Ringkasan COGS per Menu

Rincian bahan menu hero ada di [`data/bom-resep.csv`](../data/bom-resep.csv); COGS seluruh menu
di [`data/menu-pricing.csv`](../data/menu-pricing.csv).

| Kode | Menu | COGS | Harga | Resep |
|------|------|------|-------|-------|
| AR-01 | Paket Ayam Rempah Kremes | Rp9.800 | Rp23.000 | [→](resep/02-ayam-rempah-joglo.md#ar-01--paket-ayam-rempah-kremes-hero) |
| AR-02 | Paket Ayam Rempah Komplit (2pc) | Rp13.100 | Rp33.000 | [→](resep/02-ayam-rempah-joglo.md#ar-02--paket-ayam-rempah-komplit-2-pc) |
| AR-03 | Ayam Rempah + Nasi + Es Teh | Rp10.600 | Rp26.000 | [→](resep/02-ayam-rempah-joglo.md#ar-03--ayam-rempah--nasi--es-teh) |
| AR-04 | Nasi Ayam Rempah Sambal Ijo | Rp10.100 | Rp24.000 | [→](resep/02-ayam-rempah-joglo.md#ar-04--nasi-ayam-rempah-sambal-ijo) |
| AR-05 | Ayam Rempah Ala Carte | Rp5.300 | Rp15.000 | [→](resep/02-ayam-rempah-joglo.md#ar-05--ayam-rempah-ala-carte-1-pc-tanpa-nasi) |
| AR-06 | Tahu Tempe Rempah | Rp4.000 | Rp10.000 | [→](resep/02-ayam-rempah-joglo.md#ar-06--tahu-tempe-rempah-side) |
| GC-01 | Rice Box Gochujang | Rp12.800 | Rp30.000 | [→](resep/03-gochu-korean-chicken.md#gc-01--rice-box-gochujang-hero) |
| GC-02 | Rice Box Soy Garlic | Rp12.500 | Rp30.000 | [→](resep/03-gochu-korean-chicken.md#gc-02--rice-box-soy-garlic) |
| GC-03 | Rice Box Cheese | Rp13.500 | Rp32.000 | [→](resep/03-gochu-korean-chicken.md#gc-03--rice-box-cheese) |
| GC-04 | Rice Box Honey Butter | Rp13.000 | Rp31.000 | [→](resep/03-gochu-korean-chicken.md#gc-04--rice-box-honey-butter) |
| GC-05 | Chicken Only Boneless 150g | Rp12.000 | Rp28.000 | [→](resep/03-gochu-korean-chicken.md#gc-05--chicken-only-boneless-150g-saus-pilihan) |
| GC-06 | Korean Wings 5pc | Rp13.200 | Rp30.000 | [→](resep/03-gochu-korean-chicken.md#gc-06--korean-wings-5pc-saus-pilihan) |
| MB-01 | Chicken Katsu Rice Bowl | Rp11.900 | Rp26.000 | [→](resep/04-mangkok-rice-bowl.md#mb-01--chicken-katsu-rice-bowl-hero) |
| MB-02 | Chicken Teriyaki Rice Bowl | Rp11.500 | Rp25.000 | [→](resep/04-mangkok-rice-bowl.md#mb-02--chicken-teriyaki-rice-bowl) |
| MB-03 | Chicken Blackpepper Rice Bowl | Rp11.600 | Rp25.000 | [→](resep/04-mangkok-rice-bowl.md#mb-03--chicken-blackpepper-rice-bowl) |
| MB-04 | Chicken Salted Egg Rice Bowl | Rp12.800 | Rp28.000 | [→](resep/04-mangkok-rice-bowl.md#mb-04--chicken-salted-egg-rice-bowl) |
| MB-05 | Chicken Katsu Curry Rice Bowl | Rp12.500 | Rp28.000 | [→](resep/04-mangkok-rice-bowl.md#mb-05--chicken-katsu-curry-rice-bowl) |
| MB-06 | Chicken Popcorn Rice Bowl | Rp10.600 | Rp23.000 | [→](resep/04-mangkok-rice-bowl.md#mb-06--chicken-popcorn-rice-bowl) |
| KS-01 | Es Kopi Susu Gula Aren | Rp7.000 | Rp18.000 | [→](resep/05-kopi-sore.md#ks-01--es-kopi-susu-gula-aren-hero) |
| KS-02 | Americano | Rp5.000 | Rp15.000 | [→](resep/05-kopi-sore.md#ks-02--americano-panases) |
| KS-03 | Kopi Susu Reguler | Rp6.200 | Rp16.000 | [→](resep/05-kopi-sore.md#ks-03--kopi-susu-reguler) |
| KS-04 | Es Kopi Susu Cokelat | Rp7.800 | Rp20.000 | [→](resep/05-kopi-sore.md#ks-04--es-kopi-susu-cokelat) |
| KS-05 | Cokelat / Matcha Latte | Rp8.500 | Rp21.000 | [→](resep/05-kopi-sore.md#ks-05--cokelat--matcha-latte-non-kopi) |
| KS-06 | Kopi Susu Botol 250ml | Rp10.000 | Rp25.000 | [→](resep/05-kopi-sore.md#ks-06--kopi-susu-botol-250ml) |

## Kontrol Kualitas Resep

- **Timbang bahan** (timbangan digital) agar porsi & COGS konsisten.
- **Standar resep tertulis** (binder `docs/resep/`) ditempel di tiap stasiun.
- **Uji rasa harian** untuk sambal, saus, dan kopi (tiap batch baru) vs sampel standar.
- **Tinjau COGS bulanan** saat harga bahan berubah; sesuaikan porsi/harga bila perlu.
