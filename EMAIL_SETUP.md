# Setup Email Simple - Ruang Kreatif

## Cara Kerja Fitur Email

Fitur email ini menggunakan JavaScript sederhana tanpa pihak ketiga. Ketika user mengisi form dan klik "Daftar Sekarang", maka:

1. Data form akan divalidasi
2. Aplikasi email default di komputer user akan terbuka
3. Email akan terisi otomatis dengan data pendaftar
4. User tinggal klik "Send" di aplikasi email mereka

## Konfigurasi

### 1. Ganti Email Admin

Buka file `index.html` dan cari baris ini:

```javascript
const adminEmail = "admin@ruangkreatif.com"; // Ganti dengan email admin Anda
```

Ganti `admin@ruangkreatif.com` dengan email admin yang sebenarnya, contoh:

```javascript
const adminEmail = "owner@tokogelang.com";
```

### 2. Customize Subject Email

Jika ingin mengubah subject email, ganti baris ini:

```javascript
const subject = "Pendaftaran Baru - Ruang Kreatif";
```

Menjadi:

```javascript
const subject = "Pendaftaran Newsletter - Toko Gelang";
```

## Kelebihan Metode Ini

✅ **Simple**: Tidak perlu setup server atau API eksternal
✅ **No Dependencies**: Pure JavaScript, tidak perlu library
✅ **Privacy**: Data tidak melewati server pihak ketiga
✅ **Universal**: Bekerja di semua browser dan OS
✅ **Free**: Tidak ada biaya tambahan

## Kekurangan

❌ **Manual**: Admin harus manual buka email untuk lihat pendaftar
❌ **Tergantung User**: User harus punya aplikasi email di komputer
❌ **No Database**: Data tidak tersimpan otomatis di database

## Testing

1. Buka website di browser
2. Scroll ke bagian "Dapatkan Gratis Ongkir"
3. Isi nama dan email
4. Centang/tidak centang berlangganan
5. Klik "Daftar Sekarang"
6. Aplikasi email default akan terbuka (Outlook, Mail, Gmail, dll)
7. Klik "Send" untuk mengirim email

## Aplikasi Email yang Didukung

- **Windows**: Outlook, Mail, Thunderbird
- **Mac**: Mail, Outlook, Thunderbird
- **Linux**: Thunderbird, Evolution
- **Webmail**: Gmail, Yahoo (jika diset sebagai default)

## Troubleshooting

**Q: Aplikasi email tidak terbuka?**
A: User perlu setting aplikasi email default di OS mereka.

**Q: Email tidak terkirim?**
A: User harus manual klik "Send" di aplikasi email yang terbuka.

**Q: Ingin otomatis terkirim?**
A: Gunakan alternatif seperti EmailJS atau Formspree (butuh setup eksternal).

## Alternative Advanced

Jika ingin fitur lebih canggih, bisa gunakan:

1. **EmailJS** - gratis 200 email/bulan
2. **Formspree** - gratis 50 form/bulan
3. **Netlify Forms** - jika hosting di Netlify
4. **Server sendiri** - butuh backend PHP/Node.js
