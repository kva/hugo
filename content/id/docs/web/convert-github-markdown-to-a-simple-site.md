---
title: "Membuat Situs dari File Markdown"
description: "Cara mudah membuat web yang sederhana"
date: 2021-03-05T04:16:45+07:00
draft: false
---

File-file .md (Markdown) yang ada di repositori dapat dijadikan halaman web tanpa mengubahnya sama sekali.

## Tahapan

1. Tentukan repositori yang akan diaktifkan sebagai Github Pages.
2. Buat file `_.config.yml`
Berikut ini adalah konten yang perlu ditempel di file `_.config.yml`:

```yml
plugins:
  - jekyll-relative-links
relative_links:
  enabled: true
  collections: true
include:
  - CONTRIBUTING.md
  - README.md
  - LICENSE.md
  - COPYING.md
  - CODE_OF_CONDUCT.md
  - CONTRIBUTING.md
  - ISSUE_TEMPLATE.md
  - PULL_REQUEST_TEMPLATE.md
```

Pada dasarnya ini hanya konfigurasi standar Github Pages untuk menangani file-file Markdown.

3. Aktifkan Github Pages
Masuk ke `Settings` > `Option` > `Github Pages` > `Source`. Pilh `master branch`, lalu `Save`.
4. Pilih Tema yang sesuai

## Catatan

- Untuk mengakses file, hanya perlu mengakses url file tanpa menambahkan .md.
- Untuk membuat relatif URL, gunakan konfigurasi `_config.yml` yang menyediakan plugin untuk mengonversi URL
- Index dari website dapat menggunakan file `index.html` atau `README.md`. Jika kedua file ada, maka file `index.html` akan diutamakan.

## Referensi

[medium.com/@bolajiayodeji](https://medium.com/@bolajiayodeji/how-to-convert-github-markdown-files-to-a-simple-website-b08602d05e1c)
