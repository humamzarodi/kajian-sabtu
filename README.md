# Informasi Kajian Sabtu Pagi Ba'da Subuh — Masjid An-Nuur Kotagede

Halaman pengumuman untuk satu kegiatan kajian, lengkap dengan ruang foto
penceramah.

## Struktur folder

```
kajian-sabtu-pagi/
├── index.html
├── css/style.css
└── assets/
    ├── logo.svg
    └── photo-placeholder.svg   ← ikon placeholder, ganti dengan foto asli
```

## Cara memasang foto penceramah

1. Simpan foto penceramah (format .jpg atau .png) ke folder `assets/`,
   misalnya beri nama `foto-penceramah.jpg`.
2. Buka `index.html`, cari blok ini:
   ```html
   <div class="photo-slot">
     <img class="icon" src="assets/photo-placeholder.svg" alt="">
     <span>RUANG FOTO PENCERAMAH</span>
   </div>
   ```
3. Ganti seluruh blok tersebut menjadi:
   ```html
   <div class="photo-slot">
     <img src="assets/foto-penceramah.jpg" alt="Foto Ustadz Dr. Ridwan Furqoni" style="width:100%;height:100%;object-fit:cover;">
   </div>
   ```

## Cara mengubah informasi kajian

Semua detail (tema, nama penceramah, hari/tanggal, jam, tempat) ada di
bagian `<div class="poster-body">` pada `index.html` — tinggal ubah teks
di masing-masing elemen.

## Cara upload ke GitHub & tayangkan lewat GitHub Pages

1. Buat repository baru di GitHub (public).
2. Upload seluruh isi folder ini lewat "Add file → Upload files", atau lewat git:
   ```bash
   git init
   git add .
   git commit -m "Informasi kajian Sabtu pagi"
   git branch -M main
   git remote add origin https://github.com/USERNAME/NAMA-REPO.git
   git push -u origin main
   ```
3. Tambahkan file kosong bernama `.nojekyll` di root repo (mencegah error build).
4. Buka **Settings → Pages**, pilih branch `main` dan folder `/ (root)`, lalu **Save**.
5. Situs akan tayang di `https://USERNAME.github.io/NAMA-REPO/`.
