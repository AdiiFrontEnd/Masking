# Mask Side 
Adalah Sebuah Properti Untuk menentukan Ukuran Stensil Atau cetakan Pada Image


# Selanjutnya: `mask-size`

`mask-size` menentukan **ukuran gambar mask** di dalam elemen. Tanpa properti ini, mask tampil dengan ukuran aslinya (misalnya PNG 500px akan tampil 500px).

## Nilai yang tersedia

**1. `auto`** (default): memakai ukuran asli gambar.

**2. `contain`**: gambar diperbesar/diperkecil sampai **seluruhnya muat** di elemen, proporsi tetap terjaga. Bisa ada sisa ruang kosong.

**3. `cover`**: gambar diperbesar/diperkecil sampai **menutupi seluruh elemen**, proporsi tetap terjaga. Bagian gambar bisa terpotong.

**4. Satuan panjang**: lebar lalu tinggi.

```css
mask-size: 100px 50px;  /* lebar 100px, tinggi 50px */
mask-size: 100px;       /* lebar 100px, tinggi otomatis */
```

**5. Persentase**: relatif terhadap ukuran elemen.

```css
mask-size: 50% 50%;  /* setengah lebar dan setengah tinggi elemen */
```

## Contoh

```css
.kotak {
  width: 300px;
  height: 300px;
  background: linear-gradient(red, blue);
  mask-image: url(bintang.png);
  mask-repeat: no-repeat;
  mask-position: center;
  mask-size: contain;
}
```

Hasilnya: bintang diperbesar/diperkecil agar pas di dalam kotak 300px, tepat di tengah.

## `contain` vs `cover`

| Nilai | Perilaku | Cocok untuk |
|---|---|---|
| `contain` | Seluruh mask terlihat, mungkin ada ruang sisa | Bentuk (bintang, logo) yang harus utuh |
| `cover` | Elemen tertutup penuh, mask mungkin terpotong | Mask berupa tekstur atau pola |

## Kombinasi yang sering dipakai

Tiga properti yang sudah kita bahas biasanya ditulis bersama:

```css
mask-image: url(bintang.png);
mask-repeat: no-repeat;
mask-position: center;
mask-size: contain;
```

Atau dalam shorthand:

```css
mask: url(bintang.png) center / contain no-repeat;
```

Perhatikan tanda `/` yang memisahkan **position** dan **size**.

Selanjutnya kita bahas `mask-mode` (alpha vs luminance), lalu `mask-composite`. Lanjut?
