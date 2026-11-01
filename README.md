# Sifu Android Lag Fix

![Ikon Sifu Lag Fix](icon.webp)

Bikin Sifu Android lebih ringan dan anti patah-patah. Ini aplikasi kecil yang membetulkan config bawaan di dalam APK Sifu milikmu sendiri, supaya game-nya jalan lebih enteng di HP kelas bawah dan menengah. Gratis, tanpa iklan, tanpa kunci-kuncian.

Aplikasi ini **tidak berisi game sama sekali**. Yang dipakai adalah berkas APK Sifu milik kamu sendiri.

## Kenapa Sifu terasa berat, dan kenapa trik folder config nggak mempan

Cara yang beredar itu nyuruh bikin file config di folder `Android/data`. Di build Sifu yang beredar, cara itu nggak dibaca sama game-nya, jadi nggak ada efeknya. Config aslinya matang di dalam berkas pak di dalam APK, dan di situlah aplikasi ini bekerja: nilainya diganti di tempat, ukuran berkas nggak berubah, isi game nggak diubah sama sekali.

## Yang diubah

- Kualitas bayangan, post-process, tekstur, dan efek diturunkan ke 0
- MSAA dimatikan
- Bloom dimatikan
- Kolam tekstur diperkecil
- Skala resolusi diturunkan sedikit (bawaan 1 jadi 0.8)
- Batas FPS tetap 45, nggak dikunci ke 30

Mulai versi 1.1, aplikasi ini membaca GPU HP kamu dan menyesuaikan profil yang dipakai game di HP itu (kelas bawah, menengah, atau atas), dan ada layar setelan lengkap: semua nilai grafis di profilmu ditampilkan dan bisa kamu atur sendiri nilainya. Ada tombol resep ringan sekali pencet buat yang nggak mau ribet, dan tombol kembali ke bawaan pabrik.

Resep kelas menengah sudah terbukti di HP beneran (POCO F5). Resep kelas lain ditandai apa adanya di dalam aplikasi sebagai belum diuji di HP aslinya.

## Cara pakai

1. Unduh berkas Sifu-Lag-Fix.apk dari repo ini, lalu pasang di HP kamu.
2. Buka, pilih berkas APK Sifu milikmu.
3. Aplikasi memeriksanya dan menampilkan nilai yang sekarang. Kalau cocok, pencet tombol betulkan. Hasilnya tersimpan sebagai `Sifu-LagFixed.apk` di folder Download.
4. Cadangkan dulu folder `Android/data/com.keplerinteractive.sifuthegame`, lalu hapus Sifu yang lama, pasang berkas baru tadi, dan kembalikan folder cadangannya. Buka pertama akan membongkar ulang isinya, itu normal.

## Kejujuran soal build yang didukung

Aplikasi ini terbukti di build Sifu `1.0.254260c` dengan berkas pak versi 11 yang tidak terenkripsi. Kalau build Sifu kamu beda bentuk, aplikasinya akan menolak dengan penjelasan, bukan memaksa lalu merusak berkasmu. Berkas yang sudah pernah dibetulkan juga akan terdeteksi dan ditolak untuk dibetulkan dua kali.

## Soal repo ini

Repo ini etalasenya saja: halaman produk dan berkas APK jadinya. Tidak ada kode sumber di sini dan tidak akan pernah ada. Aplikasinya gratis dipakai dan boleh kamu sebar lagi apa adanya, tapi bukan untuk dibungkus ulang pakai nama orang lain - aplikasi ini memeriksa tanda tangan pemiliknya dan menolak jalan kalau diganti.

## Dukungan

Kalau aplikasi ini ngebantu Sifu kamu jadi enak dimainkan, kamu bisa dukung lewat GitHub Sponsors atau Trakteer di bagian kanan atas repo ini. Sifatnya sukarela, semua fitur tetap terbuka buat semua orang.

Dibuat oleh ptraaa. Semoga frame-mu mulus dan bos terakhir menyerah duluan.

---

## English

Sifu Android Lag Fix is a small free app that patches the cooked graphics config inside your own Sifu APK, in place and byte-size-preserving, so the game runs lighter on low-end and mid-range phones. No game data is included or distributed - you supply your own APK. It detects your phone GPU class and patches the profile your phone actually uses, and since v1.1 it includes a full settings screen where every graphics value in your profile can be adjusted freely. Proven on build 1.0.254260c (pak v11, unencrypted); other layouts are refused loudly rather than patched blindly. This repository is a storefront only - product page and the finished APK, no source code. Free to use and share as-is; rebranding is not permitted and the app refuses to run when re-signed by someone else.
