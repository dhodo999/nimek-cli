# nimek-cli

CLI untuk nonton anime subtitle Indonesia dari terminal. Source: [sokuja.uk](https://x6.sokuja.uk)

## Dependensi

`curl` `fzf` `mpv`

**Windows (Git Bash):** `scoop install fzf mpv`  
**Termux:** `pkg install curl fzf` + install MPV dari Play Store/F-Droid

## Install

**Windows (Git Bash):**
```bash
cp nimek-cli /c/Users/$USERNAME/scoop/shims/nimek-cli
```

**Termux / Linux:**
```bash
cp nimek-cli $PREFIX/bin/nimek-cli
chmod +x $PREFIX/bin/nimek-cli
```

## Penggunaan

```
nimek-cli [opsi] [judul anime]

Opsi:
  -c, --continue            Lanjut dari riwayat tontonan
  -e, --episode <n|n-m>     Tonton episode tertentu atau rentang (mis. 3 atau 1-5)
  -q, --quality <kualitas>  Pilih kualitas (480p, 720p, 1080p)
  -V, --version             Tampilkan versi
  -h, --help                Tampilkan bantuan

Contoh:
  nimek-cli                           Mode pencarian interaktif
  nimek-cli "one piece"               Langsung cari anime
  nimek-cli -c                        Lanjut dari riwayat
  nimek-cli -e 5 "one piece"          Tonton episode 5
  nimek-cli -e 1-3 -q 1080p "naruto"  Tonton episode 1-3 kualitas 1080p
```

## Riwayat

Disimpan di `~/.local/state/nimek-cli/history`.

## Lisensi

[MIT](LICENSE)
