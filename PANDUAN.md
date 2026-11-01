# KisahNada-Setup.exe

Paket Windows 10/11 x64 memasang runtime Python, mesin suara, FFmpeg/FFprobe, frontend dan server lokal. Pengguna tidak perlu memasang WSL/Ubuntu/Python atau mengetik perintah terminal.

1. Ambil `KisahNada-Setup.exe` dari hasil build di `/workspace/artifacts`.
2. Klik dua kali, ikuti wizard, lalu pilih **Buka KisahNada**. Instalasi menggunakan akun Windows saat ini, tanpa meminta hak administrator.
3. Gunakan pintasan **KisahNada** pada Desktop/Start untuk membuka lagi. Edge membuka jendela aplikasi; jika tidak tersedia, browser bawaan dipakai.
4. Tombol matahari/bulan pada header mengganti tema terang/gelap. Pilihan bertahan setelah aplikasi dimuat ulang; sebelum memilih, tema mengikuti sistem.

Jendela status menyediakan **Buka aplikasi**, **Folder data / log**, dan **Tutup studio**. Biarkan studio terbuka saat memproses. Aplikasi menolak penutupan biasa ketika job atau pemasangan model masih berlangsung. Installer tidak menerbitkan aplikasi ke internet; server hanya mendengarkan loopback lokal.

## Nyanyian AI

Di AI Song, klik **Pasang mesin nyanyian AI**, daftar/masuk akun studio lokal, lalu konfirmasikan unduhan. Ini menjalankan pemasang Windows native dengan Python terbundel: membuat runtime CPU terpisah, memasang dependency ACE-Step, memverifikasi source resmi dan mengunduh/verifikasi checkpoint. Model besar diunduh setelah konfirmasi, bukan dimasukkan ke setup awal. Tidak ada API berbayar atau fallback narasi/instrumental.

Perlu internet, ruang disk banyak GB, dan RAM memadai. CPU dapat lambat. Progress dan kegagalan ditampilkan; kegagalan perlu dicoba ulang secara manual. Instalasi runtime Windows dan inferensi ACE-Step perlu diuji pada komputer pengguna sebelum kualitas atau keberhasilan dinyatakan pasti. Impor CPU Linux dan tes transport bukan bukti nyanyian Windows.

Setelah status model terverifikasi, tulis lirik pendek pada Lyrics, pilih genre/vokal dan durasi 30 detik, lalu **Buat lagu bernyanyi AI**. Dengarkan hasil di Library, kemudian unduh. My Voice/kloning artis belum didukung. Groq tetap layanan lirik opsional dengan key dan paket gratis terkonfirmasi; tidak ada key di dalam installer. Draf template dapat dipakai tanpa key dan dilabeli bukan AI.

## Data, pembaruan dan distribusi

Instalasi: `%LOCALAPPDATA%\Programs\KisahNada`. Data/model/log: `%LOCALAPPDATA%\KisahNada`. Uninstaller mempertahankan data/model. Tutup studio sebelum memperbarui, dan cadangkan karya penting. Bersihkan data browser hanya setelah membuat cadangan Library.

Installer belum ditandatangani sertifikat penerbit; SmartScreen/antivirus dapat memperingatkan atau memblokirnya. Jangan menonaktifkan perlindungan Windows. Catat penolakan untuk diagnosis. Tidak ada klaim pengujian langsung di komputer pengguna.

Source, lisensi dan provenance komponen disertakan. Python Windows resmi diperoleh dari NuGet dengan hash SHA512 katalog, eSpeak/MSVC dari wheel PyPI dengan SHA256, FFmpeg BtbN dengan checksum rilis. Versi/hash terkunci pada `packaging/windows/dependencies.lock.json`. Tool NSIS diperoleh dari metadata Debian yang ditandatangani. Runtime/model besar diabaikan Git. Build ulang melalui `scripts/build-windows.py`; memerlukan tooling NSIS lokal yang tercatat di start instructions. Ini paket pribadi untuk percobaan, belum rilis publik yang ditandatangani dan diverifikasi.
