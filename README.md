# Struk SPBU — halaman unduhan

Halaman statis untuk informasi dan unduhan aplikasi Struk SPBU, serta sumber data versi yang dibaca oleh aplikasi Android.

## Isi folder

| Berkas | Fungsi |
| --- | --- |
| `index.html` | Halaman unduhan, fitur, panduan pemasangan, dan informasi rilis |
| `style.css` | Tema biru premium yang diselaraskan dengan tampilan aplikasi `STRUK-SPBU-NEW` |
| `version.json` | Metadata versi dan catatan rilis yang dibaca halaman ini dan aplikasi |
| `logo.png` | Logo Struk SPBU untuk header situs |
| `icon-512_2.png` | Ikon aplikasi untuk hero dan favicon |

## Publikasi dengan GitHub Pages

1. Unggah isi folder ini ke root branch yang dipakai GitHub Pages.
2. Pastikan `URL_VERSI` di `www/script.js` menunjuk ke alamat `version.json` yang dipublikasikan.
3. Pastikan berkas versi dan APK yang diunggah benar-benar berasal dari build aplikasi yang sama.

## Sebelum merilis APK terbaru

- `version` dan `version_code` di `version.json` harus selaras dengan versi aplikasi di `config.xml` dan `APP_VERSION` di `www/script.js`.
- Ganti `url_download` dengan URL HTTPS APK untuk versi yang benar-benar dirilis.
- Perbarui `ukuran` berdasarkan ukuran APK hasil build.
- Perbarui `tanggal_rilis` dan `catatan` sesuai rilis yang dipublikasikan.

**Penting:** arsip yang diberikan berisi kode aplikasi, tetapi tidak berisi APK versi `1.2.0` atau tautan unduh baru yang dapat diverifikasi. Karena tautan lama secara eksplisit bernama `STRUK-SPBU-V1.1.4.apk`, `url_download` sengaja dikosongkan agar situs tidak menyajikan tautan yang berpotensi mengunduh versi lama. Tombol unduh akan aktif otomatis setelah `url_download` diisi dengan URL HTTPS yang valid.

Aplikasi memeriksa `version.json` untuk membandingkan versi server dengan `APP_VERSION` pada perangkat. Jangan menaikkan nomor versi di `version.json` melebihi versi aplikasi yang benar-benar tersedia.
