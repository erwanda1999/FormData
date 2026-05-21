# Cara Mengaktifkan Database Online

Aplikasi sudah disiapkan untuk menyimpan data online memakai Firebase Firestore.

## 1. Buat Firebase Project

1. Buka https://console.firebase.google.com/
2. Klik `Add project`.
3. Ikuti proses sampai project selesai dibuat.

## 2. Buat Firestore Database

1. Masuk ke project Firebase.
2. Buka menu `Build > Firestore Database`.
3. Klik `Create database`.
4. Untuk uji coba, pilih mode test terlebih dahulu.
5. Pilih lokasi server, lalu buat database.

## 3. Ambil Firebase Config

1. Buka `Project settings`.
2. Pada bagian `Your apps`, pilih ikon Web `</>`.
3. Daftarkan app web.
4. Firebase akan memberi config seperti ini:

```js
const firebaseConfig = {
  apiKey: "...",
  authDomain: "...",
  projectId: "...",
  storageBucket: "...",
  messagingSenderId: "...",
  appId: "..."
};
```

## 4. Isi Config di index.html

Buka `index.html`, cari bagian:

```js
const firebaseConfig = {
  apiKey: '',
  authDomain: '',
  projectId: '',
  storageBucket: '',
  messagingSenderId: '',
  appId: ''
};
```

Isi nilainya dengan config dari Firebase.

## 5. Deploy Ulang

Upload ulang `index.html` ke hosting online, misalnya Netlify atau GitHub Pages.

Jika config benar, badge di atas aplikasi akan berubah dari:

```text
Database Lokal
```

menjadi:

```text
Database Online
```

## Catatan

- Collection Firestore yang dipakai: `formInputUsers`
- Jika Firebase belum dikonfigurasi, aplikasi tetap menyimpan data lokal memakai IndexedDB.
- Foto profil disimpan sebagai base64 di Firestore. Untuk foto besar, sebaiknya gunakan gambar kecil agar tidak melebihi batas ukuran dokumen Firestore.
