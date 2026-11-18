# Mask Position 
Adalah Sebuah Properti Untuk Menentukan Posisi Untuk Stensi Yang Digunakan

> Dari AI

# Selanjutnya: `mask-position`

`mask-position` menentukan **di mana letak gambar mask** di dalam elemen. Ini paling berguna saat dipakai bersama `mask-repeat: no-repeat`, karena kalau mask diulang, posisinya hampir tidak terlihat.

## Nilai yang tersedia

**1. Kata kunci**

```css
mask-position: center;
mask-position: top;
mask-position: bottom right;
```

Pilihannya: `top`, `bottom`, `left`, `right`, `center`.

**2. Satuan panjang** (px, em, dll.), urutannya **horizontal lalu vertikal**

```css
mask-position: 20px 50px;
```

Artinya: 20px dari kiri, 50px dari atas.

**3. Persentase**

```css
mask-position: 50% 50%;   /* sama dengan center */
mask-position: 0% 0%;     /* pojok kiri atas (default) */
mask-position: 100% 100%; /* pojok kanan bawah */
```

## Contoh

```css
.kotak {
  width: 300px;
  height: 300px;
  background: linear-gradient(red, blue);
  mask-image: url(bintang.png);
  mask-size: 100px;
  mask-repeat: no-repeat;
  mask-position: center;
}
```

Hasilnya: satu bintang 100px muncul **tepat di tengah** elemen. Tanpa `mask-position`, bintang akan menempel di pojok kiri atas, karena nilai default-nya `0% 0%`.

## Cara membaca dua nilai

```css
mask-position: 30px 80px;
/*              ↑     ↑
             kiri→  atas↓  */
```

Kalau hanya menulis **satu nilai**, nilai kedua otomatis `center`:

```css
mask-position: 40px;  /* sama dengan 40px center */
```

## Ringkasnya

| Nilai | Posisi mask |
|---|---|
| `0% 0%` / `top left` | Pojok kiri atas (default) |
| `center` | Tengah |
| `100% 100%` / `bottom right` | Pojok kanan bawah |
| `20px 50px` | 20px dari kiri, 50px dari atas |

Selanjutnya kita bahas `mask-size`, yaitu mengatur **ukuran** mask (seperti yang sudah kita pakai sekilas di contoh, `mask-size: 100px`). Lanjut?
