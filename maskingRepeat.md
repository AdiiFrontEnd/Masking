# Masking Repeat
Adalah Sebuah Properti Untuk Menentukan Sebuah Cetakan Berulan Atau Tidak Berikut Adalah Contohnya

<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/95db6968-0345-479a-a210-333c20153099" />

Berikut Dari AI

# Selanjutnya: `mask-repeat`

Setelah `mask-image` menentukan **gambar apa** yang dipakai, `mask-repeat` menentukan **apakah gambar itu diulang** atau tidak.

## Kenapa penting?

Secara default, mask **diulang** (tile) sampai memenuhi seluruh elemen. Kalau gambar mask lebih kecil dari elemen, hasilnya bentuk berulang-ulang, padahal biasanya kita maunya satu bentuk saja.

## Nilai yang tersedia

| Nilai | Efek |
|---|---|
| `repeat` | Diulang ke kanan dan ke bawah (default) |
| `no-repeat` | Tampil sekali saja |
| `repeat-x` | Diulang horizontal saja |
| `repeat-y` | Diulang vertikal saja |
| `space` | Diulang tanpa terpotong, sisa ruang dibagi sebagai jarak antar gambar |
| `round` | Diulang tanpa terpotong, gambar diperbesar/diperkecil agar pas |

## Contoh

```css
.kotak {
  width: 300px;
  height: 300px;
  background: linear-gradient(red, blue);
  mask-image: url(bintang.png);
  mask-size: 100px;
  mask-repeat: no-repeat;
}
```

Hasilnya: satu bintang berukuran 100px di pojok kiri atas, sisanya tersembunyi.

Coba ganti `no-repeat` dengan `repeat`, `repeat-x`, atau `space`, dan lihat perbedaannya.

## Perbandingan cepat

- `repeat`: bintang memenuhi elemen, bisa terpotong di tepi
- `no-repeat`: satu bintang saja
- `space`: bintang tersusun rapi, tidak ada yang terpotong, ada jarak di antaranya
- `round`: bintang disesuaikan ukurannya supaya pas tanpa jarak

Setelah ini kita bisa lanjut ke `mask-position` (mengatur **posisi** mask) lalu `mask-size` (mengatur **ukuran** mask).

Mau lanjut ke `mask-position`, atau mau coba contoh interaktif dulu untuk `mask-repeat`?
