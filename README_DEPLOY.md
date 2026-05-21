# Cara Membuat Aplikasi Bisa Diakses Online

Aplikasi ini bisa diakses online dengan hosting static website karena seluruh aplikasi ada di `index.html`.

## Opsi cepat: Netlify Drop

1. Buka https://app.netlify.com/drop
2. Drag folder project ini ke halaman Netlify Drop.
3. Tunggu proses upload selesai.
4. Netlify akan memberi link website, contoh:

```text
https://nama-acak.netlify.app
```

Link itu bisa dibuka dari mana saja selama ada internet.

## Opsi lain: GitHub Pages

1. Buat repository baru di GitHub.
2. Upload file `index.html` ke repository tersebut.
3. Buka menu `Settings > Pages`.
4. Pilih branch utama, lalu simpan.
5. GitHub akan memberi link website, contoh:

```text
https://username.github.io/nama-repository/
```

## Catatan database

Data aplikasi saat ini memakai IndexedDB, yaitu database lokal di browser pengguna.

Artinya:

- Website bisa diakses online dari mana saja.
- Data yang diinput di laptop A tidak otomatis muncul di laptop B.
- Data akan tersimpan di browser/perangkat yang dipakai.

Kalau ingin data tersimpan online dan bisa dipakai bersama oleh Maker, Checker, dan Signer dari perangkat berbeda, aplikasi perlu ditambah backend/cloud database seperti Firebase, Supabase, atau server database sendiri.
