# nimek-cli

CLI untuk nonton anime subtitle Indonesia dari terminal dengan dukungan multi-provider.

**Provider yang didukung:**
- [sokuja.uk](https://x6.sokuja.uk) (default)
- [nitrot.vercel.app](https://nitrot.vercel.app)

## Install

### Windows (Git Bash)

1. Install [Git for Windows](https://git-scm.com/download/win)
2. Install dependensi:
```bash
winget install fzf mpv
```
3. Install nimek-cli:
```bash
curl -sL https://raw.githubusercontent.com/dhodo999/nimek-cli/main/nimek-cli -o /c/Users/$USERNAME/.local/bin/nimek-cli
chmod +x /c/Users/$USERNAME/.local/bin/nimek-cli
```

### Termux (Android)

1. Install dependensi:
```bash
pkg install curl fzf
```
2. Install MPV dari [Play Store](https://play.google.com/store/apps/details?id=is.xyz.mpv) atau F-Droid
3. Install nimek-cli:
```bash
curl -sL https://raw.githubusercontent.com/dhodo999/nimek-cli/main/nimek-cli -o $PREFIX/bin/nimek-cli
chmod +x $PREFIX/bin/nimek-cli
```

> Ganti `$USERNAME` dengan username Windows kamu.

## Penggunaan

```
nimek-cli [opsi] [judul anime]

Opsi:
  -c, --continue              Lanjut dari riwayat tontonan
  -e, --episode <n|n-m>       Tonton episode tertentu atau rentang (mis. 3 atau 1-5)
  -q, --quality <kualitas>    Pilih kualitas (360p, 480p, 720p, 1080p)
  -p, --provider <provider>   Pilih provider (sokuja atau nitrot, default: sokuja)
  -V, --version               Tampilkan versi
  -h, --help                  Tampilkan bantuan

Provider:
  sokuja    - https://x6.sokuja.uk (default)
  nitrot    - https://nitrot.vercel.app

Contoh:
  nimek-cli                                  Mode pencarian interaktif
  nimek-cli "one piece"                      Langsung cari anime (sokuja)
  nimek-cli -c                               Lanjut dari riwayat
  nimek-cli -e 5 "one piece"                 Tonton episode 5
  nimek-cli -e 1-3 -q 1080p "naruto"         Tonton episode 1-3 kualitas 1080p
  nimek-cli -p nitrot "frieren"              Cari anime dengan provider nitrot
  nimek-cli -p nitrot -q 720p "one piece"    Gunakan nitrot dengan kualitas 720p
```

## Riwayat

Disimpan di `~/.local/state/nimek-cli/history`.

## Uninstall

### Windows (Git Bash)

```bash
# Hapus script
rm /c/Users/$USERNAME/.local/bin/nimek-cli

# Hapus riwayat (opsional)
rm -rf ~/.local/state/nimek-cli
```

### Termux (Android)

```bash
# Hapus script
rm $PREFIX/bin/nimek-cli

# Hapus riwayat (opsional)
rm -rf ~/.local/state/nimek-cli
```

## Lisensi

[MIT](LICENSE)
