# tes1

Repository ekstensi tes1 untuk CloudStream.

## Instalasi

CloudStream → Pengaturan → Ekstensi → Tambah repository:

```
https://raw.githubusercontent.com/alozfudi/tes1/main/repository.json
```

Install atau perbarui tes1 ke versi 4.

## Verifikasi di dalam CloudStream

1. Buka Pengaturan → Ekstensi → tes1 → ikon roda gigi.
2. Selesaikan verifikasi manusia secara manual pada halaman yang tampil.
3. Setelah situs terbuka, pilih **Gunakan sesi**.
4. Kembali ke beranda tes1 dan tekan refresh.

Halaman ini memakai sesi WebView aplikasi yang dibaca oleh CloudflareKiller bawaan CloudStream. Browser eksternal tidak diperlukan. Verifikasi dapat diperlukan lagi setelah aplikasi dimulai ulang atau sesi kedaluwarsa. Plugin tidak menjamin bahwa semua challenge Cloudflare dapat diselesaikan di setiap perangkat.

## Versi 4

Menambahkan layar verifikasi melalui pengaturan plugin dan petunjuk ketika sesi belum siap. Satu instance CloudflareKiller dipakai untuk request halaman dan video, dengan usesWebView, halaman utama berurutan, serta deteksi fallback 403/503 dan halaman challenge. Parsing, kategori, pencarian, pagination, detail, dan pemutaran provider dipertahankan.

Build Gradle berhasil. Arsip telah diperiksa: manifest versi 4 dan classes.dex valid. Alur interaktif belum diuji langsung pada perangkat Android pengguna.

Kredit sumber: [ANDonekey/cloudstreamPlugins](https://github.com/ANDonekey/cloudstreamPlugins).
