---
title: "Otomatis Deploy Github Pages Dengan Hugo Dan Actions"
date: 2021-03-05T04:16:45+07:00
draft: 
---

# Deploy Github Pages dengan Hugo dan Github Actions

## Persiapan

Diasumsikan bahwa kamu telah tahu cara membuat 

- Github Pages
- Web Hugo di lokal komputer

## Tahapan

Dalam membangun dan menerbitkan situs web, aku menggunakan [action-gh-pages](https://github.com/peaceiris/actions-gh-pages). Ada dua cara penggunaan action-gh-pages:

1. Menggunakan repositori tunggal
2. Menggunakan beberapa repositori

Dalam  tulisan ini, aku menggunakan beberapa repositori. Konsepnya adalah satu repositori untuk menyimpan *Hugo Sumber*, dan satu repository meng-*clone* file yang telah di-*generate* oleh Hugo di folder `public`.

### Syarat

1. Membuat dan mengkonfigurasi Github Pages
2. Membuat repositori untuk file-fie *Hugo Sumber*
3. Membangun situs Hugo (`hugo new site bismillah`)
4. Menguji situs Hugo (`hugo server -D`)

### Mengonfigurasi Github Actions

Mengatur *key* pada kedua repositori agar bisa situs bisa diterbitkan.

1. Dapatkan *deploy key* dengan perintah berikut:  
```bash
ssh-keygen -t rsa -b 4096 -C "$(git config user.email)" -f master -N ""
# You will get 2 files:
#   master.pub (public key)
#   master     (private key)
```

2. Tambahkan *private key* dengan nama ACTIONS_DEPLOY_KEY dalam repositori sumber.  
Masuk ke *Repositori Sumber > Settings > Secrets > Add new secrets* dan beri nama ACTIONS_DEPLOY_KEY lalu tempel dari apa yang ada dalam file `master`.

3. Tambahkan *public key* sebagai *deployment key* dalam Github Pages yang akan diterbitkan misalnya repository kva.github.io.
Masuk ke *Repository Github Pages > Settings > Deploy Key > Add new deploy key* dan atur nama file yang sesuai dengan *private key* (misalnya: Publik Key untuk deploy situs), lalu tempel dari konten yang ada di file `master.pub`.

4. Tambahkan file berikut: `.github/workflows/pages.yml` di repositori Hugo Sumber dan ganti *username/external-repository* dengan username dan nama repositori milikmu.

```yml
name: hugo publish

on:
  push:
    branches:
    - master

jobs:
  build-deploy:
    runs-on: ubuntu-18.04
    steps:
    - uses: actions/checkout@v1
      # with:
      #   submodules: true

    - name: Setup Hugo
      uses: peaceiris/actions-hugo@v2
      with:
        hugo-version: '0.59.1'

    - name: Build
      run: hugo --minify

    - name: Deploy
      uses: peaceiris/actions-gh-pages@v2
      env:
        ACTIONS_DEPLOY_KEY: ${{ secrets.ACTIONS_DEPLOY_KEY }}
        EXTERNAL_REPOSITORY: username/external-repository
        PUBLISH_BRANCH: master
        PUBLISH_DIR: ./public
      with:
        emptyCommits: false
        commitMessage: ${{ github.event.head_commit.message }}
```

5. Commit dan Push Hugo Sumber.
6. Periksa workflow dalam tab Action di repositori Hugo Sumber
Setelah *workflow* beres dan commit terlihat di repositori Github Pages, Github Pages berhasil diterbitkan.


## Referensi
[medium.com/@asishrs](https://medium.com/@asishrs/automate-your-github-pages-deployment-using-hugo-and-actions-518b959a51f9)
