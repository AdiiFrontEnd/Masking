# Mask Image
Mask Image adalah Sebuah Properti Untuk Menentukan Stensil Apa Yang berformat Img Apa Yang Akan Digunakan Untuk Masking

Berikut Dari AI

# Apa Itu `mask-image`?

`mask-image` adalah properti CSS yang menentukan **gambar apa yang dipakai sebagai mask** (stensil) untuk sebuah elemen.

## Definisi sederhana

Properti ini memberi tahu browser: "Pakai gambar ini untuk menentukan bagian mana dari elemen yang boleh terlihat."

Yang dibaca browser dari gambar mask adalah **transparansinya** (alpha channel), bukan warnanya:

| Area pada gambar mask | Efek pada elemen |
|---|---|
| Buram penuh | Elemen terlihat penuh |
| Semi-transparan | Elemen terlihat samar |
| Transparan | Elemen tersembunyi |

## Jenis nilai yang bisa dipakai

**1. File gambar** (PNG, SVG, dll.)

```css
mask-image: url(bintang.png);
```

**2. Gradient**

```css
mask-image: linear-gradient(to bottom, black, transparent);
```

**3. Tanpa mask** (default)

```css
mask-image: none;
```

**4. Beberapa mask sekaligus**, dipisah koma:

```css
mask-image: url(a.png), linear-gradient(black, transparent);
```

## Contoh visual dalam pikiran

Bayangkan sebuah foto pemandangan, lalu kamu beri `mask-image` berupa PNG lingkaran:

- Bagian foto yang tepat di bawah lingkaran → **terlihat**
- Bagian foto di luar lingkaran → **hilang**

Hasilnya foto tampak berbentuk lingkaran.

## Satu hal yang sering membingungkan

Warna pada gambar mask **tidak penting** (dalam mode default `alpha`). Gradient `black → transparent` dan `red → transparent` hasilnya **sama persis**, karena yang dibaca hanya tingkat transparansinya.

## Ringkasnya

`mask-image` = "gambar stensil" yang menentukan bentuk dan tingkat kejelasan elemen.

Sudah jelas sampai sini? Kalau ya, kita bisa lanjut praktik langsung dengan contoh interaktif, atau lanjut ke `mask-repeat`.


Dan Apa Itu Stensil

# Apa Itu Stensil?

**Stensil** adalah lembaran tipis (kertas, plastik, atau logam) yang **dilubangi membentuk pola tertentu**. Lembaran ini dipakai sebagai cetakan untuk membuat gambar atau huruf yang sama berulang kali.

## Cara kerjanya

1. Kamu punya selembar karton yang sudah dilubangi berbentuk bintang.
2. Karton itu ditempelkan di atas tembok atau kertas.
3. Kamu menyemprotkan cat ke seluruhnya.
4. Cat hanya menempel di bagian yang **berlubang**. Bagian yang tertutup karton tetap bersih.
5. Karton diangkat, dan muncullah gambar bintang.

Contoh di kehidupan sehari-hari: huruf nama sekolah atau nomor rumah yang dicat di dinding dengan pola rapi, biasanya dibuat dengan stensil.

## Hubungannya dengan CSS `mask`

Cara kerja `mask` mirip sekali:

| Stensil asli | CSS `mask` |
|---|---|
| Karton dengan lubang | Gambar mask |
| Bagian **berlubang** | Area **buram** pada mask (elemen terlihat) |
| Bagian **tertutup** | Area **transparan** pada mask (elemen tersembunyi) |
| Cat yang disemprot | Isi elemen (foto, warna, teks) |

Jadi saat saya bilang "mask itu seperti stensil", maksudnya: mask adalah penutup yang menentukan bagian mana dari elemen yang **tembus terlihat** dan bagian mana yang **tertutup**.

Satu perbedaan kecil: stensil asli hanya punya dua kondisi (lubang atau tertutup), sedangkan `mask` juga bisa **setengah-setengah** (semi-transparan), sehingga menghasilkan efek memudar.

Sudah lebih jelas? Kalau ya, kita lanjut praktik `mask-image` atau ke `mask-repeat`.
