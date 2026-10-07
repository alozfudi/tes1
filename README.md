# tes1

Repository ekstensi tes1 untuk CloudStream.

## Instalasi

CloudStream → Pengaturan → Ekstensi → Tambah repository:

```text
https://raw.githubusercontent.com/alozfudi/tes1/main/repository.json
```

Buka repository **tes1**, lalu install **tes1**. Jika versi lama masih terpasang dengan nama berbeda, hapus versi lama terlebih dahulu.

## Versi 3

Nama tampilan dan manifest plugin menggunakan **tes1**. Plugin menggunakan satu instance CloudflareKiller bawaan CloudStream untuk halaman dan video, dengan halaman utama berurutan dan fallback untuk respons 403/503 serta halaman challenge. Parsing dan fitur provider tetap dipertahankan.

Build Gradle berhasil dan arsip plugin telah diperiksa: manifest versi 3 serta classes.dex valid. Penanganan Cloudflare saat berjalan belum diuji di perangkat Android.

Kredit sumber: [ANDonekey/cloudstreamPlugins](https://github.com/ANDonekey/cloudstreamPlugins).
