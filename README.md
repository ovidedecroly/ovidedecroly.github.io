# Ovide Academy - Zola Starter

Starter personal website berbasis **Zola** untuk `https://ovideacademy.github.io`.

## Isi Website

- Home
- Blog
- Research
- Teaching Materials
- Buku Saya
- Publications
- About

## Cara Pasang ke GitHub Pages

1. Buat repository bernama `ovideacademy.github.io` di akun/organization GitHub `ovideacademy`.
2. Clone repository dengan GitHub Desktop.
3. Copy semua isi folder starter ini ke folder repository lokal.
4. Di GitHub repository, buka `Settings -> Pages`.
5. Pilih `Source: GitHub Actions`.
6. Commit dan push dari GitHub Desktop.
7. Buka tab `Actions` dan tunggu workflow berhasil.
8. Website tampil di `https://ovideacademy.github.io`.

## Cara Menambah Artikel Blog

Buat file baru di:

```text
content/blog/judul-artikel.md
```

Contoh front matter:

```toml
+++
title = "Judul Artikel"
date = 2026-06-07
description = "Deskripsi artikel."
[taxonomies]
categories = ["Artificial Intelligence"]
tags = ["AI", "Deep Learning"]
+++
```

Tulis isi artikel di bawah front matter tersebut.

## Cara Menambah Buku

Buat file baru di:

```text
content/books/judul-buku.md
```

Contoh:

```toml
+++
title = "Judul Buku"
date = 2026-06-07
description = "Deskripsi buku."
[taxonomies]
categories = ["Buku"]
tags = ["AI", "Pendidikan"]
[extra]
cover = "/images/cover-buku.svg"
pdf = "/pdf/judul-buku.pdf"
status = "Draft"
+++
```

Simpan cover di:

```text
static/images/
```

Simpan PDF di:

```text
static/pdf/
```

## Test Lokal

Install Zola, lalu jalankan:

```bash
zola serve
```

Buka browser:

```text
http://127.0.0.1:1111
```

## Catatan

- Jangan commit folder `public/`; itu hasil build lokal.
- Folder `.github/workflows/zola.yml` wajib ikut ter-push agar GitHub Actions berjalan.
- Jika alamat bukan `ovideacademy.github.io`, ubah `base_url` di `config.toml`.
