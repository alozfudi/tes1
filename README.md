# Hanime1 CloudStream Repository

Repository khusus Hanime1Provider versi 2.

## Tambahkan ke CloudStream

Pengaturan → Ekstensi → Tambah repository. Masukkan URL berikut:

```text
https://raw.githubusercontent.com/alozfudi/hanime1-cloudstream/main/repository.json
```

Buka repository **Hanime1 Cloudflare Fix**, lalu install **Hanime1.me**.

## Perubahan versi 2

- Satu instance `CloudflareKiller` bawaan CloudStream untuk halaman dan interceptor video.
- `usesWebView = true` dan `sequentialMainPage = true`.
- Fallback untuk respons 403/503 dan HTML challenge Cloudflare.
- Parsing, kategori, pagination, pencarian, metadata, rekomendasi, serta ekstraksi link tetap dipertahankan.

Build `:Hanime1Provider:make` berhasil dengan Gradle 8.13, JDK 17, Android SDK 35 dan Kotlin 2.3.0. Arsip `.cs3` diverifikasi mengandung manifest versi 2 dan DEX valid. Penanganan Cloudflare saat dijalankan belum diuji di perangkat Android.

Sumber awal dan kredit: [ANDonekey/cloudstreamPlugins](https://github.com/ANDonekey/cloudstreamPlugins).
