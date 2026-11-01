# KisahNada Windows 0.3.1 — perbaikan runtime nyanyian

[Unduh installer Windows x64, 85.4 MB](https://github.com/Rosal894/Rosal894.github.io/raw/refs/heads/kisahnada-download-0.3.1/KisahNada-Setup.exe)

Versi 0.3.1 memperbaiki ketidakcocokan Python pada pemasang ACE-Step. Source ACE-Step memerlukan Python >=3.11,<3.13; worker versi 0.2/0.3 dibuat dengan Python 3.13. Paket ini menyertakan Python 3.12 terpisah untuk nyanyian, sementara aplikasi utama tetap Python 3.13. Tidak perlu memasang Python atau WSL manual.

- [Panduan](PANDUAN.md)
- [Source aplikasi](KisahNada-source.zip)
- [SHA256](KisahNada-Setup.exe.sha256)
- [Audit dependency Windows](Windows-dependency-audit.json)
- [Audit runtime CPU bersih](Singing-runtime-audit.json)

Model nyanyian tetap diunduh terpisah melalui tombol Pasang mesin nyanyian AI setelah konfirmasi. Kesiapan Windows memerlukan marker akhir import CPU dan checkpoint terverifikasi; instalasi parsial tidak dianggap siap. Runtime lama dan karya tidak ditimpa.

37 tes backend serta regresi browser lulus. Dependency dipasang pada lingkungan Linux Python 3.12 bersih dan API CPU berhasil diimpor; 22 dependency langsung memiliki wheel Windows yang sesuai. Pemeriksaan ini bukan bukti inferensi nyanyian atau keberhasilan pada Windows asli. Nyanyian Windows dan kualitas setara Song.ai belum teruji; My Voice belum didukung. Installer unsigned.

Tampilan studio 0.3, pencarian/filter koleksi, tinjau lirik dan tema gelap/terang tetap tersedia. AI lirik Groq memerlukan key/paket gratis terkonfirmasi; template dilabeli bukan AI. Tidak ada API key atau media pribadi di paket/source.

Source commit: 95ee8414843070dec316ba00ed6a72c46cade44a
SHA256 installer: 7c0890f0a7bdebe22ad96cf86715d1a3975c18300df9f2a19f3dbf1b3b71908b
