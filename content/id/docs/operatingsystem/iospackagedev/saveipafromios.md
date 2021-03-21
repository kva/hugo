---
title: "Menyimpan IPA dari Perangkat iOS"
description: "Untuk disimpan dalam komputer "
date: 2020-01-28T00:36:19+09:00
draft: false
---

Ada beberapa cara untuk menyimpan aplikasi dari perangkat iOS, salah satunya adalah dengan menggunakan frida-ios-dump.

## Tahapan

### Dalam perangkat iOS  

- Perangkat sudah di-*jailbreak*
- Tambahkan repo https://build.frida.re di Cydia
- Pasang tweak Frida

### Dalam komputer

- Pasang Frida

```bash
pip3 install frida-tools
```

- Pasang [frida-ios-dump](https://github.com/AloneMonkey/frida-ios-dump)

```bash
git clone https://github.com/AloneMonkey/frida-ios-dump.git
cd frida-ios-dump
pip3 install -r requirements.txt --upgrade
```
- Install [usbmuxd](https://iphonedevwiki.net/index.php/SSH_Over_USB)

```bash
brew install usbmuxd
```

- Hubungkan perangkat menggunakan ssh

```bash
iproxy 2222 44 & sleep 3
ssh -p 2222 root@localhost # default password: alpine
```

- Buka terminal baru dan dapatkan .ipa yang terdekripsi

```bash
cd frida-ios-dump
python3 dump.py "<your_bundle>" # default password: alpine
```

### Referensi

[https://alteral.github.io/note-8/](https://alteral.github.io/note-8/)
