# Mask Mode

# Selanjutnya: `mask-mode`

`mask-mode` menentukan **bagian mana dari gambar mask yang dibaca**: transparansinya, atau kecerahan warnanya.

## Nilai yang tersedia

| Nilai | Yang dibaca | Efek |
|---|---|---|
| `alpha` | Transparansi | Buram = terlihat, transparan = tersembunyi |
| `luminance` | Kecerahan warna | Putih = terlihat, hitam = tersembunyi |
| `match-source` | Menyesuaikan jenis sumber | Default |

## Apa itu `match-source`?

Ini nilai default. Browser memilih mode sendiri berdasarkan sumber mask:

- Mask berupa **gambar atau gradient** → pakai `alpha`
- Mask berupa **elemen `<mask>` SVG** → pakai `luminance`

Makanya di awal tadi saya bilang gambar biasa memakai alpha secara default.

## Contoh: perbedaan alpha vs luminance

Misalkan mask berupa gradient dari **putih ke hitam** (keduanya sama-sama buram penuh):

```css
.kotak {
  width: 300px;
  height: 300px;
  background: linear-gradient(red, blue);
  mask-image: linear-gradient(to right, white, black);
}
```

Dengan mode default (`alpha`): **seluruh kotak terlihat penuh**, karena putih dan hitam sama-sama buram.

Sekarang ganti mode-nya:

```css
.kotak {
  width: 300px;
  height: 300px;
  background: linear-gradient(red, blue);
  mask-image: linear-gradient(to right, white, black);
  mask-mode: luminance;
}
```

Hasilnya: kotak terlihat di sisi kiri (putih), lalu **memudar hingga hilang** di sisi kanan (hitam).

## Kapan memakai `luminance`?

Saat kamu punya mask berupa gambar **hitam-putih** (misalnya foto grayscale atau gambar tanpa transparansi) dan ingin kecerahannya yang menentukan bentuk.

## Perbandingan dengan `mask-type`

Dari tabel W3Schools tadi:

- `mask-mode`: untuk `mask-image` pada elemen CSS biasa
- `mask-type`: untuk elemen `<mask>` di dalam SVG

Selanjutnya kita bahas `mask-composite`, yaitu cara **menggabungkan beberapa mask** sekaligus. Lanjut?
