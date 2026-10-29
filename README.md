# Ngobrol Berempat

Chat teks dan voice chat peer-to-peer untuk maksimal 4 orang. Satu file (`index.html`), tanpa server sendiri, bisa langsung di-host di GitHub Pages.

## Cara pasang di GitHub

1. Buat repo baru di GitHub (publik, mis. `ngobrol-berempat`).
2. Upload `index.html` ke repo (tombol **Add file → Upload files**), lalu **Commit**.
3. Buka **Settings → Pages**. Di **Build and deployment**, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
4. Tunggu sekitar 1 menit. Alamatnya: `https://USERNAME.github.io/ngobrol-berempat/`

## Cara pakai

1. Semua orang buka alamat di atas.
2. Isi nama dan **kode ruangan yang sama** (mis. `kami-berempat`), lalu **Masuk**.
3. Izinkan akses mikrofon saat diminta. Tanpa izin, kamu tetap bisa chat dan mendengar.
4. Tombol **Salin link undangan** membuat link yang sudah berisi kode ruangan.

## Cara kerjanya

- Setiap orang mengambil slot 1–4 di ruangan. Slot kelima ditolak, jadi maksimal 4 orang.
- Chat lewat WebRTC data channel, suara lewat WebRTC audio, langsung antar-perangkat. Pesan tidak disimpan di server mana pun dan hilang saat halaman ditutup.
- Server perantara publik PeerJS hanya dipakai untuk saling menemukan di awal (signaling), bukan untuk meneruskan chat atau suara.

## Catatan

- Harus dibuka lewat HTTPS (GitHub Pages sudah HTTPS), kalau tidak mikrofon diblokir browser.
- Kalau jaringan ketat (kantor, kampus, sebagian data seluler), koneksi langsung bisa gagal. Halaman ini memakai relay TURN publik gratis sebagai cadangan, tapi kualitasnya tidak dijamin. Untuk yang lebih stabil, ganti `RTC_CONFIG` di `index.html` dengan server TURN milikmu sendiri.
- Kode ruangan bukan password: siapa pun yang tahu kodenya bisa masuk kalau masih ada slot kosong. Pakai kode yang sulit ditebak.
- Pakai headset supaya suara tidak menggema.
